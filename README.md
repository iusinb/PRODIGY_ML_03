# Task-03: Cats vs Dogs Classification using SVM

## Objective

Implement a Support Vector Machine (SVM) to classify images of cats and dogs.

## Dataset

Dogs vs Cats image dataset.

For this implementation, 2,000 images were used:
- 1,000 Cat images
- 1,000 Dog images

## Methodology

1. Load cat and dog images
2. Resize images to 64 × 64 pixels
3. Convert images to grayscale
4. Extract HOG (Histogram of Oriented Gradients) features
5. Split the dataset into training and testing sets
6. Train a Linear SVM classifier
7. Evaluate the model using accuracy, classification report and confusion matrix
8. Test the model on an individual image

## Model

- Algorithm: Support Vector Machine (SVM)
- Kernel: Linear
- C: 1.0
- Training samples: 1,600
- Testing samples: 400

## Results

**Accuracy: 69.5%**

The model was also evaluated using:
- Precision
- Recall
- F1-score
- Confusion Matrix

## Files

- `Task_03_SVM_Cats_Dogs.ipynb` — Complete implementation
- `svm_cats_dogs_model.pkl` — Trained SVM model
- `README.md` — Project documentation

## Technologies Used

- Python
- Scikit-learn
- Scikit-image
- NumPy
- Matplotlib
- Seaborn
- Google Colab

## How to Run

Open the `.ipynb` file using Google Colab or Jupyter Notebook and run the cells sequentially.

The dataset used for training is not included in this repository due to its size.