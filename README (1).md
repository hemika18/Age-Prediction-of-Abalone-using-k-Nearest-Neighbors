# 🐚 Abalone Age Prediction using k-Nearest Neighbors

This project implements a **k-Nearest Neighbors (k-NN)** algorithm from scratch to predict the age of abalones based on their physical characteristics. The dataset is sourced from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/abalone).

---

## 📊 Project Overview

- **Goal**: Predict the age (in terms of "Rings") of abalone shells using physical attributes.
- **Dataset**: [Abalone dataset](https://archive.ics.uci.edu/ml/machine-learning-databases/abalone/abalone.data)
- **Algorithm**: Custom implementation of the k-NN algorithm using Euclidean distance.
- **Evaluation Metric**: Mean Squared Error (MSE)

---

## ✅ Features

- Manual implementation of:
  - Euclidean distance calculation
  - Nearest neighbor search
  - Prediction using mode of neighbor labels
- Hyperparameter tuning for `k` (number of neighbors)
- MSE analysis across multiple `k` values
- Prediction on a custom test input
- Visualization of `k` vs MSE curve

---

## 🛠️ Dependencies

- Python 3.x
- NumPy
- Pandas
- Matplotlib
- scikit-learn (for `train_test_split` only)

Install them using:

```bash
pip install numpy pandas matplotlib scikit-learn


**How to Run**

1.  Download or clone the project.
2. Ensure all required libraries are installed (pip install as above).
3. Run the Python script or notebook:
      If using a script (abalone_knn.py):
           python abalone_knn.py

      If using a Jupyter Notebook:
             jupyter notebook

**output**

Predict the age for a new abalone data point
Determine the optimal k value by minimizing MSE
Plot the relationship between k and prediction error
