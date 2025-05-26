# Titanic-Data-Cleaning-for-ML

This repository contains a step-by-step walkthrough of cleaning, preprocessing, and preparing the Titanic dataset for machine learning tasks.

## 📂 Dataset

The dataset is pulled directly from the [Titanic - Machine Learning from Disaster](https://www.kaggle.com/datasets/yasserh/titanic-dataset) competition. In this project, I use a hosted version via:

[https://raw.githubusercontent.com/SiddardhaShayini/Titanic-Data-Cleaning-for-ML/refs/heads/main/Dataset/Titanic-Dataset.csv](https://raw.githubusercontent.com/SiddardhaShayini/Titanic-Data-Cleaning-for-ML/refs/heads/main/Dataset/Titanic-Dataset.csv)

## 🧼 Cleaning & Preprocessing Steps

### ✅ 1. Load & Inspect Data
- Load dataset using `pandas`
- Check for missing values
- View data types and structure

### 🔧 2. Handle Missing Data
- Fill missing `Age` values with median
- Fill missing `Embarked` values with the mode
- Drop the `Cabin` column due to excessive missing data

### 🧠 3. Encode Categorical Features
- Convert `Sex` column to numeric (0 = male, 1 = female)
- Apply one-hot encoding to `Embarked` (`Embarked_C`, `Embarked_Q`, `Embarked_S`)

### 📊 4. Feature Scaling
- Standardize `Age` and `Fare` using `StandardScaler`

### 🧹 5. Outlier Detection & Removal
- Identify outliers using the IQR method on numerical features: `Age`, `Fare`, `SibSp`, `Parch`
- Remove rows with outliers (per column) using IQR-based filtering
- Visualize before & after with boxplots

### 📉 6. Final Outlier Summary

| Feature | Outliers Before | Outliers After |
|---------|------------------|-----------------|
| Age     | 66               | 43              |
| Fare    | 116              | 64              |
| SibSp   | 46               | 104             |
| Parch   | 213              | 0               |
| **Total** | **441**         | **211**         |

## 📊 Visualizations

Boxplots are provided before and after outlier removal for easy comparison.

## 🛠️ Requirements

- Python 3.x
- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`


## ✍️ Author

- Siddardha Shayini

---

