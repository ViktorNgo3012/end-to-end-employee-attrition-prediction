# End-to-End Employee Attrition Prediction

An end-to-end machine learning project that predicts employee attrition using HR data. This project demonstrates a complete data science workflow, from exploratory data analysis (EDA) and feature engineering through data preprocessing, machine learning model development, hyperparameter tuning, model evaluation, and business interpretation using Python and Scikit-learn.

The project was developed as part of my personal data science portfolio to demonstrate practical machine learning, analytical thinking, and business problem-solving skills using a real-world HR analytics dataset.

---

## Project Highlights

- End-to-end machine learning workflow using Python and Scikit-learn
- Business-focused exploratory data analysis (EDA)
- Feature engineering using existing HR variables
- Data preprocessing using Scikit-learn Pipelines
- Comparison of multiple machine learning classification models
- Hyperparameter tuning using GridSearchCV
- Model evaluation using metrics suitable for imbalanced classification
- Feature importance analysis for business interpretation
- Evidence-based business recommendations and project conclusion

---

## Business Problem

Employee attrition is a significant challenge for organisations because replacing experienced employees can be both costly and time-consuming. Understanding the characteristics associated with employee turnover can help organisations improve workforce planning, employee retention, and talent management strategies.

The objective of this project is to develop a machine learning model capable of predicting employee attrition using historical HR data while demonstrating a complete end-to-end data science workflow.

It is important to note that this project focuses on prediction rather than causal inference. The identified relationships should not be interpreted as evidence that individual variables directly cause employee attrition.

---

## Project Objectives

This project aims to:

- Explore employee data to identify meaningful patterns associated with attrition.
- Perform data cleaning and preprocessing.
- Engineer business-relevant features using existing variables.
- Build and compare multiple machine learning classification models.
- Optimise model performance through hyperparameter tuning.
- Evaluate models using appropriate metrics for an imbalanced dataset.
- Interpret model outputs from a business perspective.
- Demonstrate an end-to-end machine learning workflow suitable for a real-world HR analytics problem.

---

## Dataset

The dataset contains **1,470 employee records** and **35 variables** describing employee demographics, job characteristics, compensation, work history, satisfaction measures, and employee attrition.

The target variable is:

**Attrition**

- Yes
- No

Example variables include:

- Age
- Department
- Job Role
- Monthly Income
- Overtime
- Job Satisfaction
- Work-Life Balance
- Environment Satisfaction
- Years at Company
- Total Working Years
- Stock Option Level
- Distance From Home
- Business Travel
- Education
- Marital Status
- and other HR-related variables.

---

## Project Workflow

The project follows an end-to-end machine learning pipeline:

1. Data Loading
2. Data Quality Assessment
3. Exploratory Data Analysis (EDA)
4. Feature Engineering
5. Data Preprocessing
6. Baseline Model Development
7. Machine Learning Model Development
8. Hyperparameter Tuning
9. Model Comparison
10. Feature Importance Analysis
11. Business Interpretation
12. Project Conclusion

The complete workflow, including all code, visualisations, model development, and business interpretation, is documented in the accompanying Jupyter Notebook.

---

## Exploratory Data Analysis

The exploratory analysis investigated relationships between employee attrition and several important HR variables, including:

- Overtime
- Department
- Job Role
- Monthly Income
- Years at Company
- Job Satisfaction

The analysis focused on identifying meaningful business patterns while avoiding causal conclusions.

---

## Feature Engineering

Several additional business-oriented features were engineered using existing variables in the dataset to improve model interpretability.

All engineered features were created exclusively from existing dataset columns without introducing target leakage.

---

## Data Preprocessing

The preprocessing pipeline includes:

- Median imputation for missing numerical values
- Standardisation of numerical variables
- One-hot encoding of categorical variables

A Scikit-learn Pipeline was implemented to ensure preprocessing was applied consistently throughout model training and evaluation while preventing data leakage.

---

## Machine Learning Models

The following classification models were developed and compared:

- Dummy Classifier (Baseline)
- Logistic Regression
- Decision Tree
- Random Forest
- Support Vector Machine (SVM)

Hyperparameter tuning was performed using **GridSearchCV** with **5-fold cross-validation**.

---

## Model Evaluation

Because employee attrition is an imbalanced classification problem, model performance was evaluated using multiple complementary metrics rather than relying solely on accuracy.

Evaluation metrics include:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC
- Average Precision

Model selection prioritised the **F1-score**, providing a balanced assessment of precision and recall.

Among the evaluated models, the **Support Vector Machine (SVM)** achieved the strongest overall performance based on the F1-score and was selected as the final predictive model.

---

## Feature Importance

Support Vector Machines do not provide feature importance directly.

To improve model interpretability, a Random Forest model was trained separately to estimate the relative importance of predictor variables and support business interpretation.

This additional analysis helps explain which variables contribute most strongly to predictive performance while recognising that feature importance does not imply causation.

---

## Key Findings

The exploratory analysis identified several variables that were associated with higher employee attrition rates, including:

- Employees working overtime exhibited substantially higher attrition rates than employees who did not work overtime.
- Attrition rates varied across different job roles, with Sales Representatives showing the highest observed attrition rate.
- Lower job satisfaction levels were associated with higher observed attrition rates.
- Employees with lower monthly income generally exhibited higher attrition rates.
- Employees with fewer years at the company tended to leave more frequently than longer-serving employees.

These findings represent observed relationships within the dataset and should not be interpreted as causal effects.

---

## Technologies Used

### Programming Language

- Python

### Data Manipulation

- Pandas
- NumPy

### Data Visualisation

- Plotly
- Matplotlib

### Machine Learning

- Scikit-learn

### Development Environment

- Jupyter Notebook

---

## Repository Structure

```text
.
├── employee_attrition_prediction.ipynb
├── HR-Employee-Attrition-A2.csv
├── LICENSE
└── README.md
```

---

## How to Run

### Clone the repository

```bash
git clone https://github.com/ViktorNgo3012/end-to-end-employee-attrition-prediction.git
```

### Install the required libraries

```bash
pip install pandas numpy matplotlib plotly scikit-learn
```

### Open the notebook

```bash
jupyter notebook employee_attrition_prediction.ipynb
```

### Run the project

Run all notebook cells sequentially from top to bottom.

---

## Limitations

This analysis is based on historical employee records from a single dataset.

The identified relationships are observational and should not be interpreted as causal.

The predictive model is intended to support HR decision-making rather than replace human judgement.

Future work could incorporate additional organisational variables, temporal information, external datasets, or explainable AI techniques to further improve predictive performance and model interpretability.

---

## Acknowledgements

This project was developed independently as part of my personal data science portfolio to demonstrate practical skills in exploratory data analysis, machine learning, model evaluation, and business problem solving using Python and Scikit-learn.
