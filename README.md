# ALWM

Official repository for **Anatomy-Aware Longitudinal World Modeling for Context-Conditioned Disease Progression in Longitudinal Chest X-Rays**.

> **Release status:** The repository homepage is available. Training and evaluation code is being organized for public release.

## Overview

ALWM is a representation-learning framework for longitudinal chest X-rays that connects controlled geometric supervision with clinical-context predictive learning.

- **Geometry-Consistent Anatomical Modeling (GCAM)** learns cross-view structural relationships from CT-derived digitally reconstructed radiographs (DRRs).
- **Context-Conditioned Latent Dynamics (CCLD)** learns longitudinal representations conditioned on recorded clinical events and examination intervals.
- **Anatomy-Guided Temporal Interaction (AGTI)** connects the two branches through contrastive modulation and spatial response alignment.

The current evaluation covers retrospective disease-progression identification between observed examinations and ICU outcome prediction. The model is not presented as a causal treatment simulator or as a validated prospective radiographic forecasting system.

## Evaluation tasks

1. **Disease progression identification**  
   Classification of improvement, stability, and worsening for seven thoracic findings using three consecutive observed CXR studies.

2. **ICU outcome prediction**  
   In-hospital mortality and four-class ICU length-of-stay prediction using information available within the first 48 hours of an ICU stay.

## Data

The experiments use credentialed or separately distributed datasets:

- [MIMIC-CXR](https://physionet.org/content/mimic-cxr/)
- [MIMIC-CXR-JPG](https://physionet.org/content/mimic-cxr-jpg/)
- [MIMIC-IV](https://physionet.org/content/mimiciv/)
- [Chest ImaGenome](https://physionet.org/content/chest-imagenome/)
- [LIDC-IDRI](https://www.cancerimagingarchive.net/collection/lidc-idri/)

No source images, clinical records, or patient-level data are redistributed in this repository. Users must obtain the datasets from their official providers and comply with the corresponding data-use agreements.

## Planned repository structure

```text
ALWM/
├── configs/          # Experiment configurations
├── data/             # Cohort construction and preprocessing scripts
├── models/           # GCAM, CCLD, AGTI, and downstream heads
├── scripts/          # Training and evaluation entry points
├── tools/            # DRR generation and analysis utilities
└── README.md
```

## Reproducibility

The public release will document:

- patient-level partitioning and three-study window construction;
- disease-label mapping and validity masks;
- the 48-hour ICU observation protocol;
- model training, checkpoint selection, and five-seed evaluation;
- controlled comparisons and ablation configurations.

## Installation and usage

Environment files, preprocessing commands, training scripts, and evaluation examples will be added with the code release.

## Citation

Citation information will be added after the manuscript receives a stable public identifier.

## License

The source-code license will be specified when the implementation is released. Dataset licenses and data-use agreements remain governed by the original data providers.
