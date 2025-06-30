
---

## 📊 Dataset Overview

**Source**: [Kaggle – Telco Customer Churn](https://www.kaggle.com/blastchar/telco-customer-churn)

- 7043 rows × 21 columns
- Target Variable: `Churn` (Yes/No)
- Features: Demographics (gender, age), services (Internet, Phone), contract type, tenure, charges, etc.

---

## ⚙️ Methodology

### 🔎 1. Exploratory Data Analysis (EDA)
- Handled missing values
- Visualized churn distribution, contract types, charges
- Found important correlations (e.g., contract type, monthly charges)

### 🧹 2. Data Preprocessing
- Categorical encoding (LabelEncoder)
- Feature scaling (StandardScaler)
- Feature engineering (tenure buckets, total services)

### 🧠 3. Model Building
Used multiple classifiers:
- Logistic Regression
- Random Forest ✅ *(best model used)*
- Decision Tree
- XGBoost

**Final Model**: `RandomForestClassifier` (saved as `random_forest_model.joblib`)

### 📈 4. Model Evaluation
- Accuracy: ~82%
- ROC-AUC Score: 0.85
- Confusion matrix and classification report included

---

## 🖥️ Streamlit App

A web interface using Streamlit (`churn_app.py`) allows users to:
- Enter customer details manually
- Get churn prediction in real-time

### ▶️ To Run the App

```bash
# Step 1: Install dependencies
pip install -r requirements.txt

# Step 2: Run Streamlit app
streamlit run churn_app.py
