---
name: weekly-dtc-brief
description: Produce the weekly Supplements & DTC research brief (human supplements, pet supplements, plus ecom tech). Run this every Monday, or on demand to test/tune it.
---

# Weekly Supplements & DTC Brief

## Objective
Research and compile a weekly brief covering news, trends, and brand stories from the **human supplement, pet supplement, and broader DTC/ecommerce** industries — enough to stay current on what's circulating among the community and its key opinion leaders.

**A first-class goal of running this every week is building durable, ever-growing reference libraries — `brands.json` and `opinion_leaders.json`.** These are not just a caching side-effect of the brief; growing them is itself part of the deliverable. Every run should leave both libraries measurably richer than it found them (new brands discovered, new guests logged, new notes on existing entries) — not merely consulted and left untouched. A run that produces a good brief but adds nothing to either library has under-delivered on this objective.

## Cadence & Scope
- **Frequency:** Weekly, targeting delivery every Monday.
- **Recency window:** Sections 1 and 3 cover only items from the **last 7 days**. If a fact can't be pinned to a verified publish date, label it `background` rather than treating it as this week's news — don't guess a date to make something fit.
- **Language:** English.
- **Tone:** Executive-brief — terse, skimmable, no narrative throat-clearing. Lead each item with the fact, not the setup.
- **Output:** A single Markdown file (`archive/YYYY-MM-DD.md`) organized under the headers below, plus a new Claude Artifact (new link each week — never overwrite a prior week).

---

## Section 1 — Industry News (10 headlines)

**Primary scope: human supplements and pet supplements.** General DTC/ecommerce/retail news (beauty, apparel, platforms, etc.) is *out of scope by default*.

The one exception: a **huge outlier** story — one that clears at least one of these bars:
- $100M+ deal size or valuation
- A leadership change at a brand with 9-figure+ revenue
- Major M&A of a well-known consumer brand
- Coverage independently picked up by 3+ trusted outlets

(Cody Plofker stepping down as CEO of Jones Road Beauty is the calibration example — beauty, not supplements, but big enough to clear the bar.) When in doubt, leave it out — the ten slots are for supplements first.

Within scope, prioritize:
- Funding rounds, revenue milestones, earnings
- M&A / acquisitions
- Notable brand collaborations or partnerships
- Market expansions (retail doors, new geographies)
- Notable new product launches
- Major campaign launches

**Format per item:** headline — 1–2 sentence summary — source link — publish date.

