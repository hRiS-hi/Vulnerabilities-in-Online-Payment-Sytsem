# 🕵️‍♂️ Fraudulent Payment Detection using Machine Learning

This project detects fraudulent financial transactions using various Machine Learning techniques. It includes enhanced feature engineering, class imbalance handling, and model optimization using ensemble methods like Random Forest and XGBoost.

---

## 📌 Project Overview

- 📊 **Dataset**: Simulated transaction data (BankSim-style)
- 🎯 **Goal**: Predict whether a transaction is fraudulent
- 📈 **Models Used**:
  - Random Forest (with class weights)
  - XGBoost (optional)
- 📐 **Techniques Applied**:
  - SMOTE for class imbalance
  - Cross-validation with stratified sampling
  - Feature importance + ROC/AUC Evaluation

---

## 🧪 Features Engineered

- **Transaction Frequency**: Number of transactions per customer
- **Fraud Frequency**: Number of frauds per customer
- **Amount Stats**: Mean, Min, Max amounts per customer
- **Interaction Feature**: `amount × transaction_type`
- **Label Encoding**: Gender, Category
- **Missing Value Handling**

---

## 🧠 ML Workflow

1. **Data Cleaning & Encoding**
2. **Feature Engineering**
3. **Train-Test Split (Stratified)**
4. **SMOTE Over-Sampling**
5. **Model Training**
6. **Evaluation Metrics**:
   - Confusion Matrix
   - Precision, Recall, F1-score
   - ROC Curve, AUC Score
7. **Feature Importance Visualization**

---

## 📊 Results

| Metric     | Value  |
|------------|--------|
| Precision  | ~0.73 (Fraud class) |
| Recall     | ~0.84 (Fraud class) |
| F1-Score   | ~0.78 |
| AUC Score  | ~0.995 |

✅ Excellent fraud detection performance with strong recall (low false negatives).

---

## 🔧 Tech Stack

- Python 🐍
- Scikit-learn
- imbalanced-learn (SMOTE)
- Pandas, NumPy
- Matplotlib, Seaborn

---

## 🚀 How to Run

```bash
git clone https://github.com/yourusername/fraud-detection-ml.git
cd fraud-detection-ml

# Install requirements
pip install -r requirements.txt

# Run the notebook
jupyter notebook transaction_fraudulent_detection.ipynb

