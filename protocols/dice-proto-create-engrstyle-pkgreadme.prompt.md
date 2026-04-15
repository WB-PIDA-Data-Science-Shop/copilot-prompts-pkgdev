# Prompt: Generate Engineering-Grade README for R Package

## Objective

Create a professional, production-quality README.md aligned with modern
software engineering standards for R package development.

The README must:

-   Clearly communicate value proposition
-   Follow industry-standard open-source conventions
-   Support CI/CD workflows
-   Reflect reproducibility and testing standards
-   Scale for production and collaborative environments

This README should be suitable for: - CRAN-ready packages -
Enterprise/internal R packages - Research-grade reproducible packages -
Shiny application packages deployed in production

------------------------------------------------------------------------

# Context Inputs

Provide the following before generating the README:

-   Package Name:
-   Package Type: (Analysis / Data / Utility / Shiny / Infrastructure /
    API Client)
-   Target Audience: (Developers / Analysts / Researchers / End Users /
    Enterprise Teams)
-   Lifecycle Stage: (Experimental / Active Development / Stable /
    Production)
-   Primary Value Proposition:
-   Core Features: (3--7 bullet points)
-   Test Coverage %:
-   CI Provider: (GitHub Actions / GitLab CI / None)
-   License:
-   Maintainer / Organization:

------------------------------------------------------------------------

# Required README Structure

## 1. Header & Status Badges

Include: - CI badge - Coverage badge - Lifecycle badge - License badge -
One-sentence value proposition - Optional logo or architecture diagram

No marketing language.

------------------------------------------------------------------------

## 2. Overview

Explain: - Problem being solved - Why it exists - Who benefits -
Appropriate use cases

Concise and technical.

------------------------------------------------------------------------

## 3. Installation

Must support:

``` r
# CRAN (if applicable)
install.packages("package")

# Development version
remotes::install_github("org/package")

library(package)
```

List any required system dependencies.

------------------------------------------------------------------------

## 4. Quick Example

Provide a minimal runnable example (\<20 lines):

``` r
library(package)
result <- primary_function(data)
print(result)
```

For Shiny packages:

``` r
package::run_app()
```

------------------------------------------------------------------------

## 5. Core Features

Structured bullet format:

-   Feature --- short technical description
-   Feature --- architectural or performance benefit
-   Feature --- integration capability

Include measurable indicators when possible.

------------------------------------------------------------------------

## 6. Architecture (If Applicable)

User API Layer ↓ Service / Logic Layer ↓ Data / Infrastructure Layer

Explain: - Separation of concerns - Modularity - Test isolation -
Extensibility model

------------------------------------------------------------------------

## 7. Testing & Quality Assurance

Include:

-   Number of unit tests
-   Test coverage percentage
-   CI provider
-   devtools::check() status

Commands:

``` r
devtools::test()
devtools::check()
covr::report()
```

------------------------------------------------------------------------

## 8. Documentation

-   Function documentation via ?function_name
-   Vignettes via browseVignettes("package")
-   Wiki link: ../../wiki
-   pkgdown site if applicable

------------------------------------------------------------------------

## 9. Development Workflow

``` r
renv::restore()
devtools::test()
devtools::check()
styler::style_pkg()
lintr::lint_package()
```

Describe branching strategy if relevant.

------------------------------------------------------------------------

## 10. Dependency Management

List:

Core dependencies Development dependencies Minimum R version

State if renv is used.

------------------------------------------------------------------------

## 11. Performance & Reproducibility (If Relevant)

Include: - Benchmarks - Deterministic outputs - Parallelization - Memory
considerations

------------------------------------------------------------------------

## 12. Deployment (Shiny Only)

``` r
rsconnect::deployApp()
```

Or containerized deployment if applicable.

------------------------------------------------------------------------

## 13. Roadmap (Optional)

-   Planned features
-   Refactors
-   CRAN submission goals

------------------------------------------------------------------------

## 14. Contributing

1.  Fork repository
2.  Create feature branch
3.  Write tests
4.  Ensure devtools::check() passes
5.  Submit PR

Link to ../../wiki/Development-Workflow

------------------------------------------------------------------------

## 15. License & Maintainer

Specify license type and maintainer details.

------------------------------------------------------------------------

# Engineering Validation Checklist

-   Clear value proposition in first 5 lines
-   Reproducible example
-   Accurate CI badge
-   Valid coverage badge
-   No placeholder text
-   Professional tone
-   Suitable for CRAN or enterprise audit

------------------------------------------------------------------------

# Style Requirements

-   Professional tone
-   No unnecessary verbosity
-   No emojis unless explicitly user-facing Shiny
-   Markdown compliant
-   GitHub-renderable
-   Fenced code blocks with `r`
