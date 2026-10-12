# Nominating an inductee

The Hall of Weird grows one YAML file at a time. Every exhibit on the page is a
single file in `_data/inductees/` — merging a new file **is** the induction
ceremony: GitHub Pages rebuilds the site and the plaque appears shortly after.

## What belongs in the Hall

- **Genuinely weird, not great.** Nobody is inducted for excellence —
  only for being statistically or historically *impossible*. The best test:
  does the entry have one jaw-dropping number (`num`) that needs no further
  argument?
- **Verifiable.** Every claim must be checkable against
  [Baseball-Reference](https://www.baseball-reference.com/), the
  [MLB StatsAPI](https://statsapi.mlb.com/), or the Lahman database. Include
  the `bref:` links that prove it.
- **The right wing.**
  - `stats` — a player (or person) surfaced by an extreme-value query
  - `teams` — a whole franchise-season anomaly
  - `tales` — documented strange-but-true stories no stat table can hold

## How to submit

1. Fork this repo.
2. Copy the template for your wing from [`_templates/`](_templates/) —
   [`stats.yml`](_templates/stats.yml), [`teams.yml`](_templates/teams.yml), or
   [`tales.yml`](_templates/tales.yml) — to `_data/inductees/<slug>.yml`. Use the
   Baseball-Reference player id as the slug when there is one (`lastfi01.yml`),
   otherwise a kebab-case name (`1900-team-or-tale.yml`).
3. Fill in the fields (each wing's template documents every one, including the
   portrait cascade: `img` → `mlbam` CDN headshot → `logoId` team logo →
   initials tile).
4. Open a pull request — **one inductee per PR**, with a sentence on why it's
   impossible and where you verified it.

Not a git person? Open an issue with the story and the numbers instead — if it's
weird enough, it'll find its way in.

## Hard rules

- **No fabrications.** If it can't be verified, it's a tale — and even tales
  need documentation.
- **No image files.** Portraits are external `https` URLs only — Wikimedia
  Commons preferred. PRs adding binaries will be declined.

## Sources

Detectors run against: Chadwick Baseball Bureau / Lahman database (1871–2021) +
MLB StatsAPI (2022–present). Detectors are re-runnable queries — nominate a new
category and the Hall expands.

## Curation

The wall hangs in chronological order of each exhibit's `date` — when it
actually happened, not when it was merged. The curator may adjust dates,
colors, and prose before merging so the wing reads well as a whole.
Merge to `main` = inducted.
