# MSCS 634 – Project Deliverable 2  
## Regression Modeling and Performance Evaluation  

### Student Name: Nishan Pathak
### Course: Advanced Big Data and Data Mining  

---

## Project Overview

The objective of this deliverable is to build regression models to predict a continuous target variable using customer behavior data. This phase focuses on feature engineering, model development, evaluation, and assessing model performance using cross-validation.

---

## Dataset Description

The dataset used in this project is the **Customer Personality Analysis** dataset. It contains demographic and purchasing behavior information for customers, including income, product spending, and interaction metrics.

The dataset is suitable for regression analysis as it includes several continuous variables that can be used to predict customer income.

---

## Data Preparation and Feature Engineering

Basic data cleaning steps were performed, including:
- Handling missing values in the **Income** column using median imputation  
- Removing duplicate records  

Several new features were created to improve model performance:
- **Age**: derived from Year_Birth  
- **Total_Spending**: total spending across all product categories  
- **Children**: total number of children and teenagers in the household  

These features help better represent customer behavior and simplify the dataset.

---

## Models Implemented

Two regression models were developed:

- **Linear Regression**: Used as a baseline model  
- **Ridge Regression**: Used to address potential multicollinearity and improve model stability  

---

## Model Evaluation

The models were evaluated using the following metrics:
- R² (coefficient of determination)  
- Mean Squared Error (MSE)  
- Root Mean Squared Error (RMSE)  

### Results Summary

- Both models achieved similar performance with an R² score of approximately **0.77**, indicating strong predictive capability  
- RMSE values (~9970) suggest a moderate prediction error  
- Ridge Regression did not significantly improve performance over Linear Regression  

---

## Cross-Validation

5-fold cross-validation was performed to evaluate model generalization.

- The average cross-validation R² score (~0.65) was lower than the test R²  
- This indicates some variability in performance across different data splits  
- One fold showed a lower score, suggesting possible data variability or outliers  

Overall, the models demonstrate stable but slightly variable performance across different subsets of data.

---

## Visualizations

The following visualizations were used to support model evaluation:

- Bar charts comparing model performance (R² and RMSE)  
- Scatter plot of actual vs predicted values for Linear Regression  

These visualizations help illustrate model accuracy and prediction patterns.

---

## Key Insights

- Customer spending behavior is strongly related to income  
- Feature engineering (Total_Spending and Children) improved model effectiveness  
- Linear Regression performed as well as Ridge Regression, indicating minimal multicollinearity  
- The model performs well overall but shows some variability in cross-validation  

---

## Challenges and Limitations

- Presence of outliers may impact prediction accuracy  
- Some variability across cross-validation folds suggests the model may not generalize equally well to all subsets of data  
- Additional feature engineering or more advanced models could further improve performance  

---

## Conclusion

The regression models developed in this deliverable successfully predict customer income with strong accuracy. While both Linear and Ridge Regression performed similarly, Linear Regression is sufficient due to its simplicity.

Future improvements could include testing more advanced regression techniques and incorporating additional feature transformations.
