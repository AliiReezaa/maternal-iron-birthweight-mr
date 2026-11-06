<p align="center"><img src="assets/header.svg" width="100%" alt="Maternal iron status and birth weight"></p>

<p align="center">![Co-author](https://img.shields.io/badge/Co--author-0f6e6a?style=flat-square) ![CAUSE](https://img.shields.io/badge/CAUSE-5b4bb7?style=flat-square) ![MRlap](https://img.shields.io/badge/MRlap-5b4bb7?style=flat-square) ![Colocalisation](https://img.shields.io/badge/Colocalisation-0f6e6a?style=flat-square) ![R](https://img.shields.io/badge/R-276DC3?style=flat-square)</p>

> **Status:** manuscript in preparation
>
> This repository is a public overview of an unpublished study. It shows the research question, design and methods. **Results, data and analysis code are withheld until peer-reviewed publication**, and will be released here at that point.

## Research question
Does genetically predicted **maternal** iron status (serum iron, ferritin, transferrin saturation, TIBC) influence offspring birth weight, independent of the fetal genome?

## Study design
```mermaid
flowchart LR
  G[Iron-status variants<br/>TMPRSS6 · HFE · TF ...] --> X[Maternal iron biomarkers]
  X --> Y[Offspring birth weight<br/>maternal-effect GWAS, EGG]
  X --> T{Triangulation}
  T --> T1[Replication GWAS]
  T --> T2[Positive & negative controls]
  T --> T3[CAUSE · MRlap]
  T --> T4[MVMR · MR-Clust]
  T --> T5[Colocalisation]
  style X fill:#ede9fb,stroke:#5b4bb7
```

## Data sources
| Role | Dataset | Notes |
|---|---|---|
| Exposures | Moksnes et al. 2022 iron biomarkers | four traits |
| Outcome | EGG consortium maternal-adjusted birth weight (Warrington 2019) | N≈297k |
| Controls | type 2 diabetes (positive); hair colour, CAD (negative) | assumption checks |

## Methods
| Component | Approach |
|---|---|
| Core MR | IVW, MR-Egger, weighted median/mode, MR-RAPS, contamination mixture |
| Outliers | MR-PRESSO and radial MR |
| Bias checks | MRlap (sample overlap), CAUSE (correlated pleiotropy), LDSC via GenomicSEM |
| Mechanism | MVMR with inflammatory markers; MR-Clust; colocalisation at TMPRSS6/HFE/TF |

## Why it matters
Iron supplementation in pregnancy is routine worldwide. Genetic evidence on whether iron status itself affects fetal growth can guide supplementation policy.

## Team & role
Co-author **A. R. Soleymani Taloubaghi** (analysis) with collaborators at Tehran University of Medical Sciences.

## Reproducibility
- Analysis pipeline written in R (renv-locked; TwoSampleMR, MendelianRandomization, CAUSE, MRlap, coloc), with pinned package versions and a single entry-point script
- Public summary statistics only; no individual-level data is used or shared
- Reported according to STROBE-MR

---
<sub>Contact: <a href="mailto:alirezasoleymani24@gmail.com">alirezasoleymani24@gmail.com</a> · <a href="https://aliireezaa.github.io">aliireezaa.github.io</a></sub>
