# Loan Approval Prediction System

A data analytics and machine learning solution designed to evaluate loan applicants' eligibility based on key demographic, financial, and credit history attributes.

## Table of Contents
- [Overview](#overview)
- [Dataset Architecture](#dataset-architecture)
- [Features & Workflow](#features--workflow)
- [Installation & Setup](#installation--setup)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Technologies Used](#technologies-used)

---

## Overview
Loan qualification assessment is a critical process for financial institutions. This project analyzes loan applicant datasets to clean incomplete records, execute statistical exploratory data analysis, and establish target distributions for approval classifications (`Loan_Approved`).

---

## Dataset Architecture

The dataset (`loan_approval_data.csv`) contains **1,000 records** across **20 feature columns**[cite: 5]:

| Feature Name | Data Type | Description |
| :--- | :--- | :--- |
| `Applicant_ID` | Numerical | Unique identifier for each applicant[cite: 5] |
| `Applicant_Income` | Numerical | Primary income of the applicant[cite: 5] |
| `Coapplicant_Income` | Numerical | Additional income from a co-applicant[cite: 5] |
| `Employment_Status` | Categorical | Employment state (e.g., Employed, Self-Employed)[cite: 5] |
| `Age` | Numerical | Age of the applicant in years[cite: 5] |
| `Marital_Status` | Categorical | Marital status of the applicant[cite: 5] |
| `Dependents` | Numerical | Number of dependent family members[cite: 5] |
| `Credit_Score` | Numerical | Applicant credit score[cite: 5] |
| `Existing_Loans` | Numerical | Number of active existing loans[cite: 5] |
| `DTI_Ratio` | Numerical | Debt-to-Income ratio[cite: 5] |
| `Savings` | Numerical | Total savings amount[cite: 5] |
| `Collateral_Value` | Numerical | Total asset/collateral evaluation value[cite: 5] |
| `Loan_Amount` | Numerical | Requested loan amount[cite: 5] |
| `Loan_Term` | Numerical | Duration of the loan (in months)[cite: 5] |
| `Loan_Purpose` | Categorical | Purpose for requesting the loan[cite: 5] |
| `Property_Area` | Categorical | Location type of the property[cite: 5] |
| `Education_Level` | Categorical | Highest educational qualification[cite: 5] |
| `Gender` | Categorical | Gender of the applicant[cite: 5] |
| `Employer_Category` | Categorical | Employer type/sector[cite: 5] |
| `Loan_Approved` | Categorical | Target Variable (`Yes` / `No`)[cite: 5] |

---

## Features & Workflow

1. **Data Ingestion & Inspection:** 
   - Load raw dataset and display summary statistics (`info()`, `describe()`)[cite: 5].
2. **Missing Value Handling:**
   - **Numerical Features:** Imputed missing values using `SimpleImputer` with the **mean** strategy[cite: 5].
   - **Categorical Features:** Imputed missing values using `SimpleImputer` with the **most frequent (mode)** strategy[cite: 5].
3. **Exploratory Data Analysis (EDA):**
   - Class balance visualization for the target `Loan_Approved` variable[cite: 5].

---

## Exploratory Data Analysis (EDA)

Analysis of the target variable `Loan_Approved` reveals a distribution between approved and rejected applications[cite: 5]:

- **Rejected (`No`):** 72.2% (722 instances)[cite: 5]
- **Approved (`Yes`):** 27.8% (278 instances)[cite: 5]

---

## Installation & Setup

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/your-username/loan-approval-prediction.git
   cd loan-approval-prediction

Install Required Libraries: pip install pandas numpy seaborn matplotlib scikit-learn

Run the Notebook:
Launch Jupyter Notebook and execute the analysis file:
jupyter notebook loan_approval_analysis.ipynb