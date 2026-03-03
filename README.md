# House Prices - Advanced Regression Techniques

This repository contains my solution for the [Kaggle House Prices: Advanced Regression Techniques](https://www.kaggle.com/c/house-prices-advanced-regression-techniques) competition. The goal is to predict the final price of each home in Ames, Iowa, using 79 explanatory variables describing almost every aspect of residential homes.

## Project Structure

- `House_Price.ipynb`: Jupyter Notebook containing data exploration, feature engineering, model training, and evaluation.
- `train.csv`: The training dataset with target variables (`SalePrice`).
- `test.csv`: The test dataset for making final predictions.
- `data_description.txt`: Full description of each column in the dataset.
- `prediction.csv`: The final predicted sale prices for the test set.
- `requirements.txt`: List of dependencies required to run the project.
- `*.joblib`: Serialized versions of the best-performing models (XGBoost, Random Forest, and SGD).

## Methodology

### 1. Data Exploration & Preprocessing
- Handled missing values based on the data description (e.g., filling 'None' for categorical features where a missing value implies the absence of a feature like a garage).
- Performed log transformation on the target variable (`SalePrice`) to handle skewness.
- Encoded categorical variables and scaled numerical features for better model performance.

### 2. Modeling
I experimented with several regression algorithms and tuned them for optimal performance:
- **XGBoost**: Gradient boosted decision trees for high predictive power.
- **Random Forest**: An ensemble of decision trees to reduce overfitting.
- **Stochastic Gradient Descent (SGD)**: A linear model optimized for efficiency.
- **Linear Regression**: As a baseline model

### 3. Evaluation
The models were evaluated using Root-Mean-Squared-Error (RMSE) between the logarithm of the predicted value and the logarithm of the observed sales price, ensuring that errors in predicting expensive houses and cheap houses affect the result equally.

## Getting Started

### Prerequisites
Ensure you have Python installed. You can install the required libraries using:

```bash
pip install -r requirements.txt
