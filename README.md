# Telecom-Customer Churn Prediction

## Overview

This project aims to predict customer churn for a telecommunications company using machine learning techniques. Customer churn is an important metric for companies as it indicates the rate at which customers leave. Predicting churn helps in identifying at-risk customers and implementing strategies to retain them.

The analysis is conducted using a Jupyter Notebook which contains data preprocessing, model training, and evaluation. Various machine learning models are evaluated to find the best performing algorithm for predicting customer churn.

## Table of Contents

- [Project Structure](#project-structure)
- [Data](#data)
- [Modeling](#modeling)
- [Evaluation](#evaluation)
- [Usage](#usage)
- [Dependencies](#dependencies)
- [Contributing](#contributing)

## Project Structure

The project consists of the following main components:

- **`analysis.ipynbb`**: The Jupyter Notebook file that contains the entire data analysis and modeling process.

## Data

The dataset used in this project is related to customer churn in a telecommunications company. It includes various features related to customer behavior and account information.

### Features

- **customerID**: Unique identifier for each customer.
- **Churn**: Target variable indicating whether the customer has churned (`Yes`/`No`).
- **MultipleLines**: Whether the customer has multiple lines (`Yes`/`No`/`No phone service`).
- **Dependents**: Whether the customer has dependents (`Yes`/`No`).
- **InternetService**: Type of internet service (`DSL`/`Fiber optic`/`No`).
- **OnlineSecurity**: Whether the customer has online security (`Yes`/`No`/`No internet service`).
- **MonthlyCharges**: The amount charged to the customer monthly.
- (Other features related to customer behavior and account details.)

## Modeling

### Data Preprocessing

1. **Data Loading**: Load the dataset from the provided CSV file.
2. **Feature Engineering**: Handle categorical and numerical features, including:
   - Dropping irrelevant features such as `MultipleLines`, `Dependents`, `InternetService`, and `OnlineSecurity`.
   - Applying log transformation to the `MonthlyCharges` feature to reduce skewness.
3. **Feature Selection**: Identify categorical and numerical features.
4. **Data Transformation**: Apply one-hot encoding to categorical features.

### Models Evaluated

1. **Logistic Regression**
2. **Support Vector Machines (SVM)**
3. **Random Forest**
4. **Gradient Boosting Machines (XGBoost)**
5. **K-Nearest Neighbors (KNN)**
6. **Decision Trees**
7. **Extra Trees**
8. **Ensemble Methods:**
   - AdaBoost
   - Voting Classifier
   - Bagging
   - Gradient Boosting

### Evaluation

Each model is evaluated using:
- **Classification Report**: Precision, recall, and F1-score.
- **Confusion Matrix**: A matrix showing true positive, true negative, false positive, and false negative values.

#### Summary of Results

- **Random Forest**: High training accuracy and F1-score but drops in testing performance.
- **XGBoost**: High training accuracy and F1-score, performs similarly to Random Forest on test data.
- **SVM**: Balanced performance on both training and testing datasets.
- **Voting Classifier**: Good balance of precision and recall on the test set.
- **Bagging**: High training accuracy, competitive performance on the test set.

## Usage

To run the analysis and model evaluation:

1. **Open the Jupyter Notebook**: Launch Jupyter Notebook and open `analysis.ipynb`.

2. **Execute the Cells**: Run each cell in the notebook sequentially. This will load the data, preprocess it, train the models, and evaluate their performance.

### Example

```bash
# Launch Jupyter Notebook
jupyter analysis.ipynb
```

### Dependencies

- pandas
- numpy
- scikit-learn
- xgboost
- matplotlib
- seaborn
- imbalanced-learn

## Contributing

Contributions are welcome! Please fork the repository, make your changes, and submit a pull request. Ensure that you follow the coding standards and add relevant documentation.

For any issues or suggestions, please open an issue on GitHub.

## Acknowledgments

- Dataset source: `WA_Fn-UseC_-Telco-Customer-Churn.csv`
- Thanks to contributors and mentors who provided support and guidance.