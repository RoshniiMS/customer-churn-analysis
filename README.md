# Telco Customer Churn Prediction  
Machine Learning Project | Logistic Regression Model

This project analyzes customer churn behavior in the telecommunications sector using the popular Telco Customer Churn dataset. The objective was to identify key factors influencing churn and build a predictive model that supports data-driven retention strategies.

---

## Project Overview

Customer churn is a major challenge for subscription-based industries.  
This project focuses on:

- Understanding customer behavior using exploratory data analysis (EDA)  
- Engineering meaningful features for better model performance  
- Comparing multiple classification models  
- Selecting the best model based on performance and interpretability  
- Identifying important drivers of churn to support business decisions  

---

## 📂 Dataset Information

The dataset contains customer demographic details, service usage, billing preferences, and contract information.  
Target variable: **`Churn`** (Yes/No)

Key characteristics:
- ~7,000 customer records  
- 21 original features  
- Contains both numerical and categorical variables  

Dataset source: Kaggle — Telco Customer Churn

---

## Project Workflow

### **1. Data Cleaning**
- Removed duplicate records  
- Converted `TotalCharges` to numerical  
- Encoded categorical variables  
- Standardized numerical features  

### **2. Exploratory Data Analysis (EDA)**
Explored churn distribution, customer demographics, service usage patterns, and billing preferences.  
Identified correlations between tenure, contract type, monthly charges, and churn.

### **3. Feature Engineering**
Created new business-driven features such as:
- `TenureGroup`  
- `NumServices`  
- `AvgMonthlySpend`  
- `SeniorLongTenure`  

These features improved interpretability and added business context.

### **4. Model Building**
The following models were implemented:
- Logistic Regression  
- Random Forest Classifier  
- XGBoost Classifier  

Each model was evaluated using accuracy, precision, recall, and F1-score.

### **5. Model Comparison**
| Model                | Accuracy |
|----------------------|----------|
| Logistic Regression  | ~79–80%  |
| Random Forest        | ~78–79%  |
| XGBoost (baseline)   | ~76–77%  |

Logistic Regression demonstrated the best balance of accuracy and interpretability.

### **6. Final Model Selection**
**Logistic Regression** was selected as the final model due to:
- Strong and consistent performance  
- High interpretability using coefficients  
- Alignment with business requirements for transparent decision-making  

---

## Feature Importance (Logistic Regression)

Top features influencing churn:

- **Tenure**: Short-term customers have higher churn likelihood  
- **Contract type**: Month-to-month contracts increase churn risk  
- **Service type**: Fiber optic users show higher churn tendency  
- **Payment method**: Electronic check users churn more often  
- **Charges**: Higher monthly spending is associated with churn  

A coefficient-magnitude plot was used to visualize the top predictors.


---

##  Business Insights

Based on model insights:

- Customers in their first year are most at risk and need targeted retention programs  
- Encouraging contract upgrades can reduce churn  
- Improving service experience for fiber-optic customers may reduce dissatisfaction  
- Bundling add-on security and support services can improve customer retention  
- Simplifying billing or incentivizing non-electronic payment methods may help reduce churn  

These insights can support data-driven decision-making for telecom providers.

---

##  Technologies Used

- Python  
- Pandas, NumPy  
- Scikit-learn  
- Matplotlib, Seaborn  
- Jupyter Notebook  

---

## 📁 Repository Structure

```
telco-customer-churn-ml/
│
├── README.md
├── requirements.txt
├── .gitignore
│
├── notebooks/
│   └── telco_churn_analysis.ipynb
│
└── data/
    └── Telco-Customer-Churn.csv

```



---

##  Conclusion
This project covers the complete process of building a churn prediction model.
Among all the models tested, Logistic Regression performed well and was the easiest to interpret.
Because it clearly shows which factors influence churn, it’s practical for real business use where companies need simple, explainable insights.

---



