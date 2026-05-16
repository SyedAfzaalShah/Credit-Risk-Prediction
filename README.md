# Credit Risk Prediction

A machine learning project that predicts whether a loan application will be approved or rejected based on applicant details and financial history. Two classification models, Logistic Regression and Decision Tree, are trained, evaluated, and compared.

---

## Project Overview

Credit risk assessment is a core task in the banking and finance industry. This project builds a complete ML pipeline from raw loan data to model evaluation to predict loan approval outcomes, helping financial institutions make better lending decisions.

---

## Project Structure

```
Credit-Risk-Prediction/
│
├── Credit_Risk_Prediction.ipynb   # Main Jupyter Notebook
├── loan_prediction.csv            # Dataset (input)
└── README.md
```

---

## Workflow

```
Load Data --> Exploratory Data Analysis --> Data Cleaning --> Feature Encoding
    --> Train/Test Split --> Model Training --> Evaluation
```

---

## Dataset

**File:** `loan_prediction.csv`

| Feature | Description |
|---|---|
| Gender | Applicant's gender |
| Married | Marital status of the applicant |
| Dependents | Number of dependents |
| Education | Graduate or Not Graduate |
| Self_Employed | Whether the applicant is self-employed |
| ApplicantIncome | Income of the applicant |
| LoanAmount | Loan amount requested |
| Loan_Amount_Term | Term of the loan in months |
| Credit_History | Credit history — 1 (Good) / 0 (Bad) |
| Property_Area | Urban, Semi-Urban, or Rural |
| Loan_Status | Target variable — Y (Approved) / N (Rejected) |

The Loan_ID column is dropped as it holds no predictive value.

---

## Exploratory Data Analysis

Four visualizations are generated to understand loan approval patterns:

- Loan Amount Distribution — Histogram with KDE
- Education vs Loan Status — Grouped bar chart
- Applicant Income by Loan Status — Box plot
- Credit History vs Loan Status — Grouped bar chart

---

## Data Preprocessing

- Filled missing LoanAmount with median
- Filled missing Loan_Amount_Term and Credit_History with mode
- Filled missing categorical columns (Gender, Married, Dependents, Self_Employed) with mode
- Encoded all categorical features using Label Encoding
- Removed the Loan_ID column

---

## Models Used

| Model | Library |
|---|---|
| Logistic Regression | sklearn.linear_model |
| Decision Tree Classifier | sklearn.tree |

**Train/Test Split:** 80% training and 20% testing with stratification applied.

---

## Evaluation Metrics

Both models are evaluated using the following metrics:

- Accuracy Score
- Confusion Matrix
- Classification Report (Precision, Recall, F1-Score)

---

## Key Insights

- Credit History is the strongest predictor of loan approval
- Applicants with higher income tend to get loans approved more often
- Graduates have a slightly higher loan approval rate than non-graduates

---

## Tech Stack

- Python 3.x
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn

---

## Getting Started

**1. Clone the Repository**

```bash
git clone https://github.com/SyedAfzaalShah/Credit-Risk-Prediction.git
```

**2. Install Dependencies**

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

**3. Add the Dataset**

Place `loan_prediction.csv` in the project root directory.

**4. Run the Notebook**

```bash
jupyter notebook Credit_Risk_Prediction.ipynb
```

---

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.
