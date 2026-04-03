# Explainable Vision Transformer-Based Framework for Pancreatic Tumor Classification in CT Images

[cite_start]This repository contains the official implementation of the 3D Swin Transformer-based framework for detecting pancreatic tumors from volumetric CT scans[cite: 1, 8]. [cite_start]The project integrates Explainable AI (XAI) to provide clinical transparency alongside high-performance diagnostic accuracy[cite: 26, 31].

## 📌 Project Overview
[cite_start]Pancreatic cancer often presents with subtle visual differences and complex anatomy, making early detection challenging[cite: 7]. Our framework addresses these hurdles by:
* [cite_start]**Hierarchical Attention**: Utilizing 3D Swin Transformers to capture both local spatial features and long-range dependencies[cite: 11, 27].
* [cite_start]**Explainability**: Implementing 3D Grad-CAM to highlight diagnostically relevant regions, aiding clinician trust[cite: 28, 29].
* [cite_start]**High Accuracy**: Achieving superior performance compared to traditional CNN-based "black-box" systems[cite: 10, 25].

## 📊 Dataset Specifications
[cite_start]The model is trained and validated using the **Medical Segmentation Decathlon (MSD) Task 07 Pancreas** dataset[cite: 61, 78].
* [cite_start]**Source**: Portal venous phase CT scans with expert-refined annotations[cite: 61].
* [cite_start]**Total Slices**: 26,719[cite: 71].
* [cite_start]**Tumor Slices**: 2,537 (used for training, validation, and testing)[cite: 71].
* [cite_start]**Non-Tumor Slices**: 24,182[cite: 71].
* [cite_start]**Preprocessing**: All volumes resampled to $1 \times 1 \times 1 mm^{3}$ resolution and intensity normalized between 0 and 1[cite: 89].

## ⚙️ Model Architecture
[cite_start]The 3D Swin Transformer processes input volumes as non-overlapping 3D patches[cite: 105].
1. [cite_start]**Patch Partitioning**: Input is divided into $P^3$ sized patches[cite: 105].
2. [cite_start]**Linear Embedding**: Patches are flattened and projected into a $C$-dimensional space[cite: 106].
3. [cite_start]**SW-MSA**: Shifted Window Multi-head Self-Attention allows for cross-window connections[cite: 107].
4. [cite_start]**Hierarchical Stages**: Successive stages reduce resolution while increasing feature depth[cite: 126].

## 📈 Performance Results
[cite_start]Our framework outperforms several recent state-of-the-art models on the MSD benchmark[cite: 117, 137].

| Model | Accuracy (%) | AUC | Precision (%) | F1 (%) |
| :--- | :--- | :--- | :--- | :--- |
| **3D Swin Transformer** | **93.0** | **0.9733** | **93.0** | **93.0** |
| 3D V-Net | 86.0 | 0.9000 | 88.0 | 86.0 |
| MobileNet-V2 | 78.0 | 0.7798 | 91.0 | 82.0 |
| EfficientNet-B0 | 72.0 | 0.7700 | 73.0 | 72.0 |
| 3D U-Net | 54.0 | 0.9277 | 76.0 | 42.0 |

[cite_start]*(Data derived from experimental results [cite: 120])*

## 🔍 Explainability (XAI)
[cite_start]The framework uses **Grad-CAM** to generate class activation maps[cite: 166].
* [cite_start]**Red Regions**: Indicate high model attention corresponding to tumor areas[cite: 167].
* [cite_start]**Blue Regions**: Correspond to healthy pancreatic tissue[cite: 167].
* [cite_start]**Clinical Value**: Visualizations verify that the model's focus aligns with actual medical anatomy[cite: 165].

## 🛠️ Installation & Usage
* [cite_start]**Implementation**: TensorFlow/Keras[cite: 91].
* [cite_start]**Hardware**: Optimized for Kaggle GPU environments[cite: 91].
* [cite_start]**Optimizer**: Adam with an initial learning rate of $1 \times 10^{-4}$[cite: 94].

## 📝 Authors
* [cite_start]**Pranta Das**, **Eva Palit**, **Antu Chowdhury**[cite: 2].
* [cite_start]**Affiliation**: Department of Computer Science and Engineering, East Delta University, Bangladesh[cite: 2, 3].
