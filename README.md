# Exploratory Data Analysis & Data Preprocessing Pipeline

An end-to-end data cleaning, wrangling, and exploratory analysis pipeline in Python using Pandas, NumPy, Matplotlib, and Seaborn to prepare raw structured data for production-grade machine learning models.

---

## 📌 Project Overview
Raw real-world datasets often contain missing values, inconsistent formats, skewed outliers, and unencoded categorical labels. This project demonstrates a systematic data wrangling methodology that:
1. Audits and resolves missing and irregular records across continuous and categorical fields.
2. Normalizes skewed continuous features and handles outliers via statistical boundaries (IQR).
3. Engineers high-signal composite variables and dummy-encodes text categories.
4. Generates stakeholder-facing exploratory visualizations uncovering demographic and outcome drivers.

---

## ⚙️ Data Preprocessing Workflow
* **Missing Value Imputation:** 
  * Imputed median values for skewed numerical distributions (`Age`) to avoid mean-bias.
  * Applied mode imputation for discrete category attributes (`Embarked`).
  * Pruned sparse attributes exhibiting $>70\%$ missingness (`Cabin`).
* **Outlier Capping:** Applied Interquartile Range ($1.5 \times \text{IQR}$) thresholds to continuous financial metrics (`Fare`) to suppress long-tail distortion without discarding data.
* **Feature Engineering:** Extracted demographic titles from strings and generated a unified `FamilySize` metric.
* **Categorical Encoding:** Applied one-hot dummy encoding across discrete categories to produce a zero-null numerical matrix ready for modeling.

---

## 📊 Key Results & Insights
* **Data Cleansing:** Reduced missing and inconsistent data entries by **100%**, moving from 866 initial null cells across the dataset to 0 nulls across all final model features.
* **Demographic Patterns:** Uncovered that female passengers experienced a $>74\%$ survival rate compared to $<19\%$ for males.
* **Economic Stratification:** First-class passengers showed a $>60\%$ survival rate, more than double that of third-class passengers ($<25\%$).

---

## 🛠️ Tech Stack
* **Language:** Python
* **Data Wrangling:** Pandas, NumPy
* **Data Visualization:** Seaborn, Matplotlib

---
pip install pandas numpy matplotlib seaborn
python eda_data_preprocessing.py

## 🚀 How to Run Locally

1. Clone this repository:
```bash
git clone [https://github.com/Mohd-Adil-21/data-preprocessing-eda.git](https://github.com/Mohd-Adil-21/data-preprocessing-eda.git)
cd data-preprocessing-eda
