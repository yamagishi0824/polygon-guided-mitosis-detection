# Glioma-MDC 2025 Challenge Solution
Polygon-Guided Extraction with ConvNeXt-based Classification Models

This repository contains the official implementation for the ISBI 2025 challenge submission:

**Cell Image Classification with Polygon-Guided Extraction for Glioma Mitosis Detection**  
Yosuke Yamagishi, Shouhei Hanaoka  
2025 IEEE 22nd International Symposium on Biomedical Imaging (ISBI)

Paper: https://ieeexplore.ieee.org/abstract/document/10980953/

---

## Overview

This work addresses mitotic cell classification in glioma histopathology under one-shot and few-shot settings.  
We adopt a polygon-guided cell extraction strategy and train ConvNeXt-based models for classification.

The pipeline is implemented using Kaggle notebooks:

| Stage | Description | Notebook |
|-------|-------------|----------|
| Preprocessing | Polygon-based cell extraction and dataset construction | https://www.kaggle.com/code/yosukeyama/data-preprocessing-tr-122824 |
| Training | ConvNeXt-base training on the training set | https://www.kaggle.com/code/yosukeyama/glioma-mdc2025-convnext-base-tr-128/notebook |
| Inference | One-shot inference for challenge submission | https://www.kaggle.com/code/yosukeyama/glioma-mdc2025-one-shot-infer |

---

## Repository Structure

```
.
├── notebooks/
│ ├── 0_preprocess.ipynb # Kaggle Preprocessing Notebook
│ ├── 1_train.ipynb # Kaggle Training Notebook
│ └── 2_infer.ipynb # Kaggle Inference Notebook
└── README.md

````

Dataset is not included in this repository.  
Please follow the official ISBI Glioma-MDC dataset access instructions.

---

## Method in Brief

- Polygon-guided patch extraction from WSIs
- ConvNeXt Base pretrained on ImageNet
- Strong data augmentation
- One-shot classification using similarity-based inference
- Test-time augmentation for robustness

---

## How to Reproduce

1. Obtain the dataset from the official Glioma-MDC challenge site.
2. Run the preprocessing notebook to generate cropped-cell datasets.
3. Run the training notebook (optional if retraining is required).
4. Run the inference notebook for prediction on the test set.

---

## Citation

Please cite the following paper if you use this code:

```bibtex
@inproceedings{yamagishi2025cell,
  title={Cell Image Classification with Polygon-Guided Extraction for Glioma Mitosis Detection},
  author={Yamagishi, Yosuke and Hanaoka, Shouhei},
  booktitle={2025 IEEE 22nd International Symposium on Biomedical Imaging (ISBI)},
  pages={1--5},
  year={2025},
  organization={IEEE}
}
```

