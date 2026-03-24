# Food Label Readability: Cross-sectional Analysis
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)

The scope of this repository is to provide the data and statistical models used to examine cross-sectional relationships between perceived multiple traffic light (MTL) legibility and self-reported processed food consumption frequency in the UK.

Conceptually, the analysis is driven by data from the **Food and You Survey 2010-2018** and is split into the following methodological components:
1. **Survey Weight Adjustment and Imputation**
2. **Multicollinearity Checks (VIF tests)**
3. **Ordinal Logistic Regression Modeling**
4. **Brant Test (Proportional Odds Assumption Validation)**

## Repository Structure

The current version of this repository contains:
- `Food label readability 14052025 - V7 Ordinal Logistics Regression + Weights - editorscomments.Rmd`: The main analysis script detailing the full methodological pipeline.
- `foodandyou-w1_5combined_FSA_Correctedseeking (1).csv`: The combined Food and You Survey dataset.
- `nutrients-18-00197-v2.pdf`: The published academic paper.

## Setup R Environment

Before running the analysis code, please set up an R environment capable of processing complex variance structures and ordinal models. 

### Installing Dependencies

Open R or RStudio and run:

```r
install.packages(c("tidyverse", "plm", "car", "gplots", "tseries", "lmtest", "readr", "texreg", "ordinal", "VGAM", "survey", "foreign", "MASS", "Hmisc", "reshape2", "brant", "ggplot2", "patchwork"))
```

## Steps for running the models

1. Clone this GitHub repository locally.
```bash
git clone https://github.com/constanzaavalos/<Repository_Name>
cd <Repository_Name>
```

2. Open the `.Rmd` file in RStudio or your preferred code editor.
3. Adjust the file paths in the `data` code chunk to correctly point to the downloaded CSV file in your local directory.
4. We recommend executing chunks sequentially from start to finish, or clicking `Knit` in RStudio, to accurately replicate the descriptive tables and the final ordinal logistic regression plots shown in the paper.
