# 🛒 A/B Testing for E-commerce Landing Page

## 📌 Project Overview
This project analyzes an A/B test conducted on an e-commerce platform to evaluate whether a new landing page design improves conversion rates compared to the old page.  
Using a dataset of ~290k users, we applied statistical hypothesis testing to determine if the observed differences in conversion were statistically significant.  

The project demonstrates the end-to-end process of **data cleaning, exploratory analysis, hypothesis testing, and business decision-making**.

---

## 🎯 Objectives
- Compare **conversion rates** between control (old page) and treatment (new page) groups.  
- Conduct **statistical hypothesis tests** (Z-test and Chi-square test) to determine if the new design performs better.  
- Provide **data-driven recommendations** to guide product decisions.  

---

## 📊 Steps & Methodology

### 1. Data Cleaning & Preparation
- Merged user dataset with landing page dataset.  
- Checked and removed duplicate user IDs.  
- Validated that control group users landed on the old page and treatment group users on the new page.  
- Final dataset contained ~290k unique users.  

### 2. Exploratory Analysis
- **Overall conversion rate:** ~12%  
- **Group-wise conversion:**  
  - Control (old page) → ~12.0%  
  - Treatment (new page) → ~12.1%  
- Initial observation: conversion rates between groups are very similar.  

### 3. Hypothesis Testing
- **Null Hypothesis (H₀):** The new landing page does not improve conversion (p_control = p_treatment).  
- **Alternative Hypothesis (H₁):** The new landing page improves conversion (p_treatment > p_control).  

#### Z-test
- Z-statistic = **1.29**  
- p-value = **0.195** (> 0.05)  
- Result: Fail to reject H₀  

#### Chi-square test
- Chi-square statistic = **1.66**  
- p-value = **0.197** (> 0.05)  
- Result: Fail to reject H₀  

---

## ✅ Key Findings
- Conversion rates for old vs new landing page are nearly identical.  
- Both Z-test and Chi-square test indicate **no statistically significant improvement** from the new design.  
- Small observed differences are likely due to **random chance**.  

---

## 📌 Recommendation
- Stick with the **old landing page**, as the new design does not show measurable gains in conversion.  
- Redirect product & engineering efforts to **other areas of optimization**, such as checkout flow improvements or personalization strategies.  

---

## 🗂️ Dataset Description
The dataset used in this project is a publicly available A/B testing dataset from Kaggle.  

It contains the following key columns:  

- **user_id** → Unique identifier for each user.  
- **timestamp** → Date and time when the user visited the page.  
- **group** → Indicates whether the user was in the **control group** (saw the old page) or **treatment group** (saw the new page).  
- **landing_page** → Which page the user actually landed on (old_page or new_page).  
- **converted** → Binary variable (0/1) showing whether the user completed the desired action (conversion).  
- **country** (in a supplementary dataset) → User’s country, useful for segmentation analysis.  

📌 Why these matter:  
- `group` and `landing_page` help validate correct random assignment.  
- `converted` is the **key outcome metric** to measure success.  
- `timestamp` allows analysis of daily/temporal patterns.  
- `country` enables breakdown by geography.  

---

## 🛠️ Tools & Libraries
- **Python**: pandas, numpy, scipy, matplotlib, seaborn  
- **Jupyter Notebook** for analysis and visualization  
- **Statistical Testing**: Z-test, Chi-square test  

---


