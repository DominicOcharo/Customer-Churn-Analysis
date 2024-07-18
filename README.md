# Customer Churn Analysis

## Overview

This project performs an exploratory data analysis (EDA) on a customer churn dataset to understand the factors contributing to customer churn. The dataset is from a telecommunications company and contains various features related to customer demographics, account information, and service usage.

## Table of Contents

- [Installation](#installation)
- [Dataset](#dataset)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Findings](#findings)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)

## Installation

To get started with this project, clone the repository and install the required packages.

```bash
git clone https://github.com/yourusername/customer-churn-analysis.git
cd customer-churn-analysis
pip install -r requirements.txt
```

## Dataset

The dataset used for this analysis is `WA_Fn-UseC_-Telco-Customer-Churn.csv`. It contains various columns related to customer demographics, account information, and service usage, such as `gender`, `SeniorCitizen`, `Partner`, `Dependents`, `tenure`, `PhoneService`, `MultipleLines`, `InternetService`, `OnlineSecurity`, `OnlineBackup`, `DeviceProtection`, `TechSupport`, `StreamingTV`, `StreamingMovies`, `Contract`, `PaperlessBilling`, `PaymentMethod`, `MonthlyCharges`, `TotalCharges`, and `Churn`.

## Exploratory Data Analysis

The EDA process involves the following steps:

1. **Importing Necessary Libraries**: Libraries like NumPy, Pandas, SciPy, Matplotlib, Seaborn, Plotly, and warnings were imported for data manipulation, statistical analysis, and visualization.

2. **Loading the Data**: The dataset was loaded into a Pandas DataFrame for analysis.

3. **Dataset Overview**: An initial overview of the dataset was performed to understand its shape, columns, and data types. This also included checking for missing values.

4. **Data Preprocessing**: 
   - Columns were converted to appropriate data types.
   - Missing values in the 'TotalCharges' column were handled by dropping rows with missing values.
   - Categorical columns were analyzed for unique values, and certain values like 'No phone service' and 'No internet service' were replaced with 'No'.
   - A new column 'Automatic' was created to categorize payment methods into 'automatic' and 'manual'.

5. **Descriptive Statistics**: Descriptive statistics were calculated for numerical columns to understand the distribution and summary of the data.

6. **Univariate Analysis**: 
   - The distribution of customers based on churn status, Internet service, contract type, and payment method were visualized using bar plots and pie charts.

7. **Bivariate Analysis**: 
   - Relationships between churn and various features like streaming TV usage, payment method, and gender were analyzed using count plots and crosstab tables.

8. **Multivariate Analysis**: 
   - Correlation between various features and churn was calculated and visualized to identify significant relationships.

## Findings

- **Churn Count**: 26.5% of customers have churned, indicating a highly imbalanced dataset.
- **Internet Service**: Majority of the customers use Fiber Optic Cables.
- **Contract Type**: More than half of the customers are on a month-to-month contract.
- **Payment Method**: Around 33.63% of customers pay through Electronic Check. Other methods are almost equally used.
- **Correlation with Churn**: 
  - Tenure period and contract type have a high negative correlation with churn.
  - Month-to-month contracts and lack of online security have a high positive correlation with churn.

## Usage

To run the analysis, execute the Jupyter notebook `customer_churn_analysis.ipynb`.

```bash
jupyter notebook customer_churn_analysis.ipynb
```

## Contributing

Contributions are welcome! Please create a pull request with your proposed changes.
