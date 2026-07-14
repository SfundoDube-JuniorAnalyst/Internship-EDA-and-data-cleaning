# Titanic Dataset: Exploratory Data Analysis & Data Cleaning

## Project Overview
As part of my internship at **[Company Name]**, this project focuses on performing end-to-end Exploratory Data Analysis (EDA) and data cleaning on the historic Titanic passenger dataset. The goal of this analysis is to clean and preprocess raw, messy passenger records, handle missing values systematically, and uncover the key demographic and socio-economic factors that influenced survival rates.

---

## Technologies & Libraries Used
- **Language:** Python
- **Data Manipulation:** `pandas`, `numpy`
- **Data Visualization:** `seaborn`, `matplotlib`
- **Environment:** Jupyter Notebook

---

## Data Cleaning & Preprocessing
Raw data is rarely perfect. To make this dataset ready for analysis (and eventual machine learning), I executed the following cleaning pipeline:

* **Handling Missing Values:**
    * **`Age`:** Instead of using a simple global mean/median, I imputed missing age values based on the median age of passengers within the same **Class (`Pclass`)** and **Gender (`Sex`)** to ensure historical accuracy.
    * **`Cabin`:** With over 70% of the data missing, I engineered a new feature `Has_Cabin` (binary: 1 if cabin data was present, 0 if missing) to see if having an assigned cabin correlated with survival.
    * **`Embarked`:** Imputed the 2 missing records with the mode ("S" - Southampton).
* **Data Type Corrections:** Converted categories like `Survived`, `Pclass`, and `Embarked` to categorical data types for optimized memory usage and better plotting.
* **Feature Engineering:** Combined `SibSp` (siblings/spouses) and `Parch` (parents/children) to create a new `Family_Size` feature to analyze if traveling alone affected survival rates.

---

## Key Insights from EDA

Through visualization and statistical checks, several strong trends emerged:

1.  **The "Women and Children First" Protocol:** * Female passengers had a dramatically higher survival rate (~74%) compared to male passengers (~19%).
2.  **Socio-Economic Class Matters:**
    * Passengers in 1st Class (`Pclass = 1`) had a survival rate of over 60%, while 3rd Class passengers had a survival rate of under 25%, highlighting a stark disparity.
3.  **Family Dynamics:**
    * Passengers traveling with small families (2 to 4 members) had better survival rates than those traveling entirely alone or with very large families (5+).

---

## How to Run the Project

1. Clone this repository:
   ```bash
   git clone [https://github.com/SfundoDube-JuniorAnalyst/Internship-EDA-and-data-cleaning.git](https://github.com/SfundoDube-JuniorAnalyst/Internship-EDA-and-data-cleaning.git)