

# Graph Attention Networks for Atrial Fibrillation Detection

This repository hosts the resources for the project **"Graph Attention Networks for Atrial Fibrillation Detection."** This project leverages advanced Graph Neural Network architectures to analyze 12-lead ECG data, focusing on inter-lead spatial dependencies and geographic variations to enhance arrhythmia detection, specifically atrial fibrillation.

---

# Graph Attention Networks for Atrial Fibrillation Detection in ECG Signals


##  Overview

Atrial fibrillation (AF) is the most common cardiac arrhythmia and a leading cause of stroke and heart failure worldwide. In this project, we propose a deep learning framework that leverages **Graph Attention Networks (GATs)** to detect AF from 12-lead Electrocardiogram (ECG) recordings. Unlike traditional models, our method captures **inter-lead spatial dependencies** and **geographic variations**, significantly improving the model’s diagnostic capabilities.

This project was conducted using datasets from three geographically distinct populations (China, Germany, and the US) and integrates advanced statistical methods and visualizations to analyze cross-regional generalization.

---

## Deep Learning & GATs: A Brief Introduction

Traditional deep learning models like CNNs and RNNs perform well on grid-structured or sequential data. However, they struggle to capture **complex interdependencies** between signals from different ECG leads.

**Graph Neural Networks (GNNs)** address this limitation by treating ECG leads as nodes in a graph and modeling their relationships as weighted edges. Specifically:

- **Graph Convolutional Networks (GCNs)** aggregate information from neighboring nodes but treat all connections equally.
- **Graph Attention Networks (GATs)** extend this by assigning **dynamic importance (attention weights)** to each connection using multi-head attention, allowing the model to **prioritize diagnostically relevant lead relationships**.

---

##  Key Features

- **Accuracy**: 94.8%
- **Recall**: 88.57%
- **ROC-AUC**: 97.28%
- **Region-aware modeling**: Adjusts for geographic biases in ECG datasets using region-specific weights.
- **Feature Engineering**: Combines statistical (mean, variance, skewness) and clinical (QRS duration, P-wave amplitude) features per lead.
- **WMI Graphs**: Graph edges are created using **Weighted Mutual Information (WMI)** to capture non-linear inter-lead dependencies.



## Features

- **Preprocessing:** Signal filtering, feature extraction (statistical and clinical), and graph representation of ECG data.
- **Graph Neural Networks:** Implementation of GATs with multi-head attention for dynamic inter-lead dependency modeling.
- **Region-Specific Analysis:** Techniques for addressing geographic variability in ECG datasets.
- **Validation Methods:** Cross-region validation, statistical testing, and dimensionality reduction using t-SNE.


## Datasets

This study uses public ECG datasets:

- **Chapman-Shaoxing** 🇨🇳 (China) - 5000
- **PTB-XL** 🇩🇪 (Germany) - 5000
- **Georgia 12-Lead** 🇺🇸 (USA) - 5000

Each contains 12-lead ECG recordings labeled for arrhythmias, particularly AF. We analyzed cross-region generalization using both baseline and region-weighted models.

---

## Evaluation Metrics

| Model         | Accuracy | Recall | ROC-AUC |
|---------------|----------|--------|---------|
| Random Forest | 87.6%    | 6.3%   | 71.2%   |
| GAT (5L-4H)   | 94.8%    | 88.6%  | 97.3%   |

**Cross-region tests** showed significant accuracy drops, which were mitigated using region-specific weighting strategies.

---

## 📈 Visual Insights

- **t-SNE Plots**: Visualized embeddings showed distinct clusters per region.
- **Confusion Matrix**: High precision and recall for both AF and normal classes.
- **Heatmaps**: Revealed degradation in model performance across regions and improvements after applying regional weights.




## Citation
If you use this repository in your work, please cite:
Khirbawi, R. (2024). Graph Attention Networks for Atrial Fibrillation Detection: Leveraging Inter-Lead Dependencies and Geographic Variations in ECG Signals.
