# 🏦 Bank Customer Term Deposit Subscription Prediction

A complete end-to-end Machine Learning pipeline to predict whether a bank customer will subscribe to a term deposit based on their profile and marketing campaign data.

---

## 📌 Project Overview

Banks run expensive marketing campaigns to get customers to subscribe to term deposits. This project builds a classification model that predicts **who will subscribe** — before the call is even made. This helps banks target the right customers and save resources.

---

## 📂 Dataset

- **Source:** [Bank Marketing Dataset – Kaggle](https://www.kaggle.com/datasets/janiobachmann/bank-marketing-dataset)
- **Size:** 11,162 rows × 17 columns
- **Target Variable:** `deposit` — whether the customer subscribed (yes/no)

---

## 🔧 Tech Stack

| Tool | Purpose |
|------|---------|
| Python | Core language |
| Pandas & NumPy | Data manipulation |
| Matplotlib & Seaborn | Data visualization |
| Scikit-learn | Model training & evaluation |
| SHAP | Explainable AI |

---

## 🗂️ Project Structure

```
bank-customer-prediction/
│
├── task1_term_deposit_prediction.ipynb   # Main notebook
├── bank.csv                               # Dataset
└── README.md                             # You are here
```

---

## 🚀 Pipeline Steps

### 1. 🔍 Exploratory Data Analysis (EDA)
- Checked dataset shape, missing values, duplicates
- Analyzed target variable distribution
- Visualized categorical and numerical features
- Plotted correlation heatmap

### 2. ⚙️ Feature Engineering
- **Label Encoding** for binary columns (`yes/no` → `1/0`)
- **One-Hot Encoding** for multi-category columns (`job`, `marital`, `education`, etc.)
- **StandardScaler** for feature scaling

### 3. 🤖 Model Training
Trained and compared two classification models:
- **Logistic Regression** — simple baseline model
- **Random Forest** — ensemble model with 100 decision trees

### 4. 📊 Model Evaluation
Evaluated both models using:
- **Confusion Matrix** — where exactly is the model wrong?
- **Classification Report** — Precision, Recall, F1-Score
- **ROC Curve & AUC Score** — how well does the model separate classes?

### 5. 💡 Explainable AI (SHAP)
- Used `TreeExplainer` on Random Forest model
- Generated **global feature importance** plot
- Explained **5 individual customer predictions** with top reasons

---

## 📈 Results

| Model | Accuracy | F1 Score | AUC |
|-------|----------|----------|-----|
| Logistic Regression | ~86% | ~85% | ~0.93 |
| Random Forest | ~86% | ~85% | ~0.94 |

> Random Forest performed slightly better overall with higher AUC score.

---

## 💡 Key Insights

- **Call duration** was the strongest predictor — longer calls = more likely to subscribe
- **Account balance** played a significant role — higher balance = more likely to subscribe
- **Previous campaign outcome** heavily influenced current subscription likelihood

---

## 📚 Concepts Covered

- Exploratory Data Analysis (EDA)
- Label Encoding & One-Hot Encoding
- Train/Test Split & Feature Scaling
- Logistic Regression & Random Forest
- Confusion Matrix, F1-Score, ROC Curve
- Explainable AI with SHAP

---

## 👤 Author

**Aimen Safdar**
.
