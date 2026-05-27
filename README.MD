# EV Bleeding Prediction in HCC using Target-Lesion Radiomics

This repository contains the Python scripts and Jupyter Notebooks used for the original research manuscript: **"Machine Learning of CT Radiomics to Identify High-Risk Esophageal Varices in HCC Patients"**.

## Overview
Esophageal variceal (EV) bleeding is a lethal complication in patients with hepatocellular carcinoma (HCC). This project provides a machine learning pipeline that extracts target-lesion 3D radiomic features directly from esophageal varices on contrast-enhanced CT scans. By integrating these features with clinical parameters (e.g., Portal Vein Thrombosis), the model stratifies bleeding risk non-invasively.

## Repository Structure
- `code_for_submit.ipynb`: The main Jupyter Notebook containing the full pipeline:
  - Phase 1: High-dimensional radiomics extraction using `PyRadiomics`.
  - Phase 2: Feature selection (LASSO) and integrated model training with nested cross-validation.
  - Phase 3: External test set evaluation (AUC, Sensitivity, Specificity, Brier Score).
  - Phase 4: Model interpretability using SHAP (SHapley Additive exPlanations).

## Dependencies
To reproduce the environment, ensure you have the following packages installed:
- `python >= 3.8`
- `pandas`, `numpy`, `scipy`
- `scikit-learn`
- `SimpleITK`
- `pyradiomics`
- `shap`
- `matplotlib`, `seaborn`

## Usage
Due to patient privacy and institutional data protection regulations, the raw clinical data and CT DICOM/NIfTI files cannot be publicly shared. The provided scripts are intended to demonstrate the methodological framework and allow other researchers to replicate the pipeline using their own institutional datasets.

1. Ensure your CT imaging data is preprocessed and masks (liver, spleen, esophagus, varix) are in NIfTI format.
2. Update the `BASE_DIR` paths in the notebook to point to your local data structure.
3. Run the cells sequentially to perform extraction, training, and evaluation.

## License
This project is licensed under the MIT License - see the LICENSE file for details.