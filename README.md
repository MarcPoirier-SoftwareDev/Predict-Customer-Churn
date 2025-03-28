# Predict Customer Churn


- Project **Predict Customer Churn** of ML DevOps Engineer Nanodegree Udacity

## Project Description
This project focuses on predicting customer churn for a bank using machine learning techniques. The objective is to identify customers likely to leave based on their demographic and transactional data, enabling proactive retention strategies. Initially developed as a Jupyter notebook (`churn_notebook.ipynb`), the project has been refactored into a modular Python library (churn_library.py) that implements a complete machine learning pipeline. This pipeline includes data ingestion, exploratory data analysis (EDA), feature engineering, model training (using Logistic Regression and Random Forest), and model evaluation. A separate testing script (churn_script_logging_and_tests.py) validates the library's functions and logs the results.

The refactored code adheres to software engineering best practices, such as modularity, unit testing, logging, and PEP 8 compliance. By reading this README, users can set up the environment, run the pipeline, test the functions, and interpret the results.

## Files and Data Description

The root directory contains the following files and folders:

- churn_library.py: The core Python library containing functions for the churn prediction pipeline:
    - import_data: Loads the dataset from a CSV file.

    - perform_eda: Conducts exploratory data analysis and saves plots (e.g., histograms, correlation heatmaps) to the images/ directory.

    - encoder_helper: Encodes categorical variables using target encoding.

    - perform_feature_engineering: Prepares features and splits data into training and testing sets.

    - train_models: Trains Logistic Regression and Random Forest models, evaluates them, and saves results (e.g., ROC curves, feature importances) to images/ and models to models/.

- churn_script_logging_and_tests.py: A script with unit tests for the functions in churn_library.py, logging results to logs/churn_library.log.

- README.md: This documentation file.

- data/bank_data.csv: The dataset containing customer details (e.g., age, gender, income, transaction history) and the churn indicator (Attrition_Flag).

- images/: Directory storing EDA plots and model evaluation visuals.

- models/: Directory storing trained models (e.g., rfc_model.pkl for Random Forest, logistic_model.pkl for Logistic Regression).

- logs/churn_library.log: Log file capturing the outcomes of the unit tests.

## Running Files

### Running the Churn Prediction Pipeline
To execute the full churn prediction pipeline, run the following command in your terminal:

bash
python churn_library.py

#### What happens when you run this file?
1. The script loads data/bank_data.csv.

2. It performs EDA, generating and saving plots (e.g., histograms, bar plots, heatmaps) to images/.

3. It engineers features by encoding categorical variables and splitting the data into training and testing sets.

4. It trains Logistic Regression and Random Forest models, evaluates their performance (e.g., classification reports, ROC curves), and saves the results to images/ and the trained models to models/.

### Running the Testing Script
To test the functions in churn_library.py and log the results, run:

~~~bash~~~
    python churn_script_logging_and_tests.py

#### What happens when you run this file?
1. The script executes unit tests for each function in churn_library.py.

2. It logs the outcome of each test (success or failure) to logs/churn_library.log.

3. If all tests pass, the functions are verified to work correctly; otherwise, error details are logged for debugging.

### Testing and Logging Instructions
- How to Test Functions:
    - The churn_script_logging_and_tests.py script includes unit tests for each function in churn_library.py. These tests check:
        - import_data: Ensures the dataset is loaded as a DataFrame with the expected shape.

        - perform_eda: Verifies that EDA plots are created and saved to images/.

        - encoder_helper: Confirms categorical variables are encoded correctly.

        - perform_feature_engineering: Validates that features and train/test splits are generated properly.

        - train_models: Checks that models are trained, evaluated, and saved to models/ and images/.

    - Run the testing script as shown above to execute these tests.

- How to Log and Review Results:
    - The testing script logs results to logs/churn_library.log.

    - Open this file to review the outcomes:
        - Success Messages: Indicate a function passed its test (e.g., "Data imported successfully").

        - Error Messages: Provide details if a test fails (e.g., "EDA plot not found in images/"), aiding in troubleshooting.

    - Regularly check the log file after running tests to ensure the library functions as expected.

By following these steps, users can run the churn prediction pipeline, validate the code through testing, and use the logs to confirm the results.



