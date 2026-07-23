# Loan Default Risk Analysis (Excel)

## Project Overview

This project analyzes a mortgage loan portfolio to identify borrower and loan characteristics associated with higher loan risk. Using Microsoft Excel, the dataset was cleaned, transformed, and analyzed through Pivot Tables, calculated fields, and an interactive dashboard to highlight key lending risk indicators and support data-driven decision making.

---

## Business Problem

Financial institutions need to identify high-risk loan applications before approval to reduce portfolio risk and improve lending decisions.

The objective of this project is to:

- Analyze borrower and loan characteristics associated with loan outcomes.
- Engineer a composite Risk Score using underwriting indicators.
- Segment borrowers into risk tiers.
- Build an interactive Excel dashboard for business users to monitor portfolio risk.

---

## Dataset

**Source:** Loan Default Dataset (Kaggle)

https://www.kaggle.com/datasets/yasserh/loan-default-dataset

**Dataset Summary**

- Records: **148,670**
- Features: **34**
- Year Covered: **2019**
- Data includes:
  - Borrower demographics
  - Loan characteristics
  - Credit information
  - Property information
  - Loan outcome (Status)

---

## Tools & Excel Skills Used

- Microsoft Excel
- Pivot Tables
- Pivot Charts
- Slicers
- Conditional Formatting
- SUMPRODUCT
- IFS
- IF
- COUNTIF
- AVERAGE
- Data Validation

---

## Data Cleaning

The dataset was cleaned before analysis to improve consistency and usability.

Cleaning steps included:

- Handled missing values in:
  - Interest Rate
  - Interest Rate Spread
  - Upfront Charges
  - Property Value
- Replaced missing numerical values using grouped median where appropriate.
- Created missing-value flags where imputation was not suitable.
- Standardized abbreviated categorical values into readable labels.
- Removed unnecessary constant columns.
- Verified duplicate records before analysis.
- Reviewed outliers in LTV, DTI, and Interest Rate.

---

## Feature Engineering

Several business-oriented features were created to improve analysis.

### Credit Score Tier

Borrowers were grouped into:

- Excellent
- Good
- Fair
- Poor

---

### Income Bracket

Income was segmented into:

- Low
- Mid
- High
- Very High

---

### LTV Risk Flag

Loans with:

- **LTV > 90%** were classified as **High LTV**
- Otherwise **Normal**

---

### DTI Risk Flag

Borrowers with:

- **DTI > 43%** were classified as **High Burden**
- Otherwise **Normal**

The 43% threshold reflects a commonly used mortgage underwriting guideline.

---

### Composite Risk Score

A weighted Risk Score was engineered using:

- Credit Score (40%)
- Debt-to-Income Ratio (35%)
- Loan-to-Value Ratio (25%)

Each variable was normalized before weighting to ensure comparability.

---

### Risk Tier

Borrowers were classified as:

- Low Risk
- Medium Risk
- High Risk

based on the engineered Risk Score.

---

## Dashboard

An interactive Excel dashboard was developed using Pivot Tables and Slicers.

Dashboard includes:

- Total Loans Analysed
- Average Default Rate
- Average Loan Amount
- Average Credit Score
- High Risk Loans

Interactive filters:

- Region
- Credit Tier
- Risk Tier
- Loan Purpose
- Gender

Visualizations include:

- Default Rate by Risk Tier
- Default Rate by Income Bracket
- Default Rate by Credit Type
- Default Rate by Region
- Default Rate by Loan Purpose
- Credit Score Tier Distribution

---

## Key Findings

- A total of **148,670** loan applications were analyzed, with an overall default/rejection rate of **24.64%**.

- Borrowers classified as **High Risk** recorded an **18.6%** default/rejection rate compared with **14.0%** for **Low Risk** borrowers, indicating that the engineered Risk Score effectively differentiates borrower risk.

- The **North-East** region recorded the highest default/rejection rate (**30.45%**), while the **North** region recorded the lowest (**22.51%**).

- Borrowers in the **High Income** category showed the highest default/rejection rate (**38.78%**), highlighting an interesting pattern within this dataset.

- Loan Purpose **P2** recorded the highest default/rejection rate (**33.08%**), whereas **P4** recorded the lowest (**22.97%**).

- Applications evaluated through **EQUI** exhibited an unusually high default/rejection rate compared with other credit bureaus, suggesting further investigation is required.

---

## Workbook Structure

| Sheet | Description |
|--------|-------------|
| Raw_Data | Original dataset |
| Cleaned_Data | Cleaned dataset with engineered features |
| Pivot_Tables | Pivot tables supporting the dashboard |
| Dashboard | Interactive dashboard with KPIs and slicers |
| Key_Findings | Business insights from the analysis |

---

## Skills Demonstrated

- Data Cleaning
- Data Transformation
- Feature Engineering
- Financial Risk Analysis
- Exploratory Data Analysis (EDA)
- Dashboard Design
- Business Insight Generation
- Excel Automation using Formulas


---

## Project Outcome

This project demonstrates how Microsoft Excel can be used to perform end-to-end financial data analysis—from data preparation and feature engineering to dashboard development and business insight generation. The resulting dashboard provides a simple and interactive framework for exploring portfolio risk and supporting lending decisions.
