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

If you use this merged dataset, please cite the paper it was built for, plus the eight original source papers below.

**ArCyC [39]**
Shannag, F.; Hammo, B.H.; Faris, H.: The design, construction and evaluation of annotated Arabic cyberbullying corpus. Educ. Inf. Technol. 27, 10977–11023 (2022). https://doi.org/10.1007/s10639-022-11056-x

**L-HSAB [40]**
Mulki, H.; Haddad, H.; Bechikh Ali, C.; Alshabani, H.: L-HSAB: a Levantine Twitter dataset for hate speech and abusive language. In: Proceedings of the Third Workshop on Abusive Language Online, pp. 111–118 (2019)

**T-HSAB [41]**
Haddad, H.; Mulki, H.; Oueslati, A.: T-HSAB: a Tunisian hate speech and abusive dataset. In: Arabic Language Processing: From Theory to Practice (ICALP 2019), pp. 251–263. Springer (2019)

**OffensEval2020-Arabic [42]**
Mubarak, H.; Darwish, K.; Magdy, W.; Elsayed, T.; Al-Khalifa, H.: Overview of OSACT4 Arabic offensive language detection shared task. In: Proceedings of the 4th Workshop on Open-Source Arabic Corpora and Processing Tools, with a Shared Task on Offensive Language Detection, pp. 48–52 (2020)

**Let-Mi [43]**
Mulki, H.; Ghanem, B.: Let-Mi: an Arabic Levantine Twitter dataset for misogynistic language. In: Proceedings of the Sixth Arabic Natural Language Processing Workshop, pp. 154–163 (2021)

**HateXplain [44]**
Mathew, B.; Saha, P.; Yimam, S.M.; Biemann, C.; Goyal, P.; Mukherjee, A.: HateXplain: a benchmark dataset for explainable hate speech detection. In: Proceedings of the AAAI Conference on Artificial Intelligence, vol. 35, pp. 14867–14875 (2021)

**CAD [45]**
Vidgen, B.; Nguyen, D.; Margetts, H.; Rossini, P.; Tromble, R.: Introducing CAD: the contextual abuse dataset. In: Proceedings of the 2021 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies, pp. 2289–2303 (2021)

**HatEval [46]**
Basile, V.; Bosco, C.; Fersini, E.; Nozza, D.; Patti, V.; Rangel Pardo, F.M.; Rosso, P.; Sanguinetti, M.: SemEval-2019 Task 5: multilingual detection of hate speech against immigrants and women in Twitter. In: Proceedings of the 13th International Workshop on Semantic Evaluation, pp. 54–63 (2019)

<details>
<summary>BibTeX</summary>

```bibtex
@article{shannaq-etal-2022-arcyc,
    title = "The design, construction and evaluation of annotated {A}rabic cyberbullying corpus",
    author = "Shannaq, Fatima and Hammo, Bassam H. and Faris, Hossam",
    journal = "Education and Information Technologies",
    volume = "27",
    pages = "10977--11023",
    year = "2022",
    doi = "10.1007/s10639-022-11056-x"
}

@inproceedings{mulki-etal-2019-l-hsab,
    title = "{L}-{HSAB}: A {L}evantine {T}witter Dataset for Hate Speech and Abusive Language",
    author = "Mulki, Hala and Haddad, Hatem and Bechikh Ali, Chedi and Alshabani, Halima",
    booktitle = "Proceedings of the Third Workshop on Abusive Language Online",
    year = "2019",
    address = "Florence, Italy",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/W19-3512/",
    doi = "10.18653/v1/W19-3512",
    pages = "111--118"
}

@inproceedings{haddad-etal-2019-t-hsab,
    title = "{T}-{HSAB}: A {T}unisian Hate Speech and Abusive Dataset",
    author = "Haddad, Hatem and Mulki, Hala and Oueslati, Asma",
    booktitle = "Arabic Language Processing: From Theory to Practice (ICALP 2019)",
    year = "2019",
    publisher = "Springer",
    pages = "251--263",
    doi = "10.1007/978-3-030-32959-4_18"
}

@inproceedings{mubarak-etal-2020-overview,
    title = "Overview of {OSACT}4 {A}rabic Offensive Language Detection Shared Task",
    author = "Mubarak, Hamdy and Darwish, Kareem and Magdy, Walid and Elsayed, Tamer and Al-Khalifa, Hend",
    booktitle = "Proceedings of the 4th Workshop on Open-Source Arabic Corpora and Processing Tools, with a Shared Task on Offensive Language Detection",
    year = "2020",
    address = "Marseille, France",
    publisher = "European Language Resource Association",
    url = "https://aclanthology.org/2020.osact-1.7/",
    pages = "48--52"
}

@inproceedings{mulki-ghanem-2021-let-mi,
    title = "{L}et-{M}i: An {A}rabic {L}evantine {T}witter Dataset for Misogynistic Language",
    author = "Mulki, Hala and Ghanem, Bilal",
    booktitle = "Proceedings of the Sixth Arabic Natural Language Processing Workshop",
    year = "2021",
    address = "Kyiv, Ukraine (Virtual)",
    publisher = "Association for Computational Linguistics",
    pages = "154--163"
}

@inproceedings{mathew-etal-2021-hatexplain,
    title = "{H}ate{X}plain: A Benchmark Dataset for Explainable Hate Speech Detection",
    author = "Mathew, Binny and Saha, Punyajoy and Yimam, Seid Muhie and Biemann, Chris and Goyal, Pawan and Mukherjee, Animesh",
    booktitle = "Proceedings of the AAAI Conference on Artificial Intelligence",
    volume = "35",
    year = "2021",
    pages = "14867--14875",
    doi = "10.1609/aaai.v35i17.17745"
}

@inproceedings{vidgen-etal-2021-introducing,
    title = "Introducing {CAD}: the Contextual Abuse Dataset",
    author = "Vidgen, Bertie and Nguyen, Dong and Margetts, Helen and Rossini, Patricia and Tromble, Rebekah",
    booktitle = "Proceedings of the 2021 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies",
    year = "2021",
    address = "Online",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2021.naacl-main.182/",
    doi = "10.18653/v1/2021.naacl-main.182",
    pages = "2289--2303"
}

@inproceedings{basile-etal-2019-semeval,
    title = "{S}em{E}val-2019 Task 5: Multilingual Detection of Hate Speech Against Immigrants and Women in {T}witter",
    author = "Basile, Valerio and Bosco, Cristina and Fersini, Elisabetta and Nozza, Debora and Patti, Viviana and Rangel Pardo, Francisco Manuel and Rosso, Paolo and Sanguinetti, Manuela",
    booktitle = "Proceedings of the 13th International Workshop on Semantic Evaluation",
    year = "2019",
    address = "Minneapolis, Minnesota, USA",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/S19-2007/",
    doi = "10.18653/v1/S19-2007",
    pages = "54--63"
}
```
</details>
