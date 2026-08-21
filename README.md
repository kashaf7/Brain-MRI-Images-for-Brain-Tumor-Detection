# 🧠 Brain MRI Images for Brain Tumor Detection

## 📌 Project Overview

This project focuses on detecting brain tumors using MRI images through a Convolutional Neural Network (CNN). The dataset is loaded from Kaggle, preprocessed, and used to train a deep learning model for binary classification: **Tumor / No Tumor**.

The project covers the complete deep learning workflow, including data loading, exploration, preprocessing, augmentation, model building, training, evaluation, and prediction.

---

## 🎯 Objectives

* Load the Brain MRI dataset from Kaggle
* Explore and visualize MRI image data
* Perform preprocessing and data preparation
* Apply image augmentation
* Build and train a CNN model
* Evaluate model performance
* Make predictions on unseen MRI images

---

## 📂 Dataset

This project uses the **Brain MRI Images for Brain Tumor Detection** dataset from Kaggle.

**Dataset:** Brain MRI Images for Brain Tumor Detection

**Classes:**

* `Yes` → Tumor present
* `No` → No tumor

The dataset was loaded using `kagglehub`.

The dataset contains:

| Class           | Number of Images |
| --------------- | ---------------: |
| Tumor (`Yes`)   |              155 |
| No Tumor (`No`) |               98 |
| **Total**       |          **253** |

The dataset is split approximately into:

* **Training:** 70%
* **Validation:** 15%
* **Testing:** 15%

---

## ⚙️ Workflow

### 1️⃣ Data Loading

* Dataset downloaded using `kagglehub`
* Extracted dataset path
* Verified dataset contents and class folders

### 2️⃣ Data Exploration

* Listed dataset subdirectories
* Counted the number of images in each class
* Displayed sample MRI images for visualization

### 3️⃣ Data Preparation

* Created a Pandas DataFrame containing:

  * Image paths
  * Corresponding labels
* Shuffled the dataset using a fixed random seed

### 4️⃣ Train, Validation and Test Split

The dataset was divided approximately into:

* **70% Training**
* **15% Validation**
* **15% Testing**

### 5️⃣ Image Analysis

* Checked the dimensions of sample MRI images
* Resized all images to **224 × 224 pixels**

### 6️⃣ Image Preprocessing and Augmentation

`ImageDataGenerator` was used for preprocessing and augmentation.

The following techniques were applied:

* Pixel rescaling from `0–255` to `0–1`
* Random rotation
* Width shifting
* Height shifting
* Shear transformation
* Zoom augmentation
* Horizontal flipping

---

## 🧠 Model Architecture

A custom **Convolutional Neural Network (CNN)** was built using TensorFlow and Keras.

The model architecture includes:

* Input Layer: **224 × 224 × 3**
* Conv2D Layer with 32 filters
* MaxPooling2D Layer
* Conv2D Layer with 64 filters
* MaxPooling2D Layer
* Conv2D Layer with 64 filters
* MaxPooling2D Layer
* Flatten Layer
* Dense Layer with 64 neurons
* Output Layer for binary classification

---

## ⚙️ Model Configuration

| Parameter         | Value                    |
| ----------------- | ------------------------ |
| Framework         | TensorFlow / Keras       |
| Model             | Custom CNN               |
| Image Size        | 224 × 224                |
| Batch Size        | 32                       |
| Epochs            | 50                       |
| Optimizer         | Adam                     |
| Loss Function     | Categorical Crossentropy |
| Number of Classes | 2                        |

---

## 🏋️ Model Training

The CNN model was trained using the training dataset and evaluated using the validation dataset for **50 epochs**.

During training, the model performance was tracked using:

* Training Accuracy
* Validation Accuracy
* Training Loss
* Validation Loss

---

## 📈 Results

The trained CNN model achieved the following results:

| Metric                   |     Result |
| ------------------------ | ---------: |
| Training Accuracy        | **76.84%** |
| Test Accuracy            | **74.36%** |
| Best Validation Accuracy | **91.89%** |
| Training Epochs          |     **50** |

The final model achieved a **test accuracy of 74.36%** on the held-out test dataset.

The best validation accuracy observed during training was **91.89%**.

> **Note:** The test accuracy is considered the primary evaluation metric because it measures performance on unseen data.

---

## 🔍 Prediction

The trained model can be used to predict whether a new MRI image belongs to:

* **Tumor Present**
* **No Tumor**

For prediction, the input MRI image is:

1. Resized to **224 × 224**
2. Converted into an array
3. Normalized by dividing pixel values by `255`
4. Expanded to include the batch dimension
5. Passed through the trained CNN model

The predicted class is determined using `argmax()`.

---

## 🛠️ Technologies Used

* Python
* TensorFlow
* Keras
* Pandas
* NumPy
* Matplotlib
* PIL (Python Imaging Library)
* KaggleHub

---

## 📁 Project Structure

```text
Brain-MRI-Images-for-Brain-Tumor-Detection/
│
├── brain_MRI_images.ipynb
├── README.md
└── requirements.txt
```

---

## ⚠️ Limitations

* The dataset contains only **253 MRI images**
* The classes are slightly imbalanced
* The model was trained using a relatively small dataset
* Limited generalization testing was performed
* The model is intended for educational and experimental purposes
* This project should **not be used for clinical or medical diagnosis**

Potential improvements include:

* Using a larger and more diverse dataset
* Applying transfer learning using models such as EfficientNet or ResNet
* Performing hyperparameter tuning
* Using cross-validation
* Improving model evaluation with metrics such as precision, recall, F1-score, and a confusion matrix

---

## 🚀 How to Run

### 1. Clone the Repository

```bash
git clone https://github.com/kashaf7/Brain-MRI-Images-for-Brain-Tumor-Detection.git
```

### 2. Navigate to the Project Directory

```bash
cd Brain-MRI-Images-for-Brain-Tumor-Detection
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Open the Notebook

Run the project using Jupyter Notebook, Google Colab, or Kaggle:

```bash
jupyter notebook brain_MRI_images.ipynb
```

---

## 📌 Disclaimer

This project was developed for **educational and learning purposes** to demonstrate the application of Convolutional Neural Networks to medical image classification.

The predictions generated by this model should not be considered medical advice or a professional diagnosis.
