# Insider Threat Detection in Active Directory Environments
### Using Unsupervised Machine Learning on the CERT r4.2 Dataset

**Author:** Yug Mukesh Patel
**Affiliation:** M.S. Cyber Security, Technology, and Policy — The University of Texas at Dallas
**Status:** 🚧 Work in progress — research paper in preparation, target submission Q3 2026

---

## Overview

This repository contains the code, experiments, and reproducibility artifacts for a research project on detecting malicious insider activity in enterprise Active Directory environments. The project uses the publicly available **CERT Insider Threat Test Dataset (release r4.2)** from Carnegie Mellon University and benchmarks unsupervised anomaly detection models against rule-based and supervised baselines.

## Research Question

> Can lightweight unsupervised machine learning models detect insider threat behaviors in Active Directory logs with detection performance comparable to supervised methods, without requiring labeled attack data?

## Why This Matters

Insider threats account for a significant portion of enterprise data breaches and are notoriously difficult to detect because the malicious actor uses legitimate credentials. Supervised detection methods require labeled examples of insider attacks — which most organizations do not have. This project explores whether unsupervised approaches can fill that gap.

## Dataset

- **Name:** CERT Insider Threat Test Dataset r4.2
- **Source:** Carnegie Mellon University — Software Engineering Institute
- **Link:** https://kilthub.cmu.edu/articles/dataset/Insider_Threat_Test_Dataset/12841247
- **Note:** Dataset is not redistributed in this repo due to size. See `data/README.md` for download instructions.

## Methods (Planned)

- Feature engineering from logon, device, file, email, and HTTP activity logs
- Baseline 1: Rule-based detection (Sigma-style rules ported to Python)
- Baseline 2: Supervised — Random Forest, XGBoost
- Proposed: Unsupervised — Isolation Forest, One-Class SVM, Autoencoder
- Evaluation: Precision, Recall, F1, ROC-AUC, false-positive rate

## Repository Structure
.
├── data/              # Dataset placeholder + download instructions (data NOT committed)
├── notebooks/         # Jupyter notebooks for exploration and experiments
├── src/               # Reusable Python source code
├── results/           # Output figures, tables, model metrics
├── paper/             # LaTeX source of the paper (Overleaf-synced)
└── README.md          # This file
## Reproducibility

All experiments will be reproducible from the code in this repo using the dependencies listed in `requirements.txt`. Random seeds are fixed across all experiments.

## License

Code: MIT License. Dataset usage subject to CMU's redistribution terms.

## Acknowledgments

This work is conducted as part of the M.S. Cybersecurity, Technology, and Policy program at UT Dallas. Faculty advisor: *to be added.*

## Contact

Yug Mukesh Patel — yug3009p@gmail.com
LinkedIn: https://www.linkedin.com/in/yugpatel9409