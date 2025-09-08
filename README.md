# Diabetes Risk Score Regression – Feature Engineering 

##  Overview
This project extends the **scikit-learn diabetes dataset** to explore the impact of **derived features** on regression modeling of the diabetes risk score.  
The task demonstrates how **feature engineering** (interactions and nonlinear transformations) can improve model predictions compared to using only the original features.

## Objectives
1. Load and explore the diabetes dataset from scikit-learn.  
2. Create **three derived features**:
   - `bmi_bp` = BMI × Blood Pressure → captures the **combined effect of obesity and hypertension**.  
   - `age_squared` = Age² → models the **nonlinear effect of age** on diabetes risk.  
   - `age_bmi` = Age × BMI → captures how the **impact of obesity varies across different ages**.  
3. Train two regression models:
   - **Baseline model:** Original 10 features only.  
   - **Engineered model:** Original + derived features (13 total).  
4. Evaluate and compare the models using:
   - **R² (coefficient of determination)**  
   - **Mean Squared Error (MSE)**  
   - **5-fold Cross-validation**  

## Results
- **Hold-out test set (20% split):**
  - Baseline R² = 0.45, MSE ≈ 2900  
  - With derived features R² = 0.49, MSE ≈ 2728  

- **5-fold Cross-validation:**
  - Baseline mean R² = 0.48  
  - With derived features mean R² = 0.49  

The engineered model consistently performed better, showing that derived features add predictive value.

##  How to Run
1. Install requirements:
   ```bash
   pip install scikit-learn pandas numpy
Open the Jupyter notebook diabetes_regression.ipynb.
Run all cells to reproduce the results.
