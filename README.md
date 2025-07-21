# 💊 Drug Prescription Classifier

Welcome to the **Drug Analysis** project! Here, we combine data science and healthcare to predict which drug a patient should take based on their health profile. Built using Python and scikit-learn, this notebook walks through an end-to-end machine learning pipeline complete with exploration, modeling, and predictions.

---

## 🎯 Project Objective

The goal? **Predict the best drug** for a patient using their:

- Age
- Sex
- Blood Pressure level (BP)
- Cholesterol level
- Sodium-to-Potassium ratio (Na_to_K)

We’ll be building and tuning a **Support Vector Classifier (SVC)** to classify patients into one of five drug types ⚗️.

---

## 📊 Dataset Overview

Sourced from healthcare records, this dataset contains **200 entries** and 6 features:

| Feature        | Description                                           |
|----------------|-------------------------------------------------------|
| `Age`          | Age of the patient (numeric)                          |
| `Sex`          | Gender (M/F)                                          |
| `BP`           | Blood pressure: LOW, NORMAL, or HIGH                  |
| `Cholesterol`  | Cholesterol: NORMAL or HIGH                           |
| `Na_to_K`      | Sodium-to-Potassium ratio in the blood (float)        |
| `Drug`         | Target variable (DrugA, DrugB, DrugC, DrugX, DrugY)   |

📁 **Data file**: [`drug.csv`](./drug.csv)

---

## 🧪 What's Inside `Drug_Analysis.ipynb`?

This notebook walks through:

### 1. 🧼 Data Preparation
- Loaded the dataset using `pandas`
- Checked for missing values
- Normalized categorical features using `LabelEncoder`

### 2. 🔍 Exploratory Data Analysis (EDA)
- Distribution plots for age and Na_to_K
- Count plots to understand categorical spreads
- Outlier detection for better feature understanding

### 3. 🧠 Model Building
- Chose **Support Vector Classifier (SVC)** for its performance on small to medium-sized datasets
- Split data into training and testing subsets (`train_test_split`)

### 4. 🎯 Hyperparameter Tuning
- Applied **GridSearchCV** across multiple values for:
  - `C`: [1, 5, 10, 50, 100]
  - `gamma`: [0.1, 0.01, 20, 60, 100]
- Trained final model with best parameters (`C=100`, `gamma=0.01`)

### 5. 💡 Prediction Function
Includes a simple, user-friendly function to input patient data and get a drug recommendation instantly.


---

## 🧠 Dependencies You'll need:
1. python>=3.7
2. pandas
3. numpy
4. matplotlib
5. seaborn
6. scikit-learn
   
Install them via pip if needed:
!pip install pandas numpy matplotlib seaborn scikit-learn


---

# Interested in experimenting with other models? Try using:
- Random Forest
- Logistic Regression

---

*Made with care, code, and a little caffeine ☕*
