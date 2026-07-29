# Brain-Tumor-Classification-Using-ResNet50-project
Deep Learning-based Multi-Class Brain Tumor Classification using MRI Images with ResNet50 Transfer Learning and Explainable AI
# 🧠 Brain Tumor MRI Classification Using Fine-Tuned ResNet50

> An Explainable Deep Learning Framework for Multi-Class Brain Tumor Classification Using MRI Images

![Python](https://img.shields.io/badge/Python-3.12-blue.svg)
![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange.svg)
![Keras](https://img.shields.io/badge/Keras-Deep%20Learning-red.svg)
![OpenCV](https://img.shields.io/badge/OpenCV-Image%20Processing-green.svg)
![License](https://img.shields.io/badge/License-MIT-blue.svg)

---

# 📌 Overview

Brain tumors are among the most critical neurological diseases, where early and accurate diagnosis plays a significant role in treatment planning.

This project presents an **Explainable Deep Learning framework** for automatic classification of brain MRI images into four categories using a fine-tuned **ResNet50** model enhanced with **Transfer Learning**, **CLAHE preprocessing**, and **Grad-CAM explainability**.

> **Research Purpose Only**
>
> This project is intended for research and educational purposes and should **NOT** be used as a clinical diagnostic tool.

---

# 🎯 Objectives

- Classify brain MRI images into four classes.
- Improve image quality using CLAHE.
- Fine-tune a pretrained ResNet50 network.
- Visualize model attention using Grad-CAM.
- Evaluate the model using comprehensive performance metrics.

---

# 🧠 Classification Classes

- Glioma
- Meningioma
- Pituitary Tumor
- No Tumor

---

# 🚀 Project Pipeline

```
MRI Images
      │
      ▼
CLAHE Enhancement
      │
      ▼
Preprocessing
(Resize + Normalize)
      │
      ▼
Transfer Learning
(Fine-Tuned ResNet50)
      │
      ▼
Classification
(4 Classes)
      │
      ▼
Performance Evaluation
      │
      ▼
Grad-CAM Explainability
```

---

# 🛠 Technologies Used

- Python 3.12
- TensorFlow
- Keras
- OpenCV
- NumPy
- Matplotlib
- Scikit-Learn
- Google Colab

---

# 📂 Dataset

Dataset used:

**Brain Tumor MRI Dataset**

https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset

Dataset classes:

```
Training/
    glioma/
    meningioma/
    pituitary/
    notumor/

Validation/
    ...

Testing/
    ...
```

---

# 🖼 Image Preprocessing

The preprocessing pipeline includes:

- CLAHE (Contrast Limited Adaptive Histogram Equalization)
- Grayscale conversion
- Resize to 224×224
- Normalization
- RGB conversion after CLAHE

This improves local contrast while preserving structural information.

---

# 🧠 Deep Learning Model

Base Model:

- ResNet50 (ImageNet pretrained)

Transfer Learning:

- Frozen early layers
- Fine-tuned Conv4 and Conv5 blocks

Custom Classification Head:

- Global Average Pooling
- Dense (256)
- Batch Normalization
- Dropout (0.2)
- Softmax Output Layer

Optimizer:

- AdamW

Loss Function:

- Categorical Crossentropy

---

# 📈 Data Augmentation

Training augmentation includes:

- Rotation
- Zoom
- Width Shift
- Height Shift
- Brightness Adjustment
- Horizontal Flip

Validation and Test images are only normalized.

---

# 📊 Model Performance

| Metric | Score |
|---------|--------|
| Accuracy | **99.28%** |
| Precision | **99.30%** |
| Recall | **99.28%** |
| F1 Score | **99.28%** |
| AUC | **1.000** |

---

# 🔥 Explainable AI (Grad-CAM)

To improve model interpretability, Grad-CAM is applied to visualize the image regions responsible for each prediction.

For each test image, the project generates:

- Original MRI
- Heatmap
- Overlay Visualization

This helps understand how the CNN makes predictions.

---




---

# ⚙ Installation

Clone the repository

```bash
git clone https://github.com/YourUsername/Brain-Tumor-MRI-Classification.git

cd Brain-Tumor-MRI-Classification
```

Install dependencies

```bash
pip install -r requirements.txt
```

---

# ▶ Run

Open the notebook using Google Colab or Jupyter Notebook.

Train the model.

Evaluate performance.

Generate Grad-CAM visualizations.

---

# 📷 Results

The repository includes:

- Training Curves
- Confusion Matrix
- ROC Curves
- Classification Report
- Grad-CAM Visualizations

---

# 📚 References

The implementation is inspired by recent research in:

- ResNet50 Transfer Learning
- Brain MRI Classification
- Explainable Artificial Intelligence (Grad-CAM)
- Medical Image Analysis

---

# ⚠ Disclaimer

This project is intended solely for academic research and educational purposes.

It is **NOT** approved for clinical diagnosis or medical decision-making.

---

# 👨‍💻 Author

**Anas Mohammad**

Faculty of Artificial Intelligence Engineering

Syrian Private University (SPU)

---

# ⭐ If you found this project useful

Please consider giving it a ⭐ on GitHub!
