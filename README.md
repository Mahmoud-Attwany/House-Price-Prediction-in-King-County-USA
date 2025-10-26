# House Price Prediction in King County, USA  

---

## Overview  
This project predicts house prices in King County, including Seattle, using machine learning models.  
The dataset covers home sales between May 2014 and May 2015.  
The work includes data cleaning, exploratory analysis, model development, and performance evaluation.

---

## Objectives  
- Explore relationships between housing features and sale price  
- Build linear, polynomial, and Ridge regression models  
- Evaluate model performance using R²

---

## Dataset  
**Source:** King County House Sales (public dataset)  
**Records:** 21,613  
**Features:** 21  

**Key Columns:**  
- `price`: prediction target  
- `sqft_living`, `grade`, `bathrooms`, `view`, `waterfront`  
- `lat`, `long`, `zipcode`, `yr_built`, `yr_renovated`

---

## Methods  
1. Replaced missing values in `bedrooms` and `bathrooms` with column means  
2. Explored data using correlation analysis, boxplots, and regression plots  
3. Built and evaluated regression models  
   - Linear Regression (single and multiple features)  
   - Polynomial Regression using a Scikit-learn pipeline  
   - Ridge Regression with regularization  
4. Split data into training (85%) and testing (15%) sets  
5. Evaluated model performance using R² scores  

---

## Key Results  
| Model | Description | R² Score |
|-------|--------------|----------|
| Linear (sqft_living) | Single feature | 0.49 |
| Multiple Linear | 11 features | 0.66 |
| Polynomial Regression | With pipeline | 0.75 |
| Ridge Regression | α = 0.1 | 0.65 |
| Polynomial Ridge | α = 0.1 | 0.70 |

---

## Insights  
- Living area and grade are the strongest predictors of price  
- Waterfront properties sharply increase value  
- Polynomial features capture nonlinear effects and improve accuracy  
- Ridge regularization reduces overfitting and stabilizes predictions  
- Model explains about 70% of price variation  
- Further improvements possible with spatial and economic data  

---

## Tools and Libraries  
- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- Matplotlib  
- Seaborn  

---

## Next Steps  
- Tune Ridge `alpha` using `GridSearchCV`  
- Compare with Lasso and ElasticNet  
- Add neighborhood and location-based features  
- Visualize prediction errors and feature importance  

---

## Author  
**Mahmoud Attwany**
