# Customer Churn Prediction

## Project Overview
This project focuses on predicting customer churn using the Telco Customer Churn dataset.

The goal is to identify customers who are more likely to leave the company by using customer
information such as tenure, contract type, monthly charges, internet service, and payment method.

The project follows a complete Data Science workflow, including data understanding, data cleaning,
exploratory data analysis, data preprocessing, machine learning, model evaluation,
model explainability, and business insights.

## Business Problem
Customer churn is an important business problem because losing customers can affect revenue
and long-term customer relationships.

The objective of this project is to build a machine learning model that can predict whether
a customer is likely to churn.

The predictions can then be used to identify higher-risk customers and support targeted
customer retention activities.

## Dataset
The project uses the Telco Customer Churn dataset.

- Number of customers: 7,043
- Number of columns: 21
- Target variable: `Churn`
- Target classes:
  - `0` → No Churn
  - `1` → Churn

The dataset contains customer information related to demographics, services,
contract details, payment methods, tenure, and charges.

## Tools & Technologies
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook
- VS Code
- Git & GitHub

## Project Workflow
1. Data Understanding
2. Data Cleaning
3. Exploratory Data Analysis
4. Data Preprocessing
5. Model Building
6. Model Evaluation
7. Model Explainability
8. Business Insights
9. Conclusion

## Exploratory Data Analysis
The exploratory data analysis was performed to understand customer churn patterns
and identify important relationships between customer characteristics and churn.

Key observations:

- Overall customer churn rate is approximately 26.54%.
- Month-to-month contract customers have the highest observed churn rate.
- Customers with 0–12 months of tenure have the highest observed churn rate.
- Higher monthly-charge groups show higher observed churn rates than lower-charge groups.
- Customers using electronic check have the highest observed churn rate among payment methods.
- Fiber optic customers have the highest observed churn rate among internet service categories.

These observations were used to better understand the customer segments associated
with churn and to support the later machine learning analysis.

## Machine Learning Models
Two classification models were developed for customer churn prediction:

1. Logistic Regression
2. Random Forest Classifier

The data was split into training and testing sets using an 80/20 split with
stratification to maintain the churn class distribution.

Categorical features were encoded using One-Hot Encoding, while numerical
features were standardized using StandardScaler.

## Model Evaluation
The models were evaluated using classification performance metrics, including
Accuracy, Precision, Recall, F1 Score, and ROC-AUC.

The ROC-AUC results obtained during the project were:

| Model | ROC-AUC |
|---|---:|
| Logistic Regression | 0.8421 |
| Random Forest | 0.8227 |

ROC-AUC was used to evaluate how well the models distinguish between customers
who churn and customers who do not churn.

## Model Explainability
Model explainability was explored using feature importance from the Random Forest
model.

Feature importance was used to understand which transformed customer features
contributed more to the Random Forest predictions.

This helps connect the machine learning results with the customer characteristics
identified during exploratory data analysis.
## Business Insights
The analysis identified several customer segments with higher observed churn rates.

Key business insights:

- Month-to-month contract customers have the highest observed churn rate.
- Customers with shorter tenure, particularly 0–12 months, show higher observed churn.
- Higher monthly-charge groups show higher observed churn rates.
- Electronic check users show the highest observed churn rate among payment methods.
- Fiber optic customers show the highest observed churn rate among internet service categories.

The Logistic Regression model was also used to calculate predicted churn probabilities
for customers in the test set.

Customers with a predicted churn probability of 50% or higher were categorized as
high predicted-risk customers. These customers can be prioritized for targeted
retention activities.

## How to Run the Project

### 1. Clone the repository

```bash
git clone <your-github-repository-url>
cd customer-churn-ai
```

### 2. Create a virtual environment

```bash
python -m venv venv
```

### 3. Activate the virtual environment

```bash
venv\Scripts\activate
```

### 4. Install the required libraries

```bash
pip install -r requirements.txt
```

### 5. Run the notebooks

Open the `notebooks` folder in VS Code and run the notebooks in this order:

1. `01_data_understanding.ipynb`
2. `02_eda.ipynb`
3. `03_feature_engineering.ipynb`
4. `04_Data_Preprocessing.ipynb`
5. `05_model_building.ipynb`
6. `06_model_explainability.ipynb`
7. `07_Business_Insights.ipynb`
8. `08_Conclusion.ipynb`

## Conclusion
This project demonstrates a complete customer churn prediction workflow using
Python and machine learning.

The project covered data understanding, data cleaning, exploratory data analysis,
feature engineering, preprocessing, model building, model evaluation, and
business analysis.

Logistic Regression and Random Forest were used to predict customer churn, while
model explainability and predicted churn probabilities were used to connect the
machine learning results with business insights.

The project demonstrates how customer data can be analyzed and used to support
data-driven customer retention activities.