# SRKey — Systematic Review Search Strategy Generator

> **Generate professional, database-ready search strategies for systematic reviews — free, no API key required.**

[![Version](https://img.shields.io/badge/version-2.0.0-blue.svg)](https://chayutthaphong.github.io/srkey/)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![Live Demo](https://img.shields.io/badge/demo-live-brightgreen.svg)](https://chayutthaphong.github.io/srkey/)

**🔗 Live App:** [https://chayutthaphong.github.io/srkey/](https://chayutthaphong.github.io/srkey/)

---

## What is SRKey?

SRKey is a free, browser-based tool that helps researchers build comprehensive PICOTS-based search strategies for systematic reviews. It generates structured prompts for [Claude.ai](https://claude.ai), then renders the JSON response into export-ready Word documents — no account, no API key, no server required.

---

## Features

- **PICOTS framework** — structured input for Population, Intervention, Comparator, Outcome, Timeframe, Setting, and NOT (exclusions)
- **Multi-database support** — PubMed, Embase, Cochrane, Scopus, Web of Science, Google Scholar
- **MeSH + Title/Abstract queries** — broadest coverage with controlled vocabulary and free-text variants
- **Flexible search depth** — Comprehensive (full synonyms, truncation, MeSH explosion) or Quick (core terms only)
- **Multiple query modes** — Combined query per database, or per PICOTS element + combined
- **Word export (.docx)** — A4-formatted strategy document and blank search log template
- **100% client-side** — no data leaves your browser; powered by Claude.ai via copy-paste
- **Free to use** — no API key, no registration required

---

## How It Works

```
[You] → Fill in PICOTS + options → Copy generated prompt
         ↓
[Claude.ai] → Paste prompt → Run → Copy JSON response
         ↓
[SRKey] → Paste JSON → Render results → Export to Word
```

### Step-by-step

1. **Enter your research objective** — be specific about population, intervention, and comparator
2. **Optionally fill in PICOTS** — specify P, I, C, O, T, S terms manually, or let AI infer from the title
3. **Select study design & date range** — RCT, Observational, Systematic reviews, or All
4. **Choose databases** — minimum recommended: PubMed + Embase + Cochrane
5. **Set term type, query mode & search depth** — MeSH + TIAB is recommended for systematic reviews
6. **Build prompt → paste into Claude.ai** — click "Build prompt", open [claude.ai](https://claude.ai), paste and run
7. **Paste JSON back → render** — copy Claude's full JSON response and paste into SRKey
8. **Export to Word** — download the strategy document and/or search log template

---

## PICOTS Framework

| Letter | Meaning | Example |
|--------|---------|---------|
| **P** | Population | Adults with type 2 diabetes |
| **I** | Intervention | SGLT-2 inhibitors (dapagliflozin, empagliflozin) |
| **C** | Comparator | Placebo or standard care (metformin) |
| **O** | Outcome | HbA1c reduction, cardiovascular events |
| **T** | Timeframe | ≥6 months follow-up, published 2000–present |
| **S** | Setting | Primary care, hospital, community, LMIC |
| **NOT** | Exclusions | Animal studies, in vitro, case reports |

---

## Database Coverage

| Database | Strength | Syntax | Access |
|----------|----------|--------|--------|
| PubMed | Biomedical, free, comprehensive | `[MeSH Terms]`, `[tiab]` | Free |
| Embase | Pharmacology, European journals, Emtree | `/exp`, `:ti,ab` | Subscription |
| Cochrane | Clinical trials, SR/meta-analysis | MeSH + free-text | Free/Subscription |
| Scopus | Broad multidisciplinary | `TITLE-ABS-KEY()` | Subscription |
| Web of Science | Citation tracking, high-impact journals | `TS=()` | Subscription |
| Google Scholar | Grey literature, theses | Free-text only | Free |

---

## ⚠️ Important Disclaimer

All generated search strategies **must be reviewed and validated by a qualified medical librarian** before use in a systematic review. AI-generated queries are a starting point — they may miss database-specific syntax nuances, require additional subject-specific terms, or need adjustment based on your review protocol.

---

## Tech Stack

- **Vanilla HTML/CSS/JavaScript** — no framework, no build step
- **[Claude.ai](https://claude.ai)** — AI-powered search term generation (via copy-paste workflow)
- **[docx.js](https://docx.js.org)** — client-side Word document generation
- **MIT License**

---

## Key References

### Reporting Standards
- Page MJ, et al. *The PRISMA 2020 statement.* BMJ. 2021;372:n71. [doi:10.1136/bmj.n71](https://doi.org/10.1136/bmj.n71)
- Moher D, et al. *The PRISMA statement.* PLoS Med. 2009;6(7):e1000097. [doi:10.1371/journal.pmed.1000097](https://doi.org/10.1371/journal.pmed.1000097)

### Cochrane Methodology
- Higgins JPT, et al. *Cochrane Handbook for Systematic Reviews v6.4.* 2023. [training.cochrane.org/handbook](https://training.cochrane.org/handbook)
- Lefebvre C, et al. *Chapter 4: Searching for and selecting studies.* Cochrane Handbook v6.4.

### Search Peer Review
- McGowan J, et al. *PRESS 2015 guideline statement.* J Clin Epidemiol. 2016;75:40-46.

### Useful Tools
- [NLM MeSH Browser](https://meshb.nlm.nih.gov/) — verify MeSH terms
- [PRISMA website](https://www.prisma-statement.org/) — checklists and flow diagrams

---

## Changelog

### v2.0.0 — April 2026
- Complete UI/UX redesign — professional light theme, cleaner layout
- Added optional PICOTS specification (Cards 1–2) with NOT field for exclusions
- Added **Author & Journal** and **No term generation** search term types
- Added **Google Scholar** as a database option
- Search log: numbering resets per database
- Removed on-screen log table — export directly to Word
- Improved A4-format Word exports with professional layout
- Added **Search logic explanation** section in results
- Prominent validation warning banner throughout

### v1.4.0 — April 2026
- Query mode (Combined / Per PICOTS), search log export, database direct links

### v1.3.0 — April 2026
- PICOTS framework, study type filters, date range picker

### v1.0–1.2 — January–March 2026
- Initial release, multi-database support, Word export

---

## License

MIT License

---

*SRKey — Making systematic review search strategies accessible to every researcher.*
