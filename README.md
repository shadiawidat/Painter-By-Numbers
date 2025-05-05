# 🎨 Painter by Numbers – Artwork Similarity Detection with Siamese Networks

![Python](https://img.shields.io/badge/Python-3.8+-blue?style=flat&logo=python) 
![PyTorch](https://img.shields.io/badge/PyTorch-Deep_Learning-red?style=flat&logo=pytorch)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

## 📌 Project Overview

**Painter by Numbers** is a deep learning project that predicts whether two given paintings were created by the same artist. By leveraging **Siamese Neural Networks** with a pre-trained **ResNet-18**, the model learns to identify visual similarities and stylistic features unique to each artist. 

## 🚀 Key Features

- 🧠 **Siamese Network Architecture**: Twin neural networks process image pairs to learn stylistic similarities.
- 🏗️ **Pre-trained ResNet18 Backbone**: Utilizes transfer learning for powerful feature extraction.
- 🔺 **Triplet Loss Function**: Encourages meaningful embeddings by minimizing intra-class distance and maximizing inter-class distance.
- 🔄 **Dynamic Data Augmentation**: Increases robustness and prevents overfitting.
- 📊 **Strong Generalization**: Achieved **81.78% test accuracy** on unseen artist images.

## 🧰 Technologies Used

- **Python 3.8+**
- **PyTorch** – Deep learning model development
- **Torchvision** – Pre-trained models & transformations
- **OpenCV / PIL** – Image loading and manipulation
- **Matplotlib ** – Performance visualization
- **Google Colab & PyCharm** – Development and training platforms

## 📂 Dataset & Preprocessing

- Source: [Kaggle - Painter by Numbers](https://www.kaggle.com/competitions/painter-by-numbers)
- ~18,000 images from 1,200+ artists used for training/validation
- Test set includes images from **unseen artists** (true generalization test)
- All images center-cropped to **224x224**
- Triplet samples (Anchor, Positive, Negative) generated per epoch to increase variability


## 📈 Results

The Siamese Network was trained using **Triplet Loss** with dynamic sampling of (anchor, positive, negative) image triplets. After 12 epochs, the model reached optimal generalization performance.

- ✅ **Test Accuracy**: **81.78%**
- 📉 Overfitting observed after epoch 12
- 📦 Model trained on ~30,000 triplets per epoch using 224x224 center-cropped images

### 🟪 Training & Validation Loss

![image](https://github.com/user-attachments/assets/6883cadf-c289-4caa-8980-8e7deeff7a4e)

### 🟩 Accuracy Over Epochs

![image](https://github.com/user-attachments/assets/412a9b86-ad0b-4a8e-99d0-9919f94a0d8f)
![image](https://github.com/user-attachments/assets/7c8eb610-717e-4852-8f15-f970905e695f)

