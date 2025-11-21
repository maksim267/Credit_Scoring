# Credit Scoring Project

## Overview
This project focuses on building a machine learning model for credit scoring. The goal is to predict whether a client will repay a loan based on various factors from their credit application data. The project uses statistical models and historical data from clients who have previously taken loans to make predictions about new loan applications.

## Project Structure
The notebook is organized into the following main sections:

### 1. Data Loading
- Import necessary libraries (pandas, numpy, matplotlib)
- Mount Google Drive and load the dataset (`credit_train.csv`)
- Define the target column as "Loan Status"

### 2. Data Analysis and Transformation

#### Handling Missing Values
- **Customer ID Analysis**: Identifies duplicate customer entries and creates a "Number of Occurrences" feature
- **Missing Value Treatment**:
  - Credit Score and Annual Income: Filled with median values
  - Years in current job: Filled with -1 (indicating missing)
  - Months since last delinquent: Filled with -1
  - Maximum Open Credit: Dropped rows with missing values
  - Bankruptcies: Filled with 0
  - Tax Liens: Dropped rows with missing values

#### Categorical Feature Transformation
- **Manual Encoding**: For specific categorical features
- **One-Hot Encoding**: Applied to remaining categorical variables
- **Visualization**: Pie charts created to show distribution of categorical variables

## Key Features
The dataset contains 19 columns including:
- Loan identifiers (Loan ID, Customer ID)
- Target variable (Loan Status)
- Financial features (Current Loan Amount, Credit Score, Annual Income, Monthly Debt)
- Employment information (Years in current job)
- Credit history (Years of Credit History, Number of Open Accounts, Number of Credit Problems)
- Ownership information (Home Ownership)
- Loan purpose and terms

## Data Quality Issues Addressed
- High number of missing values in Credit Score (19,154) and Annual Income (19,154)
- Significant missing data in Months since last delinquent (53,141)
- Duplicate customer entries handled
- Outliers and unusual values (e.g., Current Loan Amount of 99,999,999)

## Next Steps
The notebook prepares the data for machine learning modeling by:
1. Cleaning and imputing missing values
2. Encoding categorical variables
3. Creating additional features (Number of Occurrences)
4. Removing identifier columns that won't be used in modeling

The cleaned dataset is now ready for feature engineering, model training, and evaluation to predict loan repayment behavior.

## Requirements
- Python 3
- pandas
- numpy
- matplotlib

## Usage
Run the notebook cells sequentially to load, clean, and prepare the data for credit scoring model development.
