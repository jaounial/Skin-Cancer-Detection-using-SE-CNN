# 🩺 Skin Cancer Detection using SE-CNN (APS360 Final Project)

This project implements a **Squeeze-and-Excitation Convolutional Neural Network (SE-CNN)** for automated **melanoma detection** from dermatoscopic images. The model performs **binary classification — benign vs malignant** — using the **HAM10000** dataset and is designed to support dermatologists with fast and reliable lesion screening.

---

## ✨ Features
- End-to-end PyTorch pipeline for medical image classification
- Google Drive data loading for Colab training
- Data augmentation + class-weighted training for imbalance
- Baseline comparison (Logistic Regression)
- Custom **Squeeze-and-Excitation attention blocks**
- Training/validation accuracy and loss visualization
- Test-set evaluation + qualitative prediction panel (correct & misclassified samples)

---

## 📁 Dataset
**HAM10000 — Human Against Machine with 10,000 Training Images**

| Label | Type | Notes |
|-------|------|-------|
| Benign | Melanocytic nevi, benign keratosis, etc. | Majority class |
| Malignant | Melanoma | ~11% of dataset |

Images were resized to **224 × 224 × 3**, normalized to **[0,1]**, and augmented via:
- Random rotation
- Horizontal/vertical flips
- Brightness shifts
- Zoom

---

## 🧠 Model Architecture
The model extends a traditional CNN with **Squeeze-and-Excitation (SE) channel attention** to emphasize clinically relevant visual patterns such as pigment networks and asymmetric borders.

