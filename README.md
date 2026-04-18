# SRKey — Systematic Review Search Strategy Generator

> A free, browser-based tool that generates PICOT-based search strategies for systematic reviews using Claude AI — no API key or installation required.

---

## Version

**v1.3.0** — April 2026

---

## Features

### PICOT Framework
Generates structured search terms across all five PICOT elements:

| Element | Description |
|---------|-------------|
| **P** | Population |
| **I** | Intervention |
| **C** | Comparator |
| **O** | Outcome |
| **T** | Time frame & Study type |

### Search Term Types
Choose how search terms are generated:
- **MeSH + Title/Abstract** — standard NLM MeSH headings combined with free-text keywords, synonyms, and abbreviations
- **MeSH terms only** — controlled vocabulary terms
- **Title/Abstract only** — free-text keywords, synonyms, and brand names

### Multi-Database Support
Generate ready-to-use queries for one or more databases in a single run:

| Database | Query Syntax |
|----------|-------------|
| PubMed | `[MeSH Terms]`, `[tiab]` |
| Embase | `/exp`, `:ti,ab` |
| Cochrane CENTRAL | MeSH + free-text |
| Scopus | `TITLE-ABS-KEY()` |
| Web of Science | `TS=()` |

### Study Type Filters (T in PICOT)
Restrict results by study design — select one or more:
- Randomised Controlled Trials (RCTs)
- Observational studies (cohort, case-control, cross-sectional)
- Systematic reviews / Meta-analyses
- All study types (no filter)

### Date Range
- Default: inception to today (no restriction)
- Optional date picker to restrict by publication date
- Date filter syntax applied automatically per database

### Export to Word
Downloads a formatted `.docx` file containing:
- Study metadata (objective, date, term type, study type, date range)
- PICOT framework table with MeSH and/or TIAB terms
- Full search query table for all selected databases

### Privacy & Cost
- **100% free** — no API key needed
- Works entirely in the browser — no data sent to any server
- Uses [Claude.ai](https://claude.ai) free tier as the AI backend

---

## How to Use

SRKey uses a **copy-paste workflow** with Claude.ai. Follow these four steps:

### Step 1 — Fill in your study details

1. Open the app in your browser
2. Enter your **study title or research objective** in the text box
   - Example: *"Effectiveness of cytisine versus varenicline for smoking cessation in adults"*
3. Select your **study type** (RCT, Observational, Systematic review, or All)
4. Optionally enable a **date range** using the date picker
5. Select one or more **databases** (PubMed, Embase, Cochrane, Scopus, Web of Science)
6. Choose your **search term type** (MeSH + TIAB, MeSH only, or TIAB only)

### Step 2 — Generate and copy the prompt

1. Click **"Build prompt for Claude.ai"**
2. A structured prompt will appear — click **"Copy prompt"**
3. Click **"Open Claude.ai ↗"** to open Claude.ai in a new tab
4. Paste the prompt into Claude.ai and press Enter

### Step 3 — Paste Claude's response back

1. Wait for Claude to generate the JSON response
2. Select and **copy the entire response** (from `{` to `}`)
3. Return to SRKey
4. Paste the JSON into the **"Paste Claude's JSON response"** box
5. Click **"Render results"**

### Step 4 — Use your search strategy

- View the **PICOT table** with all search terms displayed as chips
- Browse **individual database queries** — each has a **Copy** button
- Click **"Copy all queries"** to copy all databases at once
- Click **"Export to Word"** to download a formatted `.docx` file

---

## Tips for Best Results

- **Be specific** in your study objective — include population, intervention, and comparator where possible
- **Review and refine** generated MeSH terms before use; Claude may occasionally suggest non-standard headings
- For PubMed, verify MeSH terms at [MeSH Browser](https://meshb.nlm.nih.gov/)
- Always **validate your final search strategy** with a medical librarian before conducting the review
- The generated queries are a starting point — additional terms may need to be added based on your review protocol

---

## Changelog

### v1.3.0 — April 2026
- Upgraded PICO to **PICOT** framework (added Time / Study type element)
- Added **study type filters**: RCT, Observational, Systematic review, All
- Added **date range picker** with per-database date filter syntax
- Multi-database display: all selected databases now rendered simultaneously

### v1.2.0
- Added **Export to Word** (.docx) with formatted PICO table and query table
- Improved Word document layout with study metadata header

### v1.1.0
- Added multi-database selection (PubMed, Embase, Cochrane, Scopus, Web of Science)
- Added copy per-database and copy-all functionality
- Improved prompt engineering for professional-grade queries

### v1.0.0
- Initial release
- PICO framework with MeSH and Title/Abstract term generation
- Single-file HTML application, no installation required

---

## Tech Stack

- **Frontend**: Vanilla HTML / CSS / JavaScript (single file, no framework)
- **AI backend**: [Claude.ai](https://claude.ai) (free tier, manual copy-paste workflow)
- **Word export**: [docx.js](https://docx.js.org/) v8.5.0 (browser-side generation)
- **Fonts**: DM Serif Display, DM Mono, Outfit (Google Fonts)
- **Hosting**: GitHub Pages

---

## Disclaimer

SRKey is intended as a research aid for health sciences students and researchers. Generated search strategies are AI-assisted starting points and **must be reviewed and validated by a qualified medical librarian** before use in a systematic review. MeSH terms and database syntax should be verified against current database documentation.

---

## License

MIT License — free to use, share, and modify with attribution.
