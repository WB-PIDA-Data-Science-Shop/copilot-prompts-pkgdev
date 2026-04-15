---
output: "rmarkdown::html_vignette"
title: CPIA Data Processing and Scoring Methodology
vignette: |
  \%`\VignetteIndexEntry{CPIA Methodology}`{=tex}
  %`\VignetteEngine{rmarkdown}`{=tex} %`\VignetteEncoding{UTF-8}`{=tex}
---

# Prompt: Generate World Bank Methodology Note Vignette for cpiaetl

## Objective

Generate a professional, World Bank--quality methodology note as an R
package vignette for the `cpiaetl` package.

The output should:

-   Be written for World Bank staff (technical and non-technical)
-   Balance policy clarity with technical rigor
-   Emphasize transparency, reproducibility, and institutional
    reliability
-   Be suitable for internal circulation and potential formal review
-   Be structured as a long-form vignette
    (`vignette("cpiaetl-methodology")`)
-   Use professional, neutral institutional tone
-   Avoid marketing language
-   Avoid unnecessary academic jargon
-   Include reproducible R code blocks where appropriate

------------------------------------------------------------------------

## Context

Package: `cpiaetl`\
Purpose: Standardized ETL and scoring pipeline for CPIA governance
indicators\
Audience: World Bank governance specialists, economists, data
scientists, TTLs, OPCS reviewers\
Use Case: Institutional standardization of CPIA data processing and
scoring

The note should describe both:

1.  The CPIA data transformation and scoring methodology
2.  The engineering architecture that ensures reproducibility and
    quality control

------------------------------------------------------------------------

# Required Structure

Follow this structure exactly.

------------------------------------------------------------------------

# 1. Executive Summary

Write 1--2 pages in plain language.

Explain:

-   What CPIA is (briefly)
-   What problem this package addresses
-   Why standardization of CPIA data processing matters
-   What guarantees this workflow provides
-   What it does NOT do
-   Why this strengthens institutional reliability

No formulas in this section.

------------------------------------------------------------------------

# 2. Background and Motivation

Explain:

-   Historical CPIA data processing challenges
-   Risks of manual workflows
-   Inconsistencies across years or teams
-   Reproducibility gaps
-   Auditability concerns

Position cpiaetl as a structured response to these issues.

------------------------------------------------------------------------

# 3. Conceptual Framework for CPIA Processing

## 3.1 Data Sources

Describe:

-   Raw CPIA inputs
-   Scoring templates
-   Historical score structures
-   Metadata

## 3.2 Indicator Structure

Explain:

-   Criteria and subcomponents
-   Scoring scales
-   Aggregation logic
-   Weighting structure (if applicable)

Include light LaTeX formulas only if helpful and readable.

## 3.3 Data Transformation Logic

Explain clearly:

-   Data cleaning rules
-   Validation checks
-   Handling of missing values
-   Outlier handling
-   Rounding conventions
-   Internal consistency checks

Focus on clarity.

------------------------------------------------------------------------

# 4. Scoring and Aggregation Methodology

Describe:

-   Score calculation logic
-   Weighting rules
-   Aggregation process
-   Final CPIA index derivation (if applicable)

If formulas are included:

-   Use simple LaTeX
-   Define each term clearly
-   Avoid unnecessary statistical symbolism

------------------------------------------------------------------------

# 5. Data Engineering Architecture (cpiaetl Implementation)

Include a simple ASCII diagram:

Raw Inputs ↓ Validation Layer ↓ Transformation Layer ↓ Scoring Engine ↓
Final CPIA Dataset

Explain:

-   Separation of concerns
-   Deterministic outputs
-   Modularity
-   Test coverage
-   Version control integration
-   CI/CD validation

------------------------------------------------------------------------

# 6. Reproducibility and Quality Assurance

Explain:

-   Automated unit tests
-   Continuous integration checks
-   Deterministic transformations
-   Version control traceability
-   Audit trail capacity
-   Error handling safeguards

------------------------------------------------------------------------

# 7. Assumptions and Limitations

Be explicit:

-   Assumes valid raw inputs
-   Does not alter official CPIA methodology
-   Does not replace expert judgment
-   Sensitive to input completeness
-   Not a causal inference tool

Maintain institutional neutrality.

------------------------------------------------------------------------

# 8. Practical Implementation Guide

Provide reproducible code examples:

``` r
library(cpiaetl)

clean_data <- cpia_clean(raw_data)
scores <- cpia_score(clean_data)
```

Explain:

-   Required input structure
-   Expected data format
-   Output structure
-   Typical workflow

Keep example concise and runnable.

------------------------------------------------------------------------

# 9. Operational Use in World Bank Context

Explain:

-   How teams should integrate this pipeline
-   Relationship to dashboards (e.g., cpiaapp)
-   Cross-year comparability implications
-   Governance review process integration
-   Institutional strengthening impact

------------------------------------------------------------------------

# 10. Frequently Asked Questions

Include at least five realistic questions such as:

-   What happens if data are missing?
-   Can scores be overridden?
-   Does this change historical CPIA methodology?
-   How are updates versioned?
-   What if criteria definitions change?

Provide clear, policy-consistent answers.

------------------------------------------------------------------------

# 11. Appendix (Optional but Recommended)

Include:

-   Variable schema
-   Full formula definitions
-   Version history structure
-   Validation rule examples

------------------------------------------------------------------------

# Style Requirements

-   Professional institutional tone
-   No emojis
-   No marketing language
-   Clear section headings
-   Scannable structure
-   Markdown compatible
-   R code blocks fenced with `r`
-   Light LaTeX only where useful
-   Avoid overly academic writing style

------------------------------------------------------------------------

# Output Format

Generate full vignette markdown file with YAML header:

Ensure it is ready to be placed inside:

vignettes/cpiaetl-methodology.Rmd

------------------------------------------------------------------------

# Validation Checklist

-   Clear executive summary
-   Logical flow
-   No unexplained formulas
-   Code examples minimal and coherent
-   Institutional neutrality maintained
-   Suitable for formal review
-   Balanced for technical and non-technical readers
