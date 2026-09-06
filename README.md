# Schedule Builder — Proof of Concept

A University at Buffalo advising tool: pick a major to see its typical
semester-by-semester sequence (the same data and rendering as [UB Major
Flowsheets](https://jcgood.github.io/ub-cas-flowsheets/)), then explore
that major's own elective options and see each one's prerequisite
pathway — the chain of courses leading up to it, and how often each is
typically offered — before you register.

**Live site**: published via GitHub Pages from this repo.

## What this is — and isn't

This is an independently produced proof of concept, **not** a University
at Buffalo publication and **not** endorsed by UB, any UB school or
college, or the UB Curriculum Office.

The major sequence is parsed directly from the Undergraduate Catalog's
own "Curricular Plan" section (`catalogs.buffalo.edu`, 2026-2027 catalog
year) — a roadmap the catalog itself describes as non-binding, not an
authoritative requirements list. The Elective Planner is a planning aid,
not a requirement-completion checker: it shows a course's own
prerequisite chain and how often it's historically been offered, but
does **not** verify that a full plan satisfies the major, and does not
guarantee any course's future scheduling. Prerequisite chains are
extracted automatically from each course's own Requisites text and can
occasionally over-match (e.g. a course mentioned as an alternate
placement criterion, not a true prerequisite). Always confirm actual
requirements and course availability with HUB and an academic advisor.

## Coverage

All 259 UB undergraduate majors and combined degrees with undergraduate
Curricular Plan data (every college/school with undergraduate majors),
same program set as UB Major Flowsheets.

## Files

- `index.html` — the site itself, self-contained (no external
  dependencies beyond its own `data/` fetches).
- `data/{slug}.json` — one pre-rendered semester-sequence fragment per
  program, fetched on demand.
- `data/courses.json` — per-course prerequisite/corequisite/typical-
  offering data for the Elective Planner's pathway view.
- `data/electives.json` — per-major elective/choice-required options and
  their own quotas.

## Provenance

Built from a private repository maintained for UB academic-affairs work.
This repo publishes only the derived, already-public catalog-sequencing
and course data — not the source repository itself.
