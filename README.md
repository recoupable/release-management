# Recoup Release Management Skill

An LLM skill for managing music release campaigns using RELEASE.md documents as the single source of truth.

## What It Does

- **Creates** RELEASE.md documents for new releases
- **Updates** existing release documents as information becomes available
- **Generates** deliverables (DSP pitches, press one-sheets, production specs)
- **Infers** which artist and release you're discussing from context

## Folder Structure

The skill expects releases organized by artist:

```
[Label Name]/
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

The LLM will:
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

| # | Section |
|---|---------|
| 1 | Project Snapshot |
| 2 | Release Identifiers & Metadata |
| 3 | Narrative & Positioning |
| 4 | Artist Background |
| 5 | Audience & Market Data |
| 6 | DSP & Streaming Strategy |
| 7 | Marketing Strategy |
| 8 | Social & Digital Marketing |
| 9 | PR & Media Relations |
| 10 | Visual & Creative Assets |
| 11 | Physical Production |
| 12 | Merch |
| 13 | Experiential & OOH |
| 14 | Touring & Live |
| 15 | Team Contacts |
| 16 | Budget Overview |
| 17 | Performance Tracking |
| 18 | Links & Resources Hub |
