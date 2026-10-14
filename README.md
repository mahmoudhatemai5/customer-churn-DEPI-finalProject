# Customer Churn 

## => Project Overview

Customer Churn Analysis is a Data Science project that aims to analyze customer behavior, identify the key factors associated with customer churn, and develop machine learning models to predict customers who are likely to leave a service.

The project uses SQL for data management and querying, Python for data cleaning and exploratory data analysis (EDA), and Machine Learning techniques to build and evaluate predictive models.

The ultimate goal is to extract meaningful insights from customer data and provide data-driven recommendations that can help businesses improve customer retention and reduce churn rates.

## => Problem Statement 

Customer churn is a major challenge for businesses, as losing customers can negatively impact revenue, profitability, and long-term growth. Understanding the factors that influence customers to leave a service is essential for improving customer retention.

The main problem addressed in this project is how to analyze customer data to identify patterns and factors associated with churn and determine whether machine learning can help predict customers who are likely to leave.

By using SQL for data analysis and Python for exploratory data analysis and machine learning, this project aims to extract meaningful insights from customer data and support data-driven decisions that can help businesses develop more effective customer retention strategies.

## => Project Objectives

* Analyze customer data to understand churn patterns and behavior.
* Identify factors associated with customer churn.
* Use SQL to query, organize, and analyze customer data.
* Perform Exploratory Data Analysis (EDA) using Python.
* Build and evaluate machine learning models to predict customer churn.
* Extract actionable insights to support customer retention strategies.
* Provide data-driven recommendations to help businesses improve customer retention.

## => Dataset Description

This project uses customer subscription, transaction, and listening activity data to analyze customer churn and identify patterns associated with subscription cancellations.

The dataset consists of five CSV files, each providing a different perspective on customer information and behavior.

### Dataset Files

**1. `members.csv`**

Contains customer registration and demographic information.

Key columns:

* `msno`: Unique customer identifier.
* `city`: Customer's city code.
* `bd`: Customer's age-related field.
* `gender`: Customer's gender.
* `registered_via`: Registration method.
* `registration_init_time`: Customer registration date.

**2. `train_data.csv`**

Contains customer identifiers and the target variable used for churn prediction.

Key columns:

* `msno`: Customer identifier.
* `is_churn`: Indicates whether the customer churned, where `1` represents churn and `0` represents no churn.

**3. `kaggle_test_data.csv`**

Contains customer identifiers for the test dataset.

Key column:

* `msno`: Customer identifier.

This file can be used to identify the customers for whom churn predictions are required, depending on the competition's evaluation setup.

**4. `transactions.csv`**

Contains customer subscription and payment transaction records.

Key columns:

* `msno`: Customer identifier.
* `payment_method_id`: Payment method identifier.
* `payment_plan_days`: Duration of the subscription plan in days.
* `plan_list_price`: Listed subscription price.
* `actual_amount_paid`: Amount actually paid.
* `is_auto_renew`: Indicates whether automatic renewal is enabled.
* `transaction_date`: Transaction date.
* `membership_expire_date`: Membership expiration date.
* `is_cancel`: Indicates the cancellation status recorded for the transaction.

**5. `user_logs.csv`**

Contains customer listening activity and engagement records.

Key columns:

* `msno`: Customer identifier.
* `date`: Activity date.
* `num_25`: Number of songs played for less than 25% of their duration.
* `num_50`: Number of songs played for approximately 25%–50% of their duration.
* `num_75`: Number of songs played for approximately 50%–75% of their duration.
* `num_985`: Number of songs played for approximately 75%–98.5% of their duration.
* `num_100`: Number of songs played for their full duration.
* `num_unq`: Number of unique songs played.
* `total_secs`: Total listening time in seconds.

### Dataset Integration

The `msno` column serves as the common customer identifier across the dataset files, allowing customer information, subscription transactions, listening activity, and churn labels to be connected where matching records exist.

### Data Preparation

Before analysis and model development, the dataset will be examined for missing values, duplicate records, inconsistent data types, and potential data quality issues.

The transaction and listening activity records may require aggregation by customer before being combined with customer-level information.

The resulting dataset will be prepared for SQL analysis, exploratory data analysis (EDA), and machine learning.

### Target Variable

The target variable is `is_churn`, provided in `train_data.csv`.

It will be used to train and evaluate classification models designed to predict customer churn.

### Dataset Source

The dataset used in this project was obtained from the [Customer Retention Datathon – Riyadh Edition on Kaggle](https://www.kaggle.com/competitions/customer-retention-datathon-riyadh-edition/data).

The dataset contains customer information, transaction records, user activity logs, and churn labels. These data will be used to analyze customer behavior, identify factors associated with churn, and build a Machine Learning model to predict customer churn.

## Tools & Technologies

The following tools and technologies will be used throughout the project:

* **Python:** Data processing, analysis, and Machine Learning.
* **SQL:** Data querying, database management, and customer behavior analysis.
* **Pandas:** Data manipulation and analysis.
* **NumPy:** Numerical computing and data processing.
* **Matplotlib, Seaborn & Plotly:** Data visualization and exploratory data analysis, including interactive charts.
* **Scikit-learn:** Machine Learning model development and evaluation.
* **Jupyter Notebook:** Interactive analysis, experimentation, and documentation.
* **Git & GitHub:** Version control and project documentation.


## => Project Workflow

The project will follow these main phases:

### 1. Data Understanding

* Inspect the five CSV files and understand their structure.
* Review column names, data types, and data distributions.
* Identify relationships between the datasets using the customer identifier (`msno`).

### 2. Database Creation

* Choose a suitable SQL database system.
* Create the database and define the appropriate table structures.
* Import the CSV files into the database.
* Verify that the data has been imported correctly.

### 3. Data Cleaning and Preparation

* Check for missing values and duplicate records.
* Identify inconsistent or invalid values.
* Convert date columns into appropriate formats.
* Prepare the data for SQL analysis and further processing.

### 4. SQL Analysis

* Analyze customer information and subscription patterns.
* Explore transaction history and payment behavior.
* Investigate customer activity and listening behavior.
* Examine churn distribution and relationships between relevant variables.

### 5. Exploratory Data Analysis (EDA)

* Analyze the distribution of customer churn.
* Explore relationships between customer characteristics and churn.
* Visualize subscription, transaction, and activity patterns.
* Use interactive visualizations with Plotly to communicate key findings.

### 6. Feature Engineering

* Extract meaningful features from transaction and activity data.
* Aggregate relevant information at the customer level.
* Prepare the features required for Machine Learning.
* Check for data leakage before model training.

### 7. Machine Learning

* Define the target variable and input features.
* Split the labeled data into training and validation sets.
* Train suitable classification models.
* Compare model performance using appropriate evaluation metrics.

### 8. Model Evaluation

* Evaluate the trained models using metrics such as Precision, Recall, F1-score, and ROC-AUC, where appropriate.
* Analyze the model's ability to identify customers at risk of churn.
* Compare results and select a suitable model.

### 9. Business Recommendations

* Summarize the most important findings.
* Identify customer behavior patterns associated with churn.
* Suggest data-driven strategies to help improve customer retention.
