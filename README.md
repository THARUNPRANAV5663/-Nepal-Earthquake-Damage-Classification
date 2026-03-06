# 🏔️ Nepal Earthquake Damage Classification

Predicting the level of structural damage caused to buildings in Nepal by the 2015 Gorkha Earthquake using Machine Learning.

---

## 📌 Problem Statement

The 2015 Nepal earthquake caused massive destruction across thousands of buildings. This project builds a multiclass classification model to predict the **damage grade** of a building (1, 2, or 3) based on its structural and geographic features.

- **Grade 1** – Low damage
- **Grade 2** – Medium damage
- **Grade 3** – Complete destruction

---

## 📂 Dataset

- Source: [DrivenData – Richter's Predictor](https://www.drivendata.org/competitions/57/nepal-earthquake/)
- `train_values.csv` – Building features
- `train_labels.csv` – Damage grade labels
- Dataset size: ~260,000 buildings

---

## ⚙️ Workflow

1. **Data Loading & Merging** – Merged train values and labels on `building_id`
2. **EDA** – Analyzed distributions of `age`, `height_percentage`, `area_percentage` using boxplots and histograms
3. **Outlier Handling** – Capped `age` column at 60 using IQR-based capping
4. **Preprocessing** – Converted 8 object columns to `category` dtype for LightGBM compatibility
5. **Handling Class Imbalance** – Applied SMOTE oversampling
6. **Hyperparameter Tuning** – Used Optuna for automated LightGBM parameter optimization
7. **Threshold Tuning** – Custom threshold tuning per class to improve macro F1

---

## 🤖 Model

| Model | Notes |
|-------|-------|
| **LightGBM (LGBM)** | Primary model, handles categorical features natively |

---

## 📊 Results

| Metric | Score |
|--------|-------|
| **Macro F1 Score** | **0.7056** |
| Class 1 F1 | 0.63 |
| Class 2 F1 | 0.78 |
| Class 3 F1 | 0.70 |

---

## 🛠️ Tech Stack

- Python
- Pandas, NumPy
- LightGBM
- Scikit-learn
- Imbalanced-learn (SMOTE)
- Optuna (Hyperparameter Tuning)
- Matplotlib, Seaborn

---

## 👤 Author

**Tharun Pranav K S**  
B.E – Electronics and Communication Engineering  
Velalar College of Engineering and Technology  
Data Science Intern @ Rubixe  
