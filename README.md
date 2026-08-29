# 🐚 Abalone Age Prediction using k-Nearest Neighbors

A machine learning project that implements the **k-Nearest Neighbors (k-NN)** algorithm to predict the age of abalones based on their physical characteristics.

The project focuses on understanding the working of k-NN by implementing the core algorithm manually, experimenting with different values of `k`, and evaluating prediction performance using **Mean Squared Error (MSE)**.

---

##  Project Overview

Determining the age of an abalone traditionally involves counting the rings present on its shell. This project explores the possibility of predicting the number of rings from measurable physical characteristics of the abalone.

###  Objective

* Predict the number of **rings** of an abalone using its physical measurements.
* Implement the core k-NN algorithm manually.
* Experiment with different values of `k`.
* Evaluate model performance using Mean Squared Error.
* Identify a suitable value of `k` based on prediction error.
* Visualize the relationship between `k` and MSE.
* Make predictions for a new abalone sample.

> The number of rings is commonly used as an indicator of abalone age.

---

## 📊 Dataset

The project uses the **Abalone Dataset** from the UCI Machine Learning Repository.

**Source:** [UCI Machine Learning Repository – Abalone Dataset](https://archive.ics.uci.edu/ml/datasets/abalone)

The dataset contains physical measurements of abalones along with their corresponding number of rings.

### Features

| Feature          | Description                      |
| ---------------- | -------------------------------- |
| `Sex`            | Sex of the abalone               |
| `Length`         | Longest shell measurement        |
| `Diameter`       | Diameter perpendicular to length |
| `Height`         | Height of the shell              |
| `Whole weight`   | Whole abalone weight             |
| `Shucked weight` | Weight of the meat               |
| `Viscera weight` | Weight of the gut                |
| `Shell weight`   | Weight of the shell              |
| `Rings`          | Number of shell rings            |

`Rings` is used as the target variable.

---

##  How k-NN Works

k-Nearest Neighbors predicts the output for a new data point by looking at the **k closest observations** in the training dataset.

The project follows these steps:

```text
                 Abalone Dataset
                        │
                        ▼
                Data Preprocessing
                        │
                        ▼
                  Train / Test Split
                        │
                        ▼
              Calculate Distances
                        │
                        ▼
              Find k Nearest Neighbors
                        │
                        ▼
                   Make Prediction
                        │
                        ▼
                  Calculate MSE
                        │
                        ▼
               Compare Different k
```

### Euclidean Distance

The similarity between two observations is measured using Euclidean distance:

[
d(x,y)=\sqrt{\sum_{i=1}^{n}(x_i-y_i)^2}
]

For a new sample, distances to the training samples are calculated and the nearest neighbors are selected.

---

##  Implementation

The project implements the main components of k-NN, including:

### 1. Distance Calculation

Euclidean distance is calculated between the input sample and training samples.

### 2. Nearest Neighbor Selection

Training samples are ranked according to their distance from the input sample.

### 3. Prediction

The selected nearest neighbors are used to generate the predicted target value.

### 4. Hyperparameter Tuning

Multiple values of `k` are tested to study their effect on prediction performance.

### 5. Model Evaluation

The predictions are evaluated using **Mean Squared Error (MSE)**.

[
MSE=\frac{1}{n}\sum_{i=1}^{n}(y_i-\hat{y_i})^2
]

A lower MSE indicates lower prediction error.

---

##  Model Evaluation

The project evaluates the model for different values of `k`.

A **`k` vs MSE** plot is generated to visualize how prediction error changes as the number of neighbors changes.

The value of `k` corresponding to the lowest observed MSE can be used to select a suitable neighborhood size.

---

##  Prediction on New Data

The project also demonstrates how the trained k-NN implementation can be used to predict the number of rings for a **new abalone sample** based on its physical characteristics.

---

##  Technologies Used

* **Python 3**
* **NumPy** – numerical operations
* **Pandas** – data loading and manipulation
* **Matplotlib** – visualization
* **Scikit-learn** – train-test splitting

The core k-NN logic is implemented manually to understand the algorithm rather than relying entirely on a pre-built k-NN model.

---


---

##  How to Run

### Using Jupyter Notebook

Start Jupyter Notebook:

```bash
jupyter notebook
```

Open the project notebook and execute the cells sequentially.

### Using a Python Script

If the implementation is saved as a Python script:

```bash
python abalone_knn.py
```

---

##  Project Structure

```text
Age-Predicton-of-Abalone-using-k-Nearest-Neighbors-
│
├── abalone_knn.ipynb
├── abalone.data
├── README.md
└── ...
```

---

##  Key Learnings

This project provides practical understanding of:

* The working principle of **k-Nearest Neighbors**
* Euclidean distance-based similarity
* Data preprocessing
* Train-test splitting
* Hyperparameter selection
* Model evaluation using MSE
* Visualization of model performance
* Making predictions using a custom ML implementation

---

## 📚 Reference

**UCI Machine Learning Repository — Abalone Dataset**

https://archive.ics.uci.edu/ml/datasets/abalone

---

## ⭐ Project

This project was developed as an exploration of the **k-Nearest Neighbors algorithm and its application to predicting abalone age from physical measurements**.
