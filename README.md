# Multilingual Harmful-Content Dataset (Arabic–English)

A merged, deduplicated harmful/offensive-content corpus combining eight existing hate-speech and offensive-language resources, built for Arabic–English harmful-content classification. Constructed as part of the thesis *Sarcasm-Aware Multilingual Harmful Content Detection: A Controlled Evaluation of Integration Mechanisms Using LLMs* (ESTIN, 2025/2026).

## Composition by Source

| Source | Language | Rows (raw) | Rows (cleaned) |
|---|---|---:|---:|
| ArCyC | Arabic | 4,475 | 4,475 |
| L-HSAB | Arabic | 5,744 | 5,740 |
| T-HSAB | Arabic | 5,964 | 5,946 |
| OffensEval2020-Arabic | Arabic | 7,815 | 7,809 |
| Let-Mi | Arabic | 5,229 | 5,229 |
| HateXplain | English | 20,061 | 20,061 |
| CAD | English | 22,986 | 22,770 |
| HatEval | English | 12,730 | 12,675 |
| **Total** | | **85,004** | **84,705** |

CAD is the single largest source, ~27% of the pooled corpus. HatEval's row count already excludes ~6,599 Spanish-language rows removed from the original bilingual release (out of scope for this Arabic–English framing).

## Composition by Split

| Split | Rows | Non-harmful | Harmful | English | Arabic |
|---|---:|---:|---:|---:|---:|
| Train | 67,764 | 62.65% | 37.35% | 65.53% | 34.47% |
| Validation | 8,470 | 62.66% | 37.34% | 65.53% | 34.47% |
| Test | 8,471 | 62.65% | 37.35% | 65.53% | 34.47% |

Overall: **37.35% harmful**, **65.53% English / 34.47% Arabic**.

## Notes

- Preprocessing: cross-source deduplication, followed by Arabic-specific normalization and a stratified train/val/test split.
- Each source dataset retains its own license and citation requirements — cite the original papers for ArCyC, L-HSAB, T-HSAB, OffensEval2020-Arabic, Let-Mi, HateXplain, CAD, and HatEval individually alongside this repository.

## Citation

If you use this merged dataset, please cite the thesis/paper this pipeline was built for, plus the eight original source papers.
