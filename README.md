# 🫀 CVD Classification on BRFSS – Data Leakage Reanalysis

This repository accompanies the opinion paper:

> **Eltawil, M. (2025). Commentary on “Evaluating Binary Classifiers for Cardiovascular Disease Prediction: Enhancing Early Diagnostic Capabilities.” Journal of Clinical and Diagnostic Data, 2025.**

The work reproduces and re-evaluates the cardiovascular disease (CVD) classification study by Iacobescu *et al.* (2024, *J. Clin. Med.*), demonstrating that the reported near-perfect performance (AUC ≈ 0.99) likely resulted from **data leakage** during preprocessing.

---

## 📊 Objectives

1. Reconstruct the original (leaked) pipeline described in Iacobescu *et al.*  
   → SMOTE–ENN → normalization → train/test split (70 / 30)  
2. Implement a **leak-free** workflow  
   → train/test split first, then resampling & scaling *inside cross-validation folds*  
3. Compare resulting performance metrics and calibration.

---

## 🧪 Repository Structure

