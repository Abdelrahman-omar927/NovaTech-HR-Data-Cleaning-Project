# NovaTech-HR-Data-Cleaning-Project
# NovaTech HR Data Cleaning & Analysis

A complete, well-documented data cleaning project delivered as part of a student assignment. The work includes auditing a messy HR dataset, fixing data quality issues, engineering useful features, performing a visual data quality audit in Excel, and compiling quick insights for HR decision-making.

---

## 📁 Repository Structure

```
NovaTech-HR-Data-Cleaning-Project/
│
├── data/
│   ├── NovaTech_HR_Data_Dirty.xlsb        # Original raw data
│   ├── NovaTech_HR_Data_Cleaned.xlsb      # Cleaned and standardized dataset
│
├── docs/
│   ├── Students_Assignment.docx           # Assignment brief
│   ├── Quick_Insights.docx                # Answers to business questions
|                          
└── README.md                               # Project overview & usage
```

> **Note:** Folder names and files are suggestions; adjust to match your final submission.

---

## 🎯 Project Overview

NovaTech Industries, a mid-sized technology firm, is facing rising employee attrition. Before any analysis or modeling can be trusted, the company’s legacy HR export had to be **audited, cleaned, and standardized**. This repository captures that first phase of work and provides a **clean dataset** plus a concise **insights report** for the HR Director.

---

## 🧰 Data
- **Source:** Simulated HR export provided in the assignment.
- **Rows:** ~10,000 employees.
- **Key fields:** `EmployeeID`, `BirthDate`, `HiringDate`, `Department`, `JobRole`, `MonthlyIncome`, `PercentSalaryHike`, `OverTime`, `JobSatisfaction`, `WorkLifeBalance`, `Attrition` and others.

> See `docs/Students_Assignment.docx` for the full data dictionary.

---

## 🔧 Methods & Steps

### 1) Data Cleaning (Excel)
- **Remove duplicates** based on `EmployeeID` (ensure exactly 10,000 unique records).
- **Standardize text** capitalization across categorical columns (e.g., make `sales`, `SALES` → `Sales`).
- **Fix typos** (e.g., correct `Slaes` → `Sales`).
- **Trim leading/trailing spaces** in `JobRole` and other text fields.
- **Normalize currency**: convert `MonthlyIncome` values with `$` or `,` into pure numeric format.

### 2) Feature Engineering
- **`Current_Age`**: derived from `BirthDate` relative to today’s date.
- **`Tenure_Years`**: derived from `HiringDate` relative to today’s date.
- **`Salary_Tier`**: `Tier 1` if `MonthlyIncome > 10000`, else `Standard`.

### 3) Visual Data Quality Audit (Excel)
- **Conditional Formatting**: highlight `JobSatisfaction` of **1 or 2** in red.
- **Data Validation**: restrict `EducationLevel` to one of: `Below College`, `College`, `Bachelor`, `Master`, `Doctor`.

### 4) Quick Insights
- The ten business questions required by the assignment are answered in `docs/Quick_Insights.docx`, using the cleaned dataset.

---

## 📦 Files
- `data/NovaTech_HR_Data_Dirty.xlsb` → the original (unclean) dataset.
- `data/NovaTech_HR_Data_Cleaned.xlsb` → the cleaned, standardized dataset ready for analysis.
- `docs/Students_Assignment.docx` → the original assignment brief and data dictionary.
- `docs/Quick_Insights.docx` → concise answers to the ten HR questions.


---

## 🚀 How to Use

### Clone the repository
```bash
git clone https://github.com/<your-username>/NovaTech-HR-Data-Cleaning-Project.git
cd NovaTech-HR-Data-Cleaning-Project
```

### Explore the data
- Open `data/NovaTech_HR_Data_Cleaned.xlsb` in Excel for immediate analysis.

### Suggested analyses (next phase)
- Attrition drivers by Department / JobRole.
- Tenure vs. Salary and Performance.
- Overtime and Work-Life Balance correlations.

---

## 🛠️ Tools
- **Microsoft Excel**: primary tool for cleaning, feature engineering, and visual audit.
- **(Optional) Python / Jupyter**: for reproducibility and further analysis.

---

## ✅ Results (Summary)
- A clean dataset free of duplicate EmployeeIDs and formatting inconsistencies.
- Standardized categorical values (e.g., departments and job roles).
- Engineered features (`Current_Age`, `Tenure_Years`, `Salary_Tier`) to accelerate analysis.
- Quick insights compiled and answered per assignment requirements.

---


## 📝 Notes
- Dates in the dataset include recent years; all age and tenure calculations were performed relative to the working date at the time of cleaning.
- Some values were intentionally messy (mixed case, typos, currency symbols) to simulate real-world HR exports.

---
