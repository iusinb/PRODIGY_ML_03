# Task-03: Cats vs Dogs Classification using SVM

## Overview

This project implements a **Support Vector Machine (SVM)** to classify images into two categories:

* Cat
* Dog

The task was completed as part of the **Prodigy Infotech Machine Learning Internship – Task 03**.

---

## Objective

Implement a Support Vector Machine (SVM) model for binary image classification using a Cats vs Dogs image dataset.

The complete pipeline includes:

1. Dataset preparation
2. Image preprocessing
3. HOG feature extraction
4. Training and testing data split
5. SVM model training
6. Model evaluation
7. Prediction on unseen images

---

## Dataset

The project uses a **Dogs vs Cats image dataset**, based on the Kaggle Dogs vs Cats competition.

Kaggle competition:

https://www.kaggle.com/c/dogs-vs-cats

For this implementation, a balanced subset of **2,000 training images** was used:

| Class     |    Images |
| --------- | --------: |
| Cats      |     1,000 |
| Dogs      |     1,000 |
| **Total** | **2,000** |

The dataset itself is not included in this repository because of its large size.

---

## Technologies Used

* Python
* NumPy
* Scikit-learn
* Scikit-image
* Matplotlib
* Seaborn
* Joblib
* Google Colab

---

## Image Preprocessing

Each image was processed using the following pipeline:

```text
Input Image
     ↓
Resize to 64 × 64
     ↓
Convert to Grayscale
     ↓
HOG Feature Extraction
     ↓
Feature Vector
     ↓
SVM Classifier
```

### HOG Feature Extraction

Histogram of Oriented Gradients (HOG) features were extracted using:

```python
orientations = 9
pixels_per_cell = (8, 8)
cells_per_block = (2, 2)
```

The extracted HOG features were then used as input to the SVM classifier.

---

## Train-Test Split

The dataset was divided using an 80:20 split.

| Dataset  | Samples |
| -------- | ------: |
| Training |   1,600 |
| Testing  |     400 |

Stratified splitting was used to maintain a balanced distribution of cats and dogs in both sets.

---

## SVM Model

The classifier was implemented using Scikit-learn's `SVC`.

```python
SVC(
    kernel="linear",
    C=1.0
)
```

### Model Configuration

| Parameter        | Value                  |
| ---------------- | ---------------------- |
| Algorithm        | Support Vector Machine |
| Kernel           | Linear                 |
| C                | 1.0                    |
| Training samples | 1,600                  |
| Testing samples  | 400                    |

---

## Results

The trained SVM achieved:

### **Accuracy: 69.5%**

The model was additionally evaluated using:

* Precision
* Recall
* F1-score
* Confusion Matrix

The complete evaluation results can be found in the Jupyter/Colab notebook.

---

## Confusion Matrix

The confusion matrix shows the number of correctly and incorrectly classified cat and dog images.

![SVM Confusion Matrix](figures/confusion_matrix.png)

---

## Sample Prediction

The trained model was also tested on an unseen image from the test dataset.

![Sample Prediction](figures/sample_prediction.png)

---

## Classification Report

The model was evaluated using Scikit-learn's classification report, including:

* Precision
* Recall
* F1-score
* Support

The generated classification report is available in the project notebook.

---

## Project Structure

```text
PRODIGY_ML_03/
│
├── README.md
├── Task_03_SVM_Cats_Dogs.ipynb
├── svm_cats_dogs_model.pkl
│
└── figures/
    ├── confusion_matrix.png
    └── sample_prediction.png
```

### Files

**`Task_03_SVM_Cats_Dogs.ipynb`**

Complete implementation containing dataset preparation, preprocessing, HOG feature extraction, SVM training, evaluation, and prediction.

**`svm_cats_dogs_model.pkl`**

Saved trained SVM model.

**`figures/`**

Contains visual outputs generated during model evaluation.

---

## How to Run

1. Open `Task_03_SVM_Cats_Dogs.ipynb` in Google Colab or Jupyter Notebook.
2. Install the required Python libraries.
3. Prepare the Cats vs Dogs dataset.
4. Run the notebook cells sequentially.
5. The notebook performs preprocessing, feature extraction, model training, evaluation, and prediction.

The dataset is intentionally not included in this repository due to its size.

---

## Conclusion

A Linear Support Vector Machine was successfully implemented for Cats vs Dogs image classification using HOG-based image features.

The model achieved an accuracy of **69.5%** on the test set and was further evaluated using a classification report, confusion matrix, and individual image prediction.
