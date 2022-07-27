# Salary machine learning model
A machine learning model that  **estimates salary of data scientist**

## Overview

The machine learning model implemented by Jupyter to estimate data scientists' salaries based on features such as ratings, company establishment, etc. Design features from the text of each job description to quantify the value of the company to python, excel, tableau and SQL

## How will this project help?
• This project **helps data scientist/analyst to negotiate their income for an existing or a new job**

## Installation
* Requires Python running version 3.6 or higher
* Install jupyter package `pip install jupyter`


## Resources Used
• Packages: **pandas, numpy, sklearn, matplotlib, seaborn.**<br/>
• Dataset by **Ken Jee**: https://github.com/PlayingNumbers/ds_salary_proj

## Exploratory Data Analysis (EDA) and Data Cleaning
• **Removed unwanted columns**: 'Unnamed: 0'<br/>
• **Plotted bar graphs and count plots** for numerical and categorical features respectively for EDA<br/>
• **Numerical Features** (Rating, Founded): **Replaced NaN or -1 values with mean or median based on their distribution**<br/>
![rating](rating.png) ![rating1](rating1.png)<br/>
• **Categorical Features: Replaced NaN or -1 values with 'Other'/'Unknown' category**<br/>
• **Removed unwanted alphabet/special characters from Salary feature**<br/>
• **Converted the Salary column into one scale** i.e. from (per hour, per annum, employer-provided salary) to (per annum)

## Feature Engineering
• **Creating new features** from existing features e.g. **job_in_headquaters from (job_location, headquarters)**, etc.<br/>
![jih](jih.png)<br/>
• Trimming columns i.e., **Trimming features having more than 10 categories to reduce the dimensionality**<br/>
• **Handling ordinal and nominal categorical features**<br/>
• Feature Selection using **information gain (mutual_info_regression) and correlation matrix**<br/>

![infogain](infogain.png)<br/>
![corr1](corr1.png)<br/>
• Feature Scaling using **StandardScalar**

## Model Building and Evaluation
Metric: Negative Root Mean Squared Error (NRMSE)<br/>
• Multiple Linear Regression: -27.523<br/>
• Lasso Regression: -27.993<br/>
• **Random Forest: -17.637**<br/>
• Gradient Boosting: -24.429<br/>
• Voting (Random Forest + Gradient Boosting): -19.136<br/>
_**Note: Evaluation scores are obtained using  cross-validation.**_

## Model Prediction
![Prediction](predict.PNG)
