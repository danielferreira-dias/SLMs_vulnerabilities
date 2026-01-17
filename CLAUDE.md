# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a **Systematic Literature Review** about **Vulnerabilities of Small Language Models**. The final document will be written in LaTeX using a two-column academic template format.

## Document Format

- **Type**: Systematic Literature Review (SLR)
- **Format**: LaTeX, two-column layout
- **Citation Style**: BibTeX references
- **Structure**: IMRAD-inspired with standard SLR sections (Introduction, Methodology, Results, Discussion, Conclusions)

## Available Skills

This project uses three Claude Code skills located in `.claude/`:

### `/literature-review`
Conduct systematic literature reviews using multiple databases (PubMed, arXiv, bioRxiv, Semantic Scholar). Use for:
- Multi-database systematic search
- PRISMA-compliant methodology
- Thematic synthesis of findings
- PDF generation from markdown

### `/citation-management`
Manage citations and references. Use for:
- Converting DOIs to BibTeX entries
- Searching Google Scholar and PubMed
- Validating citation accuracy
- Formatting and cleaning BibTeX files

### `/scientific-writing`
Write scientific manuscripts in flowing prose. Use for:
- IMRAD structure guidance
- Citation style formatting (APA, Nature, Vancouver)
- Section-specific writing guidance
- Converting outlines to full paragraphs

## Key Scripts

Located in `.claude/literature-review/scripts/` and `.claude/citation-management/scripts/`:

```bash
# Verify DOIs and generate citation report
python .claude/literature-review/scripts/verify_citations.py <markdown_file>

# Generate PDF from markdown (requires pandoc + xelatex)
python .claude/literature-review/scripts/generate_pdf.py <markdown_file> \
  --citation-style apa \
  --output output.pdf

# Check PDF generation dependencies
python .claude/literature-review/scripts/generate_pdf.py --check-deps

# Convert DOI to BibTeX
python .claude/citation-management/scripts/doi_to_bibtex.py <doi>

# Format and clean BibTeX file
python .claude/citation-management/scripts/format_bibtex.py references.bib \
  --deduplicate \
  --sort year \
  --output clean_references.bib

# Validate BibTeX citations
python .claude/citation-management/scripts/validate_citations.py references.bib
```

## Dependencies

### Python packages
```bash
pip install requests bibtexparser biopython
```

### System tools (for PDF generation)
- **pandoc**: Document converter
- **xelatex**: LaTeX engine (part of TeX distribution)

Windows installation:
- pandoc: Download from https://pandoc.org/installing.html
- xelatex: Install MiKTeX or TeX Live

## Writing Guidelines

1. **Write in full paragraphs** - Never submit bullet points in the final manuscript
2. **Two-stage process**: First create outlines with key points, then convert to flowing prose
3. **Thematic synthesis** - Organize findings by themes, not study-by-study
4. **Verify all citations** - Run `verify_citations.py` before finalizing
5. **Follow PRISMA guidelines** for systematic reviews

## LaTeX Two-Column Template Structure

The document should follow this structure based on the provided template:
- Title, Authors, Affiliations
- Abstract (Context, Goal, Method, Results, Conclusion) + Keywords
- I. Introduction
- II. Theoretical Background
- III. Methodology (search strategy, inclusion/exclusion criteria)
- IV. Results (thematic synthesis)
- V. Discussion
- VI. Conclusions
- References (numbered style)

## BibTeX Entry Format

Use the template at `.claude/citation-management/assets/bibtex_template.bib` for reference. Common entry types:
- `@article{}` for journal papers
- `@inproceedings{}` for conference papers
- `@misc{}` for preprints (bioRxiv, arXiv)

## PRISMA Tracking

**IMPORTANT**: All literature searches must be tracked for PRISMA compliance. Maintain the tracking file at `prisma_tracking.md`.

### PRISMA Flow Stages

Track papers through each stage:

1. **Identification**: Records identified from each database
   - Database name, search query, date, number of results

2. **Screening**: Title/abstract screening
   - Papers excluded with reasons

3. **Eligibility**: Full-text assessment
   - Papers excluded with reasons

4. **Included**: Final papers in the review

### Tracking File Structure (`prisma_tracking.md`)

The tracking file must contain:
- Search queries used per database
- Date of each search
- Number of records per database
- Duplicate removal count
- Screening decisions (included/excluded with reasons)
- Full-text eligibility decisions
- Final included papers list with citation keys

### Update Protocol

When searching for papers:
1. Log the database, query, and date
2. Record total hits
3. After deduplication, update duplicate count
4. During screening, log exclusions with reasons
5. Keep running totals for the PRISMA flow diagram

## Resources

- Review template: `.claude/literature-review/assets/review_template.md`
- BibTeX examples: `.claude/citation-management/assets/bibtex_template.bib`
- Citation styles guide: `.claude/scientific-writing/references/citation_styles.md`
- IMRAD structure: `.claude/scientific-writing/references/imrad_structure.md`
- **PRISMA tracking**: `prisma_tracking.md`
