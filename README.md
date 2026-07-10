# SGLT2 Inhibitors vs. Placebo for Heart Failure Hospitalization in Type 2 Diabetes with Established ASCVD

A reproducible meta-analysis of randomized controlled trials, built in R with the `meta` package and reported with Quarto. The systematic search and screening were conducted independently.

## Summary

This project synthesizes randomized evidence on SGLT2 inhibitors versus placebo for **hospitalization for heart failure** in adults with type 2 diabetes and established atherosclerotic cardiovascular disease (ASCVD) — a population central to coverage and value decisions for these high-cost agents. Pooling 4 cardiovascular outcome trials using a random-effects model, SGLT2 inhibitors were associated with a **pooled hazard ratio of 0.70 (95% CI 0.62–0.78)** — an approximately 30% relative reduction in HF hospitalization — with no detectable heterogeneity (I² = 0%).

## Methods

- **Search:** PubMed (RCT filter, 2013–present), 250 records, conducted independently
- **Screening:** two-stage (title/abstract, then full text) in Rayyan; secondary analyses and substudies excluded so each trial is represented by a single primary results paper
- **Population scope:** established ASCVD only; renal-entry (CREDENCE, SCORED, DAPA-CKD) and heart-failure-entry (DAPA-HF, EMPEROR) trials excluded to keep the population coherent
- **Included trials:** EMPA-REG OUTCOME, CANVAS Program, DECLARE-TIMI 58, VERTIS-CV
- **Effect measure:** hazard ratios pooled on the log scale (inverse-variance, random effects); HRs chosen because these are time-to-event trials with differing follow-up and per-arm event counts were not uniformly reported
- **Cross-validation:** the pooled estimate was independently reproduced using `metafor` (`rma()`/`escalc()`), confirming the result (HR 0.70, 95% CI 0.62–0.78) against a second implementation
- **Reporting:** fully reproducible Quarto document — every figure and statistic computed from code

## Files

- `sglt2_meta_report.qmd` — Quarto source (the reproducible analysis)
- `sglt2_meta_report.html` — rendered report

## Limitations

Four trials (each large, but a modest number); two enrolled mixed primary/secondary-prevention populations; HF hospitalization was a secondary outcome in most trials; effect estimates extracted as reported hazard ratios rather than from individual patient data.

## Tools

R · `meta` · `tidyverse` · Quarto · Rayyan · PubMed

---
*Author: Said Adjao. Analysis built from published trial data only.*
