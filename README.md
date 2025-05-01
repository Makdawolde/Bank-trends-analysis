# Bank Trends Analysis

## **Project Overview**
This project analyzes banking deposit trends to identify factors influencing customer behavior. Using a structured approach with data cleaning, visualization, and predictive modeling, we extracted meaningful insights that can help financial institutions optimize their strategies.

## **Workflow & Key Accomplishments**
### **1. Data Processing & Cleaning**
- Imported original dataset (`bank.csv.csv`) and extracted a **random sample of 1,000 entries**.
- Converted categorical variables (e.g., `job`, `education`, `housing`) into **factors** for analysis.
- Checked for missing values using `colSums(is.na(sample_data))`, confirming **no missing data**.
- Saved the cleaned dataset to `processed_bank_data.csv` for reproducibility.

### **2. Exploratory Data Analysis (EDA)**
Generated visualizations to explore patterns in customer banking behaviors:
- **Age Distribution** (`visuals/age_distribution.png`) - Histogram of customer ages.
- **Deposit Trends by Balance** (`visuals/deposit_trend_plot.png`) - Balance vs deposit status.
- **Deposits by Job Type** (`visuals/deposits_by_job.png`) - Deposit success across occupations.
- Additional insights into loan status, housing condition, and campaign effectiveness.

### **3. Predictive Modeling**
- Built a **logistic regression model** to predict deposit success:
  ```r
  logistic_model <- glm(deposit ~ age + balance + campaign + previous + pdays, data = sample_data, family = binomial)
