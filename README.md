# LLM Leaderboard Robustness Audit — Supplementary Materials

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

## Paper

**A Reproducible Robustness Audit Framework for Human-Preference Leaderboards in Large Language Models**

Redhwan Nour — Department of Computer Science, Taibah University, Medina 42353, Saudi Arabia

*Submitted to: Computers, Materials & Continua (CMC), Special Issue: Large Language Models: Evaluation, Knowledge Integration, and Applications*

---

## Repository Contents

### Supplementary Tables (Word Document)

| File | Description |
|---|---|
| [`Supplementary_Tables.docx`](Supplementary_Tables.docx) | All 7 supplementary data tables in formatted Word format |

### Data Tables (CSV)

| File | Rows | Description |
|---|---|---|
| [`TableS1_global_leaderboard.csv`](TableS1_global_leaderboard.csv) | 20 | Full global leaderboard — Bradley–Terry scores and bootstrap uncertainty statistics |
| [`TableS2_subgroup_divergence.csv`](TableS2_subgroup_divergence.csv) | 16 | Full subgroup divergence results (all 16 subgroup leaderboards) |
| [`TableS3_ipw_results.csv`](TableS3_ipw_results.csv) | 5 | Full IPW exposure-sensitivity coefficients (all 5 focal subgroups) |
| [`TableS4_uncertainty_summary.csv`](TableS4_uncertainty_summary.csv) | 20 | Full bootstrap rank uncertainty summaries with non-separability flags |
| [`TableS5_stability_metrics.csv`](TableS5_stability_metrics.csv) | 20 | Full Rank Stability Score (RSS) and multivariate validation metrics |
| [`TableS6_temporal_results.csv`](TableS6_temporal_results.csv) | 7 | Full temporal robustness statistics (shared-model scope) |
| [`TableS7_model_classification.csv`](TableS7_model_classification.csv) | 20 | Integrated model classification (all 20 models) |

### Supplementary Figure

| File | Description |
|---|---|
| [`FigS1_permutation_results.png`](FigS1_permutation_results.png) | Fig. S1 — Permutation-based subgroup significance summary |

---

## Dataset

The raw pairwise comparison data used in this study is the publicly available LMSYS Chatbot Arena dataset:

> Chiang et al. (2024). Chatbot Arena: An Open Platform for Evaluating LLMs by Human Preference. *NeurIPS 2024*.
> Available at: https://huggingface.co/datasets/lmsys/chatbot_arena_conversations

**Important:** The specific numerical model rankings reported in the paper reflect a historical snapshot (April–June 2023) and should not be interpreted as current model standings.

---

## Audit Pipeline

The manuscript describes a 13-step reproducible audit pipeline:

1. Data loading and validation
2. Tie separation (decisive vs. tied comparisons)
3. Subgroup annotation
4. Global Bradley–Terry leaderboard estimation
5. Subgroup-specific leaderboard estimation (×16 slices)
6. Permutation significance testing (FDR-corrected)
7. Bootstrap rank uncertainty (1,000 resamples)
8. Inverse-propensity weighting (IPW) exposure audit
9. Bootstrap rank interval and non-separability analysis
10. Rank Stability Score (RSS) computation
11. Multivariate convergent validity (Mahalanobis/Euclidean)
12. Temporal robustness analysis (early/late split)
13. Result-family synthesis and model classification

---

## Citation

If you use these materials, please cite:

```bibtex
@article{nour2026leaderboard,
  title   = {A Reproducible Robustness Audit Framework for Human-Preference Leaderboards in Large Language Models},
  author  = {Nour, Redhwan},
  journal = {Computers, Materials \& Continua},
  year    = {2026},
  note    = {Submitted}
}
```

---

## License

This repository is licensed under the [MIT License](LICENSE).
The LMSYS Chatbot Arena dataset is subject to its own terms of use.
