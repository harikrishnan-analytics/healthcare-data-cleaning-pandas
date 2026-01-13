🧼 End-to-End Data Cleaning with Pandas (Healthcare Dataset)
📌 Project Overview

This project demonstrates a complete, real-world data cleaning workflow using a complex healthcare dataset:
Diabetes 130-US Hospitals Readmission Dataset.

The focus is not just on applying Pandas functions, but on making defensible, domain-aware decisions at every stage of the cleaning process — exactly how data cleaning is done in professional analytics and data science roles.

🎯 Objective

To transform a raw, messy healthcare dataset into an analysis-ready, bias-aware dataset suitable for:

Exploratory Data Analysis (EDA)

Predictive modeling (e.g., readmission risk)

Portfolio demonstration of intermediate–advanced Pandas skills

📂 Repository Contents
├── Data_cleaning_github_ready.ipynb
├── README.md


Data_cleaning_github_ready.ipynb
The main notebook containing the full data cleaning workflow with detailed reasoning and explanations.

🧠 Key Concepts Demonstrated

This notebook goes beyond basic cleaning and highlights how analysts actually think about messy data.

🔍 1. Inspect Before Cleaning

Structural inspection (info, describe)

Layered inspection of categorical and numeric columns

Understanding what each column means, not just its datatype

❓ 2. Missing Data Strategy

Differentiation between:

Encoded missing values ("?", "Unknown/Invalid")

True missing values (NaN)

Clear distinction between:

Random missingness

Systematic missingness

Avoidance of blind imputation

🗑️ 3. Defensible Column Dropping

Example: weight

Clinically important

But dropped due to extreme, systematic missingness

Emphasis on bias reduction over variable importance

🔄 4. Correct Data Type Reclassification

Conversion of:

Age → ordered categorical

Administrative ID columns → categorical

Avoidance of treating codes as numeric quantities

💊 5. Medication Feature Engineering

Instead of using 20+ raw medication columns, the notebook engineers:

num_active_meds

num_med_changes

num_med_up

num_med_down

any_med_change

on_insulin

This reduces dimensionality while preserving clinical signal.

🎯 6. Outcome Variable Preparation

Preservation of original 3-class outcome (readmitted)

Creation of a derived binary target:

readmitted_30d (30-day readmission indicator)

Explicit, documented assumptions

✅ 7. Final Data Validation

Missingness verification

Range and logic checks

Outcome integrity checks

Confirmation that all remaining NaNs are intentional

🧪 Tools & Libraries Used

Python

Pandas

NumPy

Jupyter Notebook

No modeling libraries were used — this project focuses purely on data preparation quality.

🚫 What This Project Intentionally Avoids

Blind fillna() operations

Fabricating clinical values

Over-cleaning or over-engineering

Treating extreme but valid values as outliers

Treating data cleaning as a mechanical task

🏁 Final Outcome

The final dataset is:

Structurally clean

Semantically honest

Bias-aware

Ready for EDA or machine learning

Most importantly, the notebook documents why each decision was made — making it suitable for code review, interviews, and real-world reuse.
