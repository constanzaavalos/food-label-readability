# 🏷️ Food Label Readability: Cross-Sectional Analysis

[![Language](https://img.shields.io/badge/Language-R-276DC3.svg)](https://www.r-project.org/)
[![Dataset](https://img.shields.io/badge/Dataset-Food_&_You_Survey-blue.svg)](#)
[![Models](https://img.shields.io/badge/Models-Ordinal_Logistic_Regression-lightgrey.svg)](#)
[![Status](https://img.shields.io/badge/Status-Published-success.svg)](#)

> **Executive Summary:** This repository provides the data and deep statistical modeling used to examine the cross-sectional relationships between perceived multiple traffic light (MTL) legibility and self-reported processed food consumption frequency within the UK.

## 🌍 Why This Matters
* **Nutritional Policy Making:** Validates whether the readability of front-of-pack labels (like the MTL system) actually correlates with healthier consumer dietary patterns.
* **Health Equity:** Evaluates complex stratifications across demographics, addressing whether label readability caters equally to varying levels of household income and education.
* **Large-Scale Validation:** Utilizes massive multi-year survey datasets to draw broader, national-level dietary conclusions rather than localized experiments.

## 📊 Dataset
The analysis is driven by robust, multi-wave multi-year data. 
- **Source:** Food and You Survey 2010-2018 (Waves 1-5).
- **Features:** Label Readability scale, pre-cooked meat consumption, sandwich consumption, dairy intake, and extensive demographic control variables.
- **Data File:** `foodandyou_survey_data.csv`

## 🔬 Methodology Pipeline

`Survey Weight Adjustments` ➔ `Variable Imputation & Recoding` ➔ `Multicollinearity Validation (VIF)` ➔ `Proportional Odds Checks (Brant)` ➔ `Ordinal Logistic Regression`

## 🤖 Models & Analysis Benchmarked
| Analytical Method | Purpose in Study |
| :--- | :--- |
| **Variance Inflation Factor (VIF)** | To detect and remove severe multicollinearity among the demographic and consumption predictors. |
| **Brant Test** | To definitively validate the proportional odds assumption (parallel regression) necessary for ordinal models across waves. |
| **Ordinal Logistic Regression** | The core model used to calculate the log-odds and marginal effects of readability on food frequency. |

## 🚀 How to Run Locally

### 1. Prerequisites
Ensure you have **R or RStudio** alongside a suite of statistical modeling packages:
```R
install.packages(c("tidyverse", "plm", "car", "gplots", "tseries", "lmtest", "readr", "texreg", "ordinal", "VGAM", "survey", "foreign", "MASS", "Hmisc", "reshape2", "brant", "ggplot2", "patchwork"))
```

### 2. Execution
1. Clone the repository locally.
2. Open `label_readability_analysis.Rmd` in your preferred R editor.
3. Adjust the file paths in the initial `data` code chunk to point to `foodandyou_survey_data.csv` in your cloned directory.
4. Execute the chunks sequentially, or click **Knit** to dynamically process the complex variance structures and generate the final publication-ready odds-ratio plots.

## 📁 Project Structure
The repository is purposefully flat to house the interwoven pipeline:
* `label_readability_analysis.Rmd` — The main analysis script detailing the full methodological pipeline.
* `foodandyou_survey_data.csv` — The combined mult-wave survey baseline data.

## 📄 Citation
If you use this code or dataset in your research, please cite the original paper:

> Avalos Valdebenito, C., Shryane, N., & Wang, Y. (2026). Food Label Readability and Consumption Frequency: Isolating Content-Specific Effects via a Non-Equivalent Dependent Variable Design. *Nutrients*, *18*(2), 197. https://doi.org/10.3390/nu18020197

---
👤 **Author**: Constanza Avalos-Valdebenito
