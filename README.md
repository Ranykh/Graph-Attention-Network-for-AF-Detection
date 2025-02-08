

# Graph Attention Networks for Atrial Fibrillation Detection

This repository hosts the resources for the project **"Graph Attention Networks for Atrial Fibrillation Detection."** This project leverages advanced Graph Neural Network architectures to analyze 12-lead ECG data, focusing on inter-lead spatial dependencies and geographic variations to enhance arrhythmia detection, specifically atrial fibrillation.

---

## Overview

Atrial fibrillation (AF) is the most prevalent cardiac arrhythmia and a leading cause of stroke and heart failure worldwide. Early and accurate detection is critical for effective treatment and improving patient outcomes. This project explores the use of Graph Attention Networks (GATs) to model inter-lead dependencies in ECG data and addresses geographic variations in signal characteristics.

### Key Contributions:
1. Development of a 5-layer GAT model with multi-head attention for robust ECG analysis.
2. Integration of Weighted Mutual Information (WMI) for graph construction.
3. Region-specific adaptation techniques for improved cross-region generalization.
4. Comprehensive statistical and visual validation using t-SNE and other methods.

---


## Features

- **Preprocessing:** Signal filtering, feature extraction (statistical and clinical), and graph representation of ECG data.
- **Graph Neural Networks:** Implementation of GATs with multi-head attention for dynamic inter-lead dependency modeling.
- **Region-Specific Analysis:** Techniques for addressing geographic variability in ECG datasets.
- **Validation Methods:** Cross-region validation, statistical testing, and dimensionality reduction using t-SNE.

n
# Citation
If you use this repository in your work, please cite:
Khirbawi, R. (2024). Graph Attention Networks for Atrial Fibrillation Detection: Leveraging Inter-Lead Dependencies and Geographic Variations in ECG Signals.
