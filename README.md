# Titanic Survival Prediction – Machine Learning Model Comparison

## 📌 Overview
This project is an end-to-end machine learning pipeline that predicts passenger survival using a Titanic-style dataset. It focuses on data preprocessing, feature engineering, model training, and performance comparison across multiple classical machine learning algorithms.

---

## 🎯 Problem Statement
Build and compare machine learning models to predict passenger survival from a Titanic-style dataset.

- **Input:** `survival.csv`
- **Target Variable:** `Survived`
- **Goal:** Identify the best-performing model using standardized evaluation metrics.

---

## 📂 Dataset
- File: `survival.csv`
- Loaded and processed within the notebook / project script
- Contains passenger demographic and travel-related features

---

## ⚙️ Data Preprocessing
The following preprocessing steps are applied:

- Inspected data types and missing values
- Handled missing data:
  - `Age` → Median imputation
  - `Embarked` → Mode imputation
  - `Cabin` → Filled as `"Unknown"`
- Dropped identifier columns:
  - `PassengerId`, `Name`, `Ticket`
- Feature engineering:
  - `Title` extracted from passenger names
  - `FamilySize` feature
  - `HasCabin` binary feature
- Encoded categorical variables using Label Encoding
- Standardized numerical features:
  - `Age`, `Fare`, `FamilySize`

---

## 🔀 Data Splitting
Data is split using a **stratified approach** to preserve class distribution:

- 60% Training
- 20% Validation
- 20% Testing

---

## 🤖 Models Evaluated
The following machine learning models are trained and evaluated:

- K-Nearest Neighbors (KNN)
- Decision Tree
- Gaussian Naive Bayes
- Logistic Regression
- Support Vector Machine (SVM)
- Linear Regression (used as a baseline)

---

## 📊 Evaluation Metrics
Models are evaluated on the validation set using:

- Accuracy
- F1 Score
- ROC AUC

---

## 📈 Visualizations
The project includes:
- Bar chart comparing F1-scores across models
- ROC curves for all models on a single plot
- Final comparison table summarizing model performance

---

## 🚀 How to Run
1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd titanic-survival-ml
2. Install dependencies:
   pip install -r requirements.txt
3. Run the notebook or script:
   python project.py
or open and run survival.ipynb
