# Everbetter War Room (interim public board)

Living dashboard for Everbetter — AI news intelligence war room.

**DNA:** *good, better, best. Never put to rest, until good is better, and better is best.*

Enforced by **IRRE** (Innovation, Renaissance & Radical Enlightenment). Everything is a launch pad. Founder has no operating role.

## Interim host — GitHub Pages

This repo is an **interim public bridge** so the war room stays live while Everbetter stands up a **company-owned host**.

- Public board (once Pages is enabled): https://etchy.github.io/everbetter-war-room/
- Quiet Ledger: https://etchy.github.io/everbetter-war-room/ledger.html
- Owner today: personal GitHub user `etchy` (not Everbetter org infrastructure)
- Destination later: Everbetter-owned domain/host; this Pages site will be retired or redirected then

Do **not** treat this repo as the long-term production home. It is a temporary public mirror of the board until the company host exists.

Source of truth on disk: `data/board.json` + `data/org.json`. **EXAMPLE DATA is retired** — real cards ship with `example: false` after CIO pressure-test.

Local preview (browsers block `file://` fetch):

```bash
cd war-room
python3 -m http.server 8765
```

Then: http://127.0.0.1:8765/ and http://127.0.0.1:8765/ledger.html

If fetch fails, the page embeds a **cached copy of the last live board** (not EXAMPLE) so the UI still renders.

A root `.nojekyll` file is present so GitHub Pages serves `data/*.json` without Jekyll interference.

## Quiet Ledger (founder directives)

On-demand directive tracker — **not a task list**. Three zooms per directive: **Orbit** (glance) → **Flight Path** (action arc) → **Ground Truth** (plan / thought / deliverables / IRRE·TLC pressure).

- Live: [ledger.html](./ledger.html) (or Quiet Ledger toggle in the War Room top bar)
- Update surface: `data/directives.json`

## Update surface

| File | What to edit |
|------|----------------|
| `data/board.json` | Active stories, polyangles, confidence/blind spots, Process Forge |
| `data/org.json` | Wave 1 roles, DNA motto, Org Pulse |
| `data/freshness.json` | Freshness thresholds |
| `data/directives.json` | Quiet Ledger directives |

1. Write a real card (`example: false`) with CIO+CSO required fields.
2. Save JSON.
3. Refresh the browser.

Required write fields: `claim`, `angles`, `source_classes`, `confidence`, `blind_spot`, `freshness_bucket`, `evidence_links`, `headline`, `link`, `priority`, `displace_what`, `why_in`, `why_out`. Contested: `contested: true` + `contested_legs` (both legs, never averaged). No receipts → no card.

## Files

```
war-room/
├── index.html
├── ledger.html
├── .nojekyll
├── data/*.json
├── data/why/
└── README.md
```

## Wave 1 roles (see `data/org.json`)

CEO (Ceo Of Ai News Analysis), COO, CIO (Intelligence), CPO, CSO, CLO (Learning), TLC Chair (outside War Room), **IRRE Chair** (DNA enforcement).
