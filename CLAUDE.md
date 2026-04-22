# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What This Repository Is

**Ulysses** is a prompt engineering repository for an AI tactical trading assistant. The assistant adopts the persona of **Ulysses S. Grant** (Union commanding general) and guides a NQ futures trader using military-terrain metaphors mapped to market microstructure.

There are no build systems, tests, or code in this repo. All work is authoring and refining the AI system prompt and its operational playbook.

## Repository Structure

| File | Purpose |
|------|---------|
| `Instructions.md` | The concise system prompt — loaded into the AI as its identity and operating rules |
| `Tactical_Companion_Playbook.md` | The full operational playbook — defines every framework, pattern, and format the AI references |
| `*.pdf` | Quick-reference cheat sheets for specific order flow patterns (visual aids for the trader) |
| `drafts/` | Working directory for draft versions of prompts and playbook sections |

## Core Concepts You Must Understand

**Terrain Model** — The foundational metaphor. Price moves through zones:
- **Acceptance Zones** (HVN — high volume, equilibrium)
- **Void Zones** (LVN — thin volume, fast travel)
- **Acceptance Borders** — the LVN/MGI transitions between zones; the only valid entry points

**Structural Hierarchy** (macro overrides micro, always):
1. HTF MGI levels (Weekly/Monthly VWAPs, major composites) — campaign borders
2. Rip (Rolling Pivot) + Session VWAPs — intraday directional bias
3. Leg VWAP — micro-timing only, never used for targets/stops/borders

**MGI (Market Generated Information)** — Named price levels derived from prior sessions (PDH/PDL, RVAH/RVAL, ONH/ONL, IBH/IBL, VWAPs, etc.). The glossaries for Daily/Weekly/Monthly MGIs live in the playbook.

**Color convention** — ALWAYS blue = buying, red = selling. Never bid/ask.

**CSV Output Format** — The AI generates terrain maps as CSV for charting. Critical rules:
- Must span full range: Stratosphere (top HTF resistance) → Abyss (bottom HTF support)
- Zones use colors blue/red/green/pink/purple assigned strictly top-to-bottom
- Key levels (lines) always use yellow
- Row N bottom price must equal Row N+1 top price (no gaps)

**Morning Brief structure** — 5-section format: Terrain Table → CSV Export → Tactical Overview → Strategic Alignment (Primary/Secondary objectives with Entry A/B, stops, targets, tables) → Intelligence Notes

## How the Files Relate

`Instructions.md` is the **short system prompt** — it sets persona, critical overrides, user profile, and chart analysis sequence. It explicitly defers to the playbook for all technical detail.

`Tactical_Companion_Playbook.md` is the **full specification** — when the Instructions say "see playbook," this is the source of truth. Changes to doctrine, new patterns, new MGI definitions, or updated output formats belong here.

## Authoring Conventions

- Keep `Instructions.md` short and high-impact — it's the first thing the AI reads and sets the operating frame
- The playbook is organized into major sections; add new patterns to the **Pattern Recognition Library**, new MGI definitions to the appropriate **MGI Glossary**, new output formats to **Daily Operational Sequence**
- Use checkbox lists (`- [ ]`) for validation checklists and decision trees
- Military metaphors are load-bearing — preserve the terrain/campaign/general framing throughout
- The trader has ADHD: when editing guidance, keep key-area callouts to 1-2 items, avoid cognitive overload
