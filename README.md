# Restaurant Success Analysis in Istanbul

**DSA 210 – Introduction to Data Science | Spring 2026**  
**Elif Kopal**

## Overview

This project analyzes what makes a restaurant successful in Istanbul by examining the effects of **district** and **cuisine type** on restaurant performance. Data was collected from Google Maps across three districts: Kadıköy, Beşiktaş, and Şişli.

**Success score** = `rating × number of reviews`

## Dataset

- 210 restaurants (70 per district — balanced)
- Features: district, cuisine type, rating, number of reviews, price level
- Source: Google Maps (manual collection)

## Methods

- **Exploratory Data Analysis** — distributions, outlier detection, group comparisons
- **Hypothesis Testing** — one-way ANOVA + Kruskal-Wallis for district and cuisine type
- **OLS Regression** — effect of district and cuisine on success score
- **Machine Learning** — binary classification (high/low success) using Logistic Regression, Decision Tree, and Random Forest with train/test split, 5-fold cross-validation, and GridSearchCV hyperparameter tuning

## Key Findings

- District does **not** significantly affect success (ANOVA p = 0.196)
- Cuisine type **does** significantly affect success (ANOVA p < 0.001)
- Tuned Random Forest achieved 70.2% CV accuracy vs 53.3% baseline
- Price level is the strongest predictor in the ML models

## Repository Structure

| File | Description |
|---|---|
| `milestonecode.ipynb` | Full analysis notebook (executed with outputs) |
| `restaurants (1).xlsx` | Dataset |
| `final_report.pdf` | Final project report |
| `updated_proposal.pdf` | Project proposal |

## How to Run

1. Install dependencies: `pip install pandas numpy matplotlib seaborn scipy statsmodels scikit-learn openpyxl`
2. Place `restaurants (1).xlsx` in the same directory as the notebook
3. Open `milestonecode.ipynb` and run all cells
