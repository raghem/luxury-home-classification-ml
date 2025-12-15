# Luxury Home Classification Using Logistic Regression

## Author
**Raghe Mahamud**  
Course: D600 – Task 2  
Instructor: Eric Straw  

---

## Project Overview
This project uses **multiple logistic regression** to determine whether a house can be classified as **luxury** based on **square footage** and **number of bedrooms**. The model evaluates how well these variables predict luxury status and how incremental increases affect classification probability.

---

## Research Question
**Are square footage and number of bedrooms accurate predictors of whether a house is classified as luxury?**

If so:
- How accurate is the prediction?
- How do increases in square footage and bedrooms affect luxury classification?

---

## Objective
The goal is to quantify how well square footage and number of bedrooms predict luxury home status.  
In a real estate or construction context, this model could:
- Identify high-value homes early
- Assist with pricing and commission strategy
- Guide luxury-focused development decisions

---

## Data & Variables

### Dependent Variable
- **IsLuxury** (binary: 1 = luxury, 0 = non-luxury)

### Independent Variables
- **Square Footage**
- **Number of Bedrooms**

These features were selected for simplicity and because they are universally available and strongly associated with luxury housing.

---

## Exploratory Data Analysis

### Descriptive Statistics
- Luxury status is categorical
- Square footage is right-skewed
- Number of bedrooms follows a near-normal distribution

### Visualizations
- Univariate plots for luxury status, square footage, and bedrooms
- Bivariate plots show:
  - Luxury homes tend to have more bedrooms
  - Larger square footage increases likelihood of luxury classification

---

## Model Development

### Data Split
- **80% training / 20% testing**
- CSV files retained for reproducibility

### Optimization Method
**Backward Stepwise Elimination**
- Removed predictors with p-values > 0.05
- Both predictors remained in the final model
- Confirms square footage and bedrooms are statistically significant

---

## Model Performance

### Accuracy
- **Training Accuracy:** 71%
- **Test Accuracy:** 71%

Minimal difference indicates good generalization.

### Confusion Matrix (Test Set)
- [[521 161]
- [239 479]]


After scaling for comparison, training and test matrices showed similar distributions, confirming model stability.

---

## Assumptions & Verification

- **No Multicollinearity:** VIF ≈ 1 for both predictors
- **Categorical Outcome:** Luxury variable is binary (0/1)
- **Independence:** No duplicate or dependent observations
- **Sample Size:** ~7,000 rows (well above minimum)

All logistic regression assumptions were satisfied.

---

## Final Model Equation

\[
Luxury = -4.29 + 0.0021(\text{Square Footage}) + 0.7134(\text{Bedrooms})
\]

### Interpretation
- Each additional square foot increases log-odds of luxury by **0.0021**
- Each additional bedroom increases log-odds of luxury by **0.7134**
- Bedrooms have a stronger effect than square footage

---

## Results & Recommendations
- Square footage and bedrooms are meaningful predictors
- 71% accuracy indicates other variables also matter

### Recommended Improvements
- Add variables such as:
  - Price
  - Bathrooms
  - Crime rate
  - Renovations
  - Location features

### Practical Use
This model is useful for:
- Predicting luxury status during design/build phases
- Evaluating renovation impact
- Estimating commission potential

---

## Tools & Libraries
- **Pandas** – data handling
- **Seaborn** – visualization
- **Matplotlib** – plotting
- **NumPy** – array operations
- **Statsmodels** – logistic regression & VIF
- **Scikit-learn** – train/test split, metrics

---

## Sources
No sources were used beyond official WGU course materials.




## Related Projects
- [Home Value Prediction (Regression)](https://github.com/raghem/home-value-prediction-ml)
- [Luxury Home Classification (Logistic Regression)](https://github.com/raghem/luxury-home-classification-ml)
