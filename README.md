# Dino-Derm: Multimodal Skin Lesion Classification with Explainable AI

## 📌 Overview
Dino-Derm is an advanced multimodal diagnostic framework for skin lesion classification that combines computer vision (DINOv2) with clinical metadata and introduces a novel interpretability metric called the **Quantifiable Severity Index (QSI)**.

---

## 🚀 Project Overview
Traditional AI models in dermatology rely only on image data and often act as black boxes. Dino-Derm addresses these limitations by:

- Integrating dermoscopic images + patient metadata  
- Using a self-supervised foundation model (DINOv2)  
- Providing quantitative interpretability (QSI) instead of just heatmaps  

---

## 🏗️ System Architecture
The system follows a **multimodal late-fusion architecture**:

### 🔹 Visual Branch
- DINOv2 Vision Transformer extracts a 768-dimensional feature vector from dermoscopic images.

### 🔹 Metadata Branch
- Patient data (age, sex, lesion location) is encoded using an MLP (32-dimensional embedding).

### 🔹 Fusion Layer
- Features are concatenated and passed to a classification head.

### 🔹 QSI Module
- Computes a 0–100 severity score using attention-based feature contrast.

---

## 📊 Dataset
**HAM10000 Dataset**
- 10,015 dermoscopic images  
- 7 classes:
  - akiec  
  - bcc  
  - bkl  
  - df  
  - mel  
  - nv  
  - vasc  

---

## ⚙️ Tech Stack
- Python  
- PyTorch  
- DINOv2 (Meta AI)  
- NumPy / Pandas  
- Matplotlib  
- Scikit-learn  

---

## 🧪 Results
- **Accuracy:** 82%  

### ✅ Strong Performance
- Nevi (nv): Recall = 0.96  
- Vascular lesions (vasc): Precision = 1.00  

### ⚠️ Challenges
- Melanoma classification (due to visual similarity)

---

## 🔍 Explainability (QSI)
The **Quantifiable Severity Index (QSI)** is the key innovation of this project.

It measures lesion abnormality using:

- Cosine similarity between lesion and global features  
- Attention-based region importance  


