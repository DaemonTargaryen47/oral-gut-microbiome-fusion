# Oral-Gut Microbiome Fusion

Interpretable ML analysis of paired stool and oral cavity microbiome samples, classifying age-group status (adult vs. newborn) while testing whether multi-site fusion adds real, non-redundant signal, not just accuracy.

## Contents

```
├── oral_gut_microbiome_fusion.ipynb   # Full analysis pipeline (Colab-ready)
├── results/                           # Figures, tables, and robustness check outputs
└── README.md
```

## Data

Public shotgun metagenomic data from Ferretti et al. (2018), accessed via the [`curatedMetagenomicData`](https://bioconductor.org/packages/release/data/experiment/html/curatedMetagenomicData.html) Bioconductor package. No new data collected.

## Methods

CLR-transformed abundance features, evaluated with Logistic Regression, Random Forest, and XGBoost (5-fold CV). Interpretability via SHAP (`TreeExplainer` / `LinearExplainer`), including site-of-origin attribution and per-taxon dependence analysis. Robustness confirmed via null baseline, bootstrap CIs, and preprocessing sensitivity checks.

## Running

Open the notebook in Google Colab and run all cells top to bottom. The R/Bioconductor setup step takes 10-15 minutes on first run. Outputs save to `results/`.

## Authors

Chowdhury Aseer Ruthbah, Talim Hossain Sadi, Nur E Shiratun Jahan, Abu Nayem Md. Tanzim Adib, BRAC University

## License

[MIT](LICENSE). The underlying dataset retains its original licensing terms.

## Contact

Chowdhury Aseer Ruthbah, chowdhury.aseer.ruthbah@g.bracu.ac.bd
