# Iris Flower Classification

This is my very first Machine Learning project! In this repository, I built a classification model using Python to predict the exact species of an Iris flower based on its physical sepal and petal measurements.

---

## 📊 Dataset Overview
The project utilizes the classic **Iris Dataset** loaded directly via the `seaborn` library. 

### Data Structure:
- **Total Samples:** 150 instances
- **Features (Inputs):** `sepal_length`, `sepal_width`, `petal_length`, `petal_width`
- **Target Variable (Output):** `species` 

The dataset contains exactly 3 unique flower classes:
1. `setosa`
2. `versicolor`
3. `virginica`

---

## 🛠️ Project Workflow & Code Implementation

### 1. Data Preparation
- Checked for missing data values using `df.isnull().sum()` to ensure clean data input.
- Split the dataset into features (`X`) and target labels (`y`).
- Used `train_test_split` from `sklearn.model_selection` to divide the dataset into a training set and a testing set (`test_size=0.2`, `random_state=42`).

### 2. Model Training
- Imported and initialized a **K-Neighbors Classifier (`KNeighborsClassifier`)** from `sklearn.neighbors`.
- Fitted the model on the training data (`X_train`, `y_train`).

### 3. Model Evaluation
- Generated predictions on the unseen test data (`X_test`).
- Computed a detailed breakdown of performance using `classification_report`.
- Plotted a visual **Confusion Matrix Heatmap** using `seaborn.heatmap` to cross-examine true versus predicted labels.

---



### 🔬 Classification Report
The model achieved an outstanding **0.96 accuracy rate (96.67%)** on the testing subset, correctly predicting 29 out of 30 flowers.



### 🔍 Results Analysis:
- **Setosa:** Performed perfectly with 1.00 precision and recall. Because of its distinct physical properties, it never gets confused with other classes.
- **Versicolor & Virginica:** The 0.96 overall accuracy indicates that exactly **one flower** was misclassified due to natural measurement overlaps between these two species. 

---

## 📦 Core Libraries Used
- **`pandas`** & **`numpy`**: For data ingestion and data structuring.
- **`seaborn`** & **`matplotlib.pyplot`**: For data sourcing and plotting the confusion matrix heatmap.
- **`scikit-learn`**: For data splitting, executing the `KNeighborsClassifier`, and processing evaluation metrics.

---
*This repository serves as a foundational milestone in my Machine Learning journey.*
