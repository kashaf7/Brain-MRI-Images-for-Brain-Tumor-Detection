# 🧠 Brain MRI Images for Brain Tumor Detection

## 📌 Project Overview
This project focuses on detecting brain tumors using MRI images through a Convolutional Neural Network (CNN). The dataset is loaded from Kaggle, preprocessed, and used to train a deep learning model for binary classification (Tumor / No Tumor).

---

## 🎯 Objectives
- Load MRI dataset from Kaggle
- Explore and visualize image data
- Perform preprocessing and data preparation
- Build and train a CNN model
- Evaluate model performance
- Make predictions on unseen data

---

## 📂 Dataset
- **Source:** Kaggle Hub  
- **Dataset:** Brain MRI Images for Brain Tumor Detection  
- **Classes:**
  - `Yes` → Tumor present
  - `No` → No tumor

---

## ⚙️ Workflow

### 1️⃣ Data Loading
- Dataset downloaded using `kagglehub`
- Extracted dataset path and verified contents

### 2️⃣ Data Exploration
- Listed all subdirectories (classes)
- Counted number of images per class
- Displayed sample images for visualization

### 3️⃣ Data Preparation
- Created a DataFrame with:
  - Image paths
  - Corresponding labels
- Shuffled dataset for randomness

### 4️⃣ Train-Test Split
- Training set: 70%
- Validation set: 15%
- Testing set: 15%

### 5️⃣ Image Analysis
- Checked image dimensions (height & width)

### 6️⃣ Image Preprocessing
- Resized images to (224 × 224)
- Used `ImageDataGenerator` for:
  - Rescaling
  - Augmentation

### 7️⃣ Model Building (CNN)
- Built using TensorFlow/Keras
- Layers used:
  - Conv2D
  - MaxPooling2D
  - Flatten
  - Dense

### 8️⃣ Model Training
- Trained on training dataset
- Validated using validation dataset

### 9️⃣ Model Evaluation
- Evaluated performance on test dataset
- Metrics:
  - Accuracy
  - Loss

### 🔟 Predictions
- Model predicts tumor presence on new MRI images

---

## 🛠️ Technologies Used
- Python
- TensorFlow / Keras
- Pandas
- NumPy
- Matplotlib
- PIL (Python Imaging Library)
## 📂 Dataset

This project uses the **Brain MRI Images for Brain Tumor Detection** dataset from Kaggle.

🔗 https://www.kaggle.com/datasets/navoneel/brain-mri-images-for-brain-tumor-detection

The dataset is automatically downloaded using `kagglehub`, so no manual dataset upload is required.
---


