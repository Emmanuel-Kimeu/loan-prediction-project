# Loan Approval Predictor Report
**Group:** GROUP6

---

## 1. Project Overview
This project focuses on building a machine learning model to predict whether a loan should be approved based on applicant details. A supervised binary classification approach was used, comparing two models: Logistic Regression and a Decision Tree. The project followed a full machine learning lifecycle, from data exploration and preprocessing to model evaluation.

**Tech Stack:**
* Python
* Pandas
* NumPy
* Scikit-learn
* Seaborn
* Matplotlib

---

## 2. Dataset
The data for this project was sourced from the "Loan Approval Dataset" on Kaggle.
* **File Used:** `Loan_train.csv`
* **Target Variable:** `Loan_Status` (Approved = 1, Not Approved = 0)

---

## 3. Methodology

### 3.1 Exploratory Data Analysis (EDA)
The dataset was analyzed to understand its structure and identify patterns.
* Missing values were identified in columns like `Gender`, `Married`, and `LoanAmount`.
* The class balance for the `Loan_Status` target variable was found to be slightly imbalanced.
* Relationships between categorical features and the loan status were visualized.
* Distributions and correlations for numerical features were explored.

### 3.2 Data Preprocessing
To prepare the data for modeling, the following steps were taken:
* **Missing Value Imputation:**
    * Categorical features (e.g., `Gender`, `Married`) were filled using the **mode**.
    * `LoanAmount` was filled using the **mean**.
* The `Dependents` column was converted to an integer format.
* Categorical features were encoded using `LabelEncoder`.
* Numeric features (`ApplicantIncome`, `CoapplicantIncome`, `LoanAmount`) were scaled using `StandardScaler`.

### 3.3 Model Building
* The dataset was split into training and testing sets with an 80-20 ratio.
* Two models were trained:
    1.  **Logistic Regression**
    2.  **Decision Tree Classifier**

---

## 4. Findings and Evaluation

### 4.1 Model Performance
The models were evaluated using accuracy, precision, recall, and F1-score.

| Metric | Logistic Regression | Decision Tree |
|---|---|---|
| **Accuracy** | 0.79 | 0.70 |
| **Precision** | 0.76 | 0.77 |
| **Recall** | 0.99 | 0.78 |
| **F1-Score** | 0.86 | 0.77 |

The Logistic Regression model demonstrated slightly better overall performance.

### 4.2 Feature Importance
According to the Decision Tree model, the most influential features for predicting loan approval were:
* Credit_History
* LoanAmount
* ApplicantIncome
* Education
* Property_Area

---

## 5. Conclusion
Both models performed reasonably well, with Logistic Regression showing a more balanced performance between precision and recall. A key finding is that an applicant's `Credit_History` is a very strong predictor of loan approval outcomes.