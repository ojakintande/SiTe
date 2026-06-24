# SiTe: Statistical Significance Explanations

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Status: Under Review (NeurIPS 2026)](https://img.shields.io/badge/Status-NeurIPS%202026%20Submission-blue)](https://github.com/ojakintande/LLM_Who_Audit_Reviewers)

This repository contains the implementation of **SiTe (Statistical Significance Explanations)**, a framework that bridges Explainable AI (XAI) with inferential statistics to provide trustworthy, significance-aware feature importance.

---

## 1. Abstract
While SHapley Additive exPlanations (SHAP) is a cornerstone of model interpretability, it lacks measures of statistical significance, often leading to unstable or overconfident interpretations. **SiTe** addresses this by augmenting SHAP with a rank-based hypothesis test and the False Feature Identification Rate (FAIR) via the Benjamini-Hochberg procedure. By assigning p-values to feature importance directly, SiTe quantifies whether a feature’s contribution is statistically distinguishable from noise without the computational overhead of traditional resampling methods.

## 2. Key Contributions
*   **Significance-Aware Interpretability:** Assigns formal p-values to feature contributions, moving beyond raw importance scores[cite: 1].
*   **Statistical Rigor:** Implements the Benjamini-Hochberg procedure to control the **False Feature Identification Rate (FAIR)**[cite: 1].
*   **Computational Efficiency:** Achieves significance quantification without intensive resampling[cite: 1].
*   **Superior Stability:** Experiments demonstrate substantial improvements over baseline SHAP, including up to 247% improvement in FAIR and enhanced ranking stability (up to 0.92)[cite: 1].

## 3. Empirical Validation
SiTe has been validated across diverse modalities[cite: 1]:
*   **Synthetic Benchmarks:** Demonstrating clear separation between signal and noise[cite: 1].
*   **Computer Vision (MNIST):** Maintaining near-perfect FAIR (1.00) in digit classification tasks[cite: 1].
*   **Real-world datasets:** Bridging the gap between empirical feature importance and inferential trust[cite: 1].

## 4. Repository Structure
*   `/scripts`: Core SiTe engine, including hypothesis testing and FAIR calculation modules[cite: 1].
*   `/data`: Datasets used for the NeurIPS 2026 evaluation[cite: 1].
*   `/notebooks`: Reproducible examples demonstrating SiTe compared to standard SHAP[cite: 1].

## 5. Quick Start
To integrate SiTe into your own interpretability pipeline[cite: 1]:

1.  **Environment:** Ensure R (v4.x) is installed[cite: 1].
2.  **Dependencies:** Install necessary statistical libraries[cite: 1]:
```r
    install.packages(c("tidyverse", "SHAPforxgboost", "stats"))
    ```
3.  **Audit:** Run the SiTe significance test[cite: 1]:
```r
    source("scripts/site_engine.R")
    site_results <- calculate_site_significance(model, data, alpha = 0.05)
    ```
#
## 6. Citation
This work is currently under review for **NeurIPS 2026**[cite: 1]. Please cite as:
> [Awaiting official proceedings information]

## 7. License
This project is licensed under the **MIT License**[cite: 1].
