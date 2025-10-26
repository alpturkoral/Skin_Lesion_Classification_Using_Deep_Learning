<h1 align="center">🩺 Skin Cancer Detection Using Deep Learning</h1>

<p align="center">
  <b>A comprehensive deep learning pipeline for automatic classification of skin lesion images using multiple CNN architectures and transfer learning.</b>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Framework-TensorFlow-orange?style=flat-square">
  <img src="https://img.shields.io/badge/Language-Python-blue?style=flat-square">
  <img src="https://img.shields.io/badge/Web%20App-Streamlit-red?style=flat-square">
  <img src="https://img.shields.io/badge/Dataset-ISIC-green?style=flat-square">
</p>

---

## 📌 Project Description

This project focuses on the **automatic classification of skin lesion images** using deep learning.  
The goal is to build a system that can analyze a dermoscopic skin image and classify it into one of **nine lesion categories**, some of which are cancerous and require urgent medical attention.

The project includes a full machine learning pipeline:

### 1) **Dataset Preparation**
- The ISIC Skin Cancer Dataset was used.
- The dataset includes 9 different lesion types.
- The images were separated into **training** and **testing** sets.
- Corrupted, unreadable, or completely blank images were automatically detected and removed.

### 2) **Data Preprocessing**
- All images were resized to **224×224**.
- Pixel values were normalized to the **0–1** range.
- **Data augmentation** was applied to increase variation and reduce overfitting, including rotation, shifting, zooming, flipping and shearing.

### 3) **Model Development**
Four different deep learning architectures were trained and compared:

| Model | Type | Purpose |
|------|------|---------|
| **CNN (Baseline Model)** | Custom CNN | Used as a base reference performance |
| **LeNet** | Classic CNN | Lightweight alternative for fast inference |
| **VGG16** | Transfer Learning | Deep hierarchical feature extraction |
| **InceptionV3** | Transfer Learning | Multi-scale feature learning → **Best results** |

Each model was trained for 10 epochs using `categorical_crossentropy` loss and `Adam` optimizer.

### 4) **Model Evaluation**
- Accuracy and loss curves were analyzed.
- InceptionV3 and VGG16 achieved the **highest classification performance**.
- The baseline CNN model showed signs of overfitting.
- LeNet performed moderately but efficiently.



---





