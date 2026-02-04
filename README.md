# Release Management Skill

A Claude skill for managing music release campaigns using RELEASE.md documents as the single source of truth.

## What It Does

- **Creates** RELEASE.md documents for new releases
- **Updates** existing release documents as information becomes available
- **Generates** deliverables (DSP pitches, press one-sheets, production specs)
- **Infers** which artist and release you're discussing from context

## Folder Structure

The skill expects releases organized by artist:

```
[Org Root]/
└── [Artist Name]/
    └── Releases/
        └── [Release Name]/
            └── RELEASE.md
```

## Usage

Just mention a release naturally:

> "What's the status on Drake's new album?"

> "The UPC for Mac's single 'Sunrise' is 123456789012"

> "Generate a DSP pitch for Taylor's Midnights"

> "Let's start planning the new Wiz Khalifa project"

Claude will:
1. Infer the artist and release from your message
2. Find or create the RELEASE.md
3. Read, update, or generate outputs as needed

## Files

| File | Purpose |
|------|---------|
| `SKILL.md` | Core skill instructions |
| `references/release-template.md` | Blank template for new releases |
| `references/deliverables.md` | Output formats (DSP pitch, press one-sheet, etc.) |
| `references/section-guide.md` | Field-by-field guidance for each section |

## RELEASE.md Sections

| # | Section | Sharing |
|---|---------|---------|
| 1 | Project Snapshot | SHAREABLE |
| 2 | Release Identifiers & Metadata | OPS |
| 3 | Narrative & Positioning | SHAREABLE |
| 4 | Artist Background | SHAREABLE |
| 5 | Audience & Market Data | SHAREABLE |
| 6 | DSP & Streaming Strategy | SHAREABLE |
| 7 | Marketing Strategy | INTERNAL |
| 8 | Social & Digital Marketing | INTERNAL |
| 9 | PR & Media Relations | SHAREABLE |
| 10 | Visual & Creative Assets | SHAREABLE |
| 11 | Physical Production | OPS/INTERNAL |
| 12 | Merch | INTERNAL |
| 13 | Experiential & OOH | INTERNAL |
| 14 | Touring & Live | SHAREABLE |
| 15 | Team Contacts | INTERNAL |
| 16 | Budget Overview | INTERNAL |
| 17 | Performance Tracking | INTERNAL |
| 18 | Links & Resources Hub | — |

## Sharing Tags

- `[INTERNAL]` — Scrub before sharing externally
- `[SHAREABLE]` — Safe for DSPs, press, management, partners
- `[OPS]` — Operations/production team reference
