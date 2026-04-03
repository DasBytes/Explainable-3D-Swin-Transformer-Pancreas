# Explainable Vision Transformer for Pancreatic Tumor Classification (CT)

This repository contains the official implementation of a **3D Swin Transformer–based deep learning framework** for detecting pancreatic tumors from volumetric CT scans.  
The framework integrates **Explainable AI (XAI)** to provide clinical transparency alongside high diagnostic performance.

---

# 📌 Project Overview

Pancreatic cancer is difficult to detect early due to subtle visual differences and complex anatomy in CT imaging.  
This project addresses these challenges using a transformer-based medical imaging pipeline.

---

## ⭐ Key Contributions

### 🧠 Hierarchical Attention
3D Swin Transformer captures both **local spatial features** and **long-range dependencies**.

### 🔍 Explainability
- 3D Grad-CAM highlights diagnostically relevant tumor regions  
- Improves clinician trust and interpretability

### 🚀 High Performance
Outperforms traditional CNN-based models for pancreatic tumor classification.

---

# 📊 Dataset

The model is trained and evaluated using:

**Medical Segmentation Decathlon (MSD) – Task 07 Pancreas**

### Dataset Details
- Portal venous phase abdominal CT scans  
- Expert-refined annotations  
- **Total slices:** 26,719  
- **Tumor slices:** 2,537  
- **Non-tumor slices:** 24,182  

### Preprocessing
- Resampled to **1×1×1 mm³**
- Intensity normalized to **[0, 1]**

---

# 🏗️ Model Architecture — 3D Swin Transformer

Pipeline overview:

1. **Patch Partitioning**  
   Volumes are divided into non-overlapping 3D patches.

2. **Linear Embedding**  
   Flattened patches projected into feature space.

3. **Shifted Window Attention (SW-MSA)**  
   Enables cross-window contextual learning.

4. **Hierarchical Representation**  
   Spatial resolution decreases while feature depth increases.

---

# 📈 Performance

The transformer-based approach significantly improves classification performance.

---

# 🔬 Explainable AI (Grad-CAM)

We apply **3D Grad-CAM** to visualize model decision regions.

- 🔴 **Red regions → Tumor-relevant areas**
- 🔵 **Blue regions → Healthy pancreatic tissue**

These visualizations confirm the model focuses on anatomically meaningful regions.

---

# ⚙️ Installation

Clone the repository:

```bash
git clone https://github.com/DasBytes/Explainable-3D-Swin-Transformer-Pancreas.git
cd Explainable-3D-Swin-Transformer-Pancreas