**Hygiene rule:** max **one headline per brand**. If a brand has multiple stories in one week, pick the more significant and drop the rest (or fold the second into the first item's summary).

### 1a — Competitor & Emerging Brand Watch

Same format, dedicated to brand-level moves (launches, campaigns, funding, expansions, partnerships, unusual marketing) across **both human and pet supplements**.

Anchor brands — track these at minimum, but they're a starting point, not the whole list:
- **Pet supplements:** Zesty Paws, PetLab Co., DogSuppy (Belgium), Finn, Balto
- **Human supplements:** Gruns, IM8, Holy

Beyond the anchors, actively scan for **other notable or emerging brands** making news this week in either category — the goal is a picture of the market, not just these names. If an anchor brand has no news this week, say so plainly ("no news this week") rather than padding with filler.

**This scan is not optional and is not satisfied by whatever surfaces incidentally in the Section 1 sweep.** Every run, execute at least 2 dedicated discovery searches per category — one for each of human and pet supplements — aimed specifically at finding brands not already in `brands.json`. Rotate the angle run to run so it doesn't go stale (e.g. "new [pet/human] supplement brand launch [month year]", "emerging [category] brand funding [year]", "[category] supplement brand viral growth [year]", a specific subreddit search). If these searches turn up nothing new, say so explicitly ("ran discovery searches on X and Y, no new brands found") rather than silently omitting the step — the report should show the scan happened, not just its results.


**Sourcing methodology (applies to all sections):** Start from trusted outlets first, then expand to secondary sources (Reddit, general search, aggregators) to fill gaps or corroborate. Don't let secondary/SEO content override what a trusted outlet or primary source already covered.

**Trusted outlets:**
- General DTC/ecommerce: Modern Retail, Digiday, Retail Dive, Glossy
- Supplement-vertical trade press: NutraIngredients (US and Europe editions), Nutritional Outlook, SupplySide Supplement Journal, NBJ (Nutrition Business Journal), PetfoodIndustry.com, Pet Food Processing
- Secondary: Reddit (r/ecommerce, r/Entrepreneur, r/Supplements, r/dogs), general search, aggregators

**Note on LinkedIn/X:** most posts sit behind a login wall and aren't reliably reachable by search/fetch tools, and automating around that (fake sessions, scraping authenticated pages) isn't something to build — it violates both platforms' terms. Workarounds: (1) search for the public, indexed version of a post; (2) rely on cross-posted content elsewhere — Substack, YouTube, podcast show notes — which is usually the primary source anyway; (3) a logged-in manual check via Claude in Chrome is fine as a one-off, not something to lean on for the automated weekly pull. If a claim can't be verified directly, say so rather than guessing at the content.

**Disambiguation:** common names collide (e.g. searching "Moiz Ali" surfaces an unrelated Streamlabs/Stonks founder ahead of the Native Deodorant founder this brief means). Anchor ambiguous-name searches with a distinguishing term — the person's company, brand, or a known fact about them — before trusting the result.

---

## Section 2 — Brand Spotlight (1 brand)

**Scope: a supplement brand — human or pet — global.** Select one that has shown standout growth over the **trailing 6–12 months**, or a huge outlier-scale success story (e.g. Gruns, IM8, Holy are the kind of brand this section is built for). Sources cited can be older than 7 days as long as they support the growth story — but the growth claim itself should rest on something from the trailing 6–12 months, not a stale valuation headline with only forward-looking targets attached (a prior run picked Vuori on mostly Dec-2024 data — avoid repeating that gap; if the freshest evidence you can find is old, say so rather than presenting it as current).

**Geography: do not prefer EU by default.** EU/UK brands are genuinely interesting and worth surfacing, but US brands tend to be bigger and faster-growing — don't let a geographic tiebreaker cost the strongest story of the week. When multiple brands qualify in a given week, pick by strength/verifiability of the growth story first; briefly name the runner-ups in the notes rather than picking one for geographic balance.

Cover:
- Why has it grown? What's driving the attention?
- Acquisition channels and tactics
- Retention/loyalty tactics
- Primary marketing channels
- Geographic markets
- What makes the business model unique?

**Target length:** ~300–400 words, plus sources (LinkedIn, X, publications, podcast mentions, acquisition news).

---

## Section 3 — Ecom Tech (5–8 items)

Unchanged scope — news and updates in the ecommerce tech world generally (not supplement-specific):
- New or notable apps that help DTC operators
- Apps showing strong growth
- Shopify product/platform updates
- Anything relevant to using Shopify Markets for EU expansion

Same format as Section 1: item — summary — source link — date. Same 7-day window and `background` labeling rule as Section 1.

---

## Research Approach — Opinion Leaders

Check recent posts, newsletters, and podcast appearances (past 7 days) from — but not limited to:
- **Nik Sharma** (including guests on his *Limited Supply* podcast — treat notable guests as leads worth researching individually)
- **Moiz Ali** (Native Deodorant — disambiguate, see note above)
- **Cody Plofker**
- **Dara Denney**
- **Andrew Youderian**
- **Harley Finkelstein**
- **Kurt Elster**

Prefer primary sources (the person's own post or podcast episode) over secondhand recaps or aggregator summaries.

**Do a real per-person check, not one generic name search.** A single "<name> news" query that comes back empty is not sufficient evidence someone had nothing to say this week — check their actual channel. For podcast hosts (Nik Sharma, Kurt Elster, and any others with a known show), check the podcast's own recent-episodes list directly, not just a name search — Limited Supply publishes weekly, so a "nothing found" result for Nik Sharma in a given week should be treated as a signal to check harder, not an answer. Report status **per person** in the notes (found + cited, or "checked <channel/platform>, nothing in-window"), not just an aggregate line for the whole list — this makes it visible when a check was shallow versus genuinely empty.

**`opinion_leaders.json`** (project root) is the library for this — same pattern and same standing as `brands.json`: growing it is a real objective of each run, not just a lookup cache. Read it first: it has each person's known channels/podcast, `last_checked`, and running notes, so you're not rediscovering someone's platform from scratch every week. Nik Sharma and Moiz Ali specifically **co-host Limited Supply** — checking that one podcast's recent-episodes list covers both of them, don't search them separately. Guests on Limited Supply are logged in `_limited_supply_guest_log`; treat notable new guests as individual research leads (per the Objective above), and append newly found guests to that log with episode/date. After the run, bump `last_checked` for every person touched, same discipline as the brand library.

---

## Brand Library

`brands.json` (project root) is a growing roster of every brand this skill has ever profiled. It serves two purposes equally: stop re-deriving a brand's basic profile from scratch every week, **and** build a genuinely valuable, ever-expanding asset over time. Treat "did the library grow this week" as a real success criterion, not an incidental side-effect.

**Before researching Section 1a or a Section 2 candidate:**
1. Read `brands.json`.
2. For any brand already in the library, don't re-research its full background — search only for what's new *since* its `last_checked` date (e.g. `"<brand> news since <date>"`), and read its existing `profile` and `key_facts` for context instead of rebuilding them.
3. For brands not yet in the library (the open scan turns these up), do the full research and add a new entry.

**After the run, update `brands.json`:**
- Bump `last_checked` to today for every brand touched this run — even ones with no news, so the next run knows they were checked and doesn't waste a search re-confirming silence.
- Append any new dated fact to that brand's `key_facts` (don't rewrite `profile` wholesale — it's a slow-changing summary; `key_facts` is the running log).
- Add a new entry for every newly discovered brand, with `status: "discovered"`. Anchor brands (from the brief) keep `status: "anchor"`.

This is the mechanism for "always research more, but remember what we find" — the anchor list never shrinks, and the discovered list only grows.

---

## Verification & Cost Discipline

- Before treating any fact as "this week's news," confirm its publish date — a search-engine summary alone is not enough. If a direct fetch to confirm the date fails (paywall, 403), label the item `background`/`date unconfirmed` rather than dropping it silently or guessing.
- Check `state.json` (in the project root) before including a source; skip anything already reported. Update `state.json` with this run's URLs before finishing.
- Read the most recent 1–2 files in `archive/` for continuity before starting.
- It's fine — expected, even — to come in under 10 Section 1 headlines or report "no news" in 1a if that's genuinely what this week has. Don't manufacture filler to hit a quota.

## Persisting the run

This project lives in a git repo specifically so state carries over between runs (especially cloud/scheduled runs, which get a fresh checkout each time). **After finishing the archive file, `state.json`, and `brands.json` updates, and publishing the Artifact:**

```
git add archive/ state.json brands.json opinion_leaders.json
git commit -m "Weekly brief: <date>"
git push
```

If `git push` fails (e.g. no configured remote credentials in this environment), say so explicitly in your final summary rather than silently dropping the changes — persistence for next week depends on this step succeeding.
