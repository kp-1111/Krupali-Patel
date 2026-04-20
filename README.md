# 📱 Telecom Customer Churn Prediction & Retention Analysis

## 📌 Project Overview
A full end-to-end machine learning project that predicts customer churn 
for a telecom company. The project covers data cleaning, exploratory 
data analysis, feature engineering, and machine learning modeling — 
comparing three classification algorithms to identify the best predictor 
of customer churn.

---

## 🎯 Business Problem
Customer churn is a critical challenge in the telecom industry. 
Retaining existing customers is significantly cheaper than acquiring 
new ones. This project aims to:
- Identify customers at high risk of churning
- Understand the key factors driving churn
- Support the business in building targeted retention strategies

---

## 📊 Dataset
- **Source:** Telco Customer dataset (`telco.csv`)
- **Size:** 7,000+ customer records
- **Features include:** Demographics (Age, Gender, Senior Citizen), 
  Services (Phone, Internet, Streaming), Account info 
  (Contract type, Payment method, Monthly charges, Tenure)
- **Target variable:** `Churn Label` (Yes / No)

## 📋 Data Dictionary (Key Columns)

| Column | Description |
|---|---|
| `Customer ID` | Unique customer identifier |
| `Tenure in Months` | How long the customer has been with the company |
| `Contract` | Contract type (Month-to-Month, One Year, Two Year) |
| `Monthly Charge` | Amount charged per month |
| `Churn Label` | Target variable — Yes if customer churned, No if retained |
| `Churn Score` | Propensity score for churn (0–100) |
| `CLTV` | Customer Lifetime Value |
| `Internet Type` | Type of internet service (Fiber, DSL, etc.) |
| `Payment Method` | How the customer pays |
| `Satisfaction Score` | Customer satisfaction rating |
---

## 🔍 Project Workflow

### 1. 📥 Data Import & Exploration
- Loaded and inspected dataset shape, column types, and summary statistics
- Identified missing values in `Offer` and `Internet Type` columns

### 2. 🧹 Data Cleaning
- Filled missing `Offer` values with `"No Offer"`
- Filled missing `Internet Type` values with `"Unknown"`
- Dropped leakage columns: `Churn Category`, `Churn Reason`
- Calculated overall **churn rate**

### 3. 📈 Exploratory Data Analysis (EDA)
Analyzed customer behavior through multiple visualizations:
- Gender & Senior Citizen distribution
- Age, Tenure, Monthly Charges, Total Charges distributions
- Tenure vs Churn and Monthly Charge vs Churn (boxplots)
- Contract Type, Payment Method, Gender vs Churn (crosstabs)
- Correlation heatmap of numerical features

### 4. ⚙️ Feature Engineering
- Encoded binary Yes/No columns to 1/0
- Applied one-hot encoding to remaining categorical columns
- Removed leakage/ID columns: `Customer ID`, `Churn Score`, 
  `Satisfaction Score`, etc.
- Performed full sanity checks before modeling

### 5. 🤖 Machine Learning Models
Trained and evaluated **3 classification models:**

| Model | Notes |
|---|---|
| Logistic Regression | Baseline linear model |
| Random Forest | Ensemble model (200 estimators) |
| XGBoost | Gradient boosting (300 estimators, lr=0.05) |

### 6. 📉 Model Evaluation
- Accuracy Score
- Classification Report (Precision, Recall, F1-Score)
- Confusion Matrix
- **ROC-AUC Score** for all 3 models
- **Precision-Recall Curve** (XGBoost)
- **Feature Importance** — Top 20 features driving churn (XGBoost)

---

## 🛠️ Tools & Libraries

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-189FDD?style=for-the-badge)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge)
![Seaborn](https://img.shields.io/badge/Seaborn-4C8CBF?style=for-the-badge)

- **Python** — Core programming language
- **Pandas & NumPy** — Data manipulation
- **Matplotlib & Seaborn** — Data visualization
- **Scikit-learn** — ML models, train/test split, evaluation metrics
- **XGBoost** — Gradient boosting classifier

---

## 📁 Repository Structure


---

## 💡 Key Insights
- Customers on **month-to-month contracts** show significantly higher 
  churn rates
- **Higher monthly charges** are associated with increased churn
- **Shorter tenure** customers are more likely to churn
- XGBoost outperformed Logistic Regression and Random Forest based 
  on ROC-AUC score

---

## 🚀 How to Run
1. Clone this repository
2. Install dependencies:
```bash
   pip install pandas numpy matplotlib seaborn scikit-learn xgboost
```
3. Place `telco.csv` in the same folder as the notebook
4. Open `Telco_Customer_Churn_Analysis.ipynb` in Jupyter Notebook or 
   VS Code and run all cells

---

## 👩‍💻 Author
**Krupali Patel**  
Business Insights & Analytics Graduate — Humber College, Toronto  
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Krupali%20Patel-0077B5?style=flat&logo=linkedin)](https://www.linkedin.com/in/krupalippatel)
