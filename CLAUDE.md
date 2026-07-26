# Weekly Supplements & DTC Research Agent

This folder runs a standing weekly research digest. It is not a coding project.

Core focus: human supplements and pet supplements. General DTC/ecommerce is in scope only for the ecom-tech section and for rare huge-outlier stories — see the skill for the exact bar.

## What lives here
- `archive/` — one Markdown file per week (`YYYY-MM-DD.md`), the permanent record of every digest ever produced. Read recent files here before starting a new run to avoid repeating last week's items.
- `state.json` — links/items already reported. Check it before including a source; update it after each run.
- `brands.json` — the accumulated library of every brand this project has profiled (human + pet supplements). Check it before researching a brand from scratch; update it after each run. See the skill for the exact protocol.
- `opinion_leaders.json` — same idea, for the tracked opinion leaders and podcast guests (e.g. Limited Supply's guest log). Check it before researching a person from scratch; update it after each run.
- `.claude/skills/weekly-dtc-brief/SKILL.md` — the full step-by-step research procedure (sections, sources, format, search budget). A weekly run should invoke `/weekly-dtc-brief`.

## Always true
- Tone: executive-brief. Terse, skimmable, fact-first — no narrative throat-clearing.
- Never fabricate a source, and never fetch content from behind a LinkedIn/X login wall. If a claim can't be verified via a reachable source, say so rather than guessing.
- Every run produces: an updated `archive/YYYY-MM-DD.md` file, an updated `state.json`, and a new Claude Artifact (new link each week — do not overwrite prior weeks).
