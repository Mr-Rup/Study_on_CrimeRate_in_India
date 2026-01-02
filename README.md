
---

# 📊 Study on Crime Rates in India using Regression Analysis

## 📌 Overview

This repository contains an end-to-end **statistical analysis of crime rates in India**, focusing on **IPC and SLL crimes** and their relationship with key **socio-economic indicators** across Indian states and union territories.

The project applies **multiple linear regression**, **diagnostic testing**, and **model refinement** to examine whether commonly cited economic variables meaningfully explain variations in crime rates.

This work was carried out as part of an **academic dissertation** and emphasizes **statistical rigor over black-box modeling**.

---

## 🎯 Objectives

The primary goals of this study are:

1. **Quantify the relationship** between crime rates and socio-economic indicators such as:

   * Unemployment (rural & urban)
   * GDP and NSDP
   * Inflation (general & food)
2. **Compare IPC vs SLL crime behavior** under identical predictors
3. **Diagnose and correct regression issues**, including:

   * Influential observations
   * Multicollinearity
   * Heteroscedasticity
4. **Identify statistically significant predictors** of crime rates

---

## 📂 Dataset Description

* **Observations:** 33 Indian states & union territories (2021)
* **Response Variables:**

  * `Rate_IPC`: IPC crimes per lakh population
  * `Rate_SLL`: SLL crimes per lakh population
* **Predictor Variables:**

  * Rural unemployment rate
  * Urban unemployment rate
  * Log(GDP)
  * Log(NSDP)
  * General CPI inflation
  * Food CPI inflation
  * Population-based dummy variables

**Data Sources:**

* National Crime Records Bureau (NCRB)
* Reserve Bank of India (RBI)

---

## 🧪 Methodology

The analysis follows a **classical regression pipeline**, not shortcuts.

### 1️⃣ Exploratory Data Analysis

* Scatter plots of each predictor vs response
* Initial visual assessment of linearity and spread

### 2️⃣ Regression Modeling

Two primary models were fitted:

* **Case 1:** IPC crime rate as response
* **Case 2:** SLL crime rate as response

Each model initially included **all predictors jointly**.

---

### 3️⃣ Regression Diagnostics

To ensure validity of inference, the following diagnostics were performed:

* **Influential Point Detection**

  * Standardized residuals
  * Cook’s Distance
* **Multicollinearity**

  * Correlation heatmaps
  * Variance Inflation Factors (VIF)
* **Heteroscedasticity**

  * Residual vs fitted plots
  * Glejser test
  * Goldfeld–Quandt test

Only **statistically justified corrections** were applied.

---

### 4️⃣ Model Refinement

After removing influential observations and redundant predictors:

* Final models reduced to **GDP as the sole significant predictor**
* Separate final regressions for IPC and SLL crimes

---

## 📈 Key Findings

* **GDP is the only statistically significant predictor** (at 10% level) for both IPC and SLL crime rates
* Most commonly assumed predictors (unemployment, inflation) **do not show significance**
* Overall explanatory power of the models remains **limited**

  * Indicates **missing socio-structural variables**
  * Highlights limits of purely economic explanations

👉 This is an *important negative result*, not a failure.

---

## 🧠 Interpretation

This study demonstrates that:

* Crime is **not adequately explained by macro-economic indicators alone**
* Statistical diagnostics matter — naïve regression would lead to misleading conclusions
* There is strong scope for:

  * Micro-level data
  * Policy, policing, education, and demographic variables
  * Panel or time-series extensions

---

## 🛠 Tools & Technologies

* **Language:** R
* **Libraries:**

  * `car`
  * `ggplot2`
  * `reshape2`
* **Statistical Methods:**

  * OLS regression
  * Diagnostic testing
  * Correlation analysis

---

## 📁 Repository Structure

```
├── data/
│   └── regression_data.csv
├── report/
|   ├── Study_on_crime_rate_in_India.docx
│   └── Study_on_crime_rate_in_India.pdf
├── scripts/
│   ├── scatterplot.R
│   ├── regression.R
│   ├── regression_diagnostics.R
│   └── dummy.R
├── LICENSE
└── README.md
```

---

## 📚 References

* Goon, Gupta & Dasgupta — *Fundamentals of Statistics (Vol I & II)*
* NCRB — *Crimes in India 2021*
* RBI — *Handbook of Statistics on Indian States*

---

## 📜 License

This project is licensed under the **MIT License** — see the  
[LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgement

This project was completed under the guidance of Prof. Mausumi Bose, with sincere thanks to her and college for giving me such an opportunity.

---
