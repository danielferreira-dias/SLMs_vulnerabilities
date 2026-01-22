# Results Section Reduction Summary

**Date:** 2026-01-22
**Purpose:** Condense Results section to make room for Discussion and Conclusions (~1.5-2 pages)

---

## Changes Made

### 1. Appendix Removed (~110 lines saved)
- **What:** Complete 65-study characteristics table (Table A.1)
- **Location:** Lines 584-692 (original)
- **Resolution:** Added note in Overview: "Complete characteristics of all 65 included studies are available in supplementary materials."

### 2. Table 3 Removed (~22 lines saved)
- **What:** Study Distribution by Venue Type and Year table
- **Location:** Lines 359-378 (original)
- **Reason:** Redundant with text already stating "78% from 2024-2025" and "58% arXiv preprints"
- **Resolution:** Information retained in prose form

### 3. Quality Assessment Condensed (~15 lines saved)
- **Before:** 3 paragraphs explaining assessment criteria, quality tiers, and synthesis influence
- **After:** 1 paragraph with key numbers only
- **Retained:** Quality tier breakdown (24 high, 32 medium, 9 lower) and weighting note

### 4. Itemized Lists Converted to Prose (~25 lines saved)

#### a) Jailbreak Techniques List
- **Before:** 4 bullet points (template-based, optimization-based, adaptive, distillation)
- **After:** 2 sentences of flowing prose

#### b) Edge Deployment Constraints List
- **Before:** 4 bullet points (physical access, resource limitations, update constraints, isolation)
- **After:** 2 sentences of flowing prose

### 5. RQ1 Vulnerability Subsubsections Consolidated (~30 lines saved)

| Original | New |
|----------|-----|
| Jailbreak Attacks | Prompt-Level Attacks (combined) |
| Prompt Injection | ↑ merged above |
| Backdoor Attacks | Training-Time Attacks (condensed) |
| Adversarial Examples | Adversarial Robustness (condensed) |
| Membership Inference | Privacy Attacks (combined) |
| Model Extraction | ↑ merged above |
| Hardware-Level Attacks | Moved to RQ3 quantization section |

### 6. RQ2-RQ4 Trimmed (~20 lines saved)

| Section | Before | After |
|---------|--------|-------|
| RQ2 (SLM vs LLM) | 4 subsubsections | 2 paragraphs, no headers |
| RQ3 (Architecture) | 4 subsubsections | 3 paragraphs, no headers |
| RQ4 (Mitigations) | 4 subsubsections | 2 paragraphs, no headers |

---

## Total Estimated Savings

| Category | Lines Saved |
|----------|-------------|
| Appendix removal | ~110 |
| Table 3 removal | ~22 |
| Quality Assessment | ~15 |
| Lists to prose | ~25 |
| RQ1 consolidation | ~30 |
| RQ2-RQ4 trimming | ~20 |
| **Total** | **~222 lines** |

---

## New Results Section Structure

```
\section{Results}
  \subsection{Overview of Included Studies}
    - Table 2: Distribution by Category (KEPT)
    - Quality assessment (1 paragraph)
    - Supplementary materials note

  \subsection{Vulnerability Taxonomy (RQ1)}
    \subsubsection{Prompt-Level Attacks}
    \subsubsection{Training-Time Attacks}
    \subsubsection{Adversarial Robustness}
    \subsubsection{Privacy Attacks}

  \subsection{SLM-Specific Vulnerability Patterns (RQ2)}
    - 2 paragraphs (no subsubsection headers)

  \subsection{Architectural Contributing Factors (RQ3)}
    - 3 paragraphs (no subsubsection headers)

  \subsection{Defense Mechanisms (RQ4)}
    - 2 paragraphs (no subsubsection headers)
```

---

## PRISMA Compliance Retained

- PRISMA flow diagram (Figure 1)
- Study selection numbers in text
- Table 2: Distribution by vulnerability category
- Quality assessment summary (condensed)
- All RQ1-RQ4 synthesis findings

---

## Space Now Available

- **Discussion:** ~1.5 pages
  - Key Findings
  - Implications for Practice
  - Limitations
- **Conclusions:** ~0.5 page
  - Summary of contributions
  - Future research directions
