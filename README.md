# CSP571 Project - Boston House Prices Dataset Analysis
## Dataset Overview
This project utilizes the "Boston House Prices dataset" from Kaggle, which contains data on various attributes of houses in Boston suburbs. The dataset provides insights into the housing values in suburbs of Boston, with features like crime rate, property tax rate, number of rooms, and more.

https://www.kaggle.com/datasets/vikrishnan/boston-house-prices 

## Project Objective
This project focuses on predicting housing prices using data from the Boston housing dataset. The goal is to explore the data, develop predictive models, and compare their performance using cross-validated metrics. 

## Data Description
The dataset contains 506 rows and 14 columns:
- CRIM: Per capita crime rate by town
- ZN: Proportion of residential land zoned for lots over 25,000 sq.ft.
- INDUS: Proportion of non-retail business acres per town.
- CHAS: Charles River dummy variable (1 if tract bounds river; 0 otherwise)
- NOX: Nitric oxides concentration (parts per 10 million)
- RM: Average number of rooms per dwelling
- AGE: Proportion of owner-occupied units built prior to 1940
- DIS: Weighted distances to five Boston employment centres
- RAD: Index of accessibility to radial highways
- TAX: Full-value property-tax rate per $10,000
- PTRATIO: Pupil-teacher ratio by town
- B: 1000(Bk - 0.63)^2 where Bk is the proportion of blacks by town
- LSTAT: % lower status of the population
- MEDV: Median value of owner-occupied homes in $1000's

## **Project Steps**
### 1. **Data Exploration and Initial Analysis**
- Conducted exploratory data analysis (EDA), including:
  - Correlation heatmaps to identify features strongly related to housing prices (**MEDV**).
  - Principal Component Analysis (PCA) to visualize patterns in the dataset.
  - K-means clustering to identify natural groupings in the data.

### 2. **Model Development**
Three models were developed and evaluated using 5-fold cross-validation:
- **Linear Regression**: A baseline model for comparison.
- **Lasso Regression**: A regularized linear model to reduce overfitting by penalizing large coefficients.
- **Decision Tree Regression**: A non-linear model to capture complex relationships in the data.

### 3. **Model Comparison**
The models were compared using three metrics:
- **Mean Absolute Error (MAE)**: Measures average prediction error.
- **Mean Squared Error (MSE)**: Penalizes larger errors more heavily.
- **Root Mean Squared Error (RMSE)**: Provides a metric in the same units as the target variable.

---

## **Results**
The performance of each model is summarized below:

| **Model**               | **MAE**       | **MSE**       | **RMSE**      |
|--------------------------|---------------|---------------|---------------|
| Linear Regression        | 3.39          | 23.49         | 4.84          |
| Lasso Regression         | 3.57          | 26.67         | 5.16          |
| Decision Tree Regression | 2.19          | 9.00          | 3.00          |

- The **Decision Tree Regression** model outperformed all others across all metrics, making it the most suitable model for this dataset.

---

## **Conclusion**
- The **Decision Tree Regression model** is the best-performing model and is recommended for predicting housing prices due to its ability to capture non-linear relationships in the data.
- Regularization via Lasso regression did not improve performance compared to the baseline linear regression, indicating that regularization was not necessary for this dataset.

---

## **Files in the Repository**
- `CSP571 Project - Yingqi.ipynb`: Jupyter notebook containing Yingqi's data exploration and initial analysis.
- `CSP571 Project - Fatima.ipynb`: Jupyter notebook containing Fatima's baseline model development and evaluation.
- `CSP571 Project - Conan.ipynb`: Jupyter notebook containing Nan's model optimization, alternative model development, and model comparison.
- `CSP571 Project - Combined.ipynb`: A comprehensive Jupyter notebook merging the coding sections from all three team members, providing a complete view of the project.
- `README.md`: Project documentation and an overview of the repository.
- `housing.csv`: The dataset used for analysis, provided in a suitable format for direct loading into Python.

---

## **Team Members**
1. **Yingqi Jiang**: Data Exploration and Initial Analysis
2. **Fatima Vahora**: Baseline Model Development and Evaluation
3. **Nan Wang**: Model Optimization, Alternative Model Development, and Model Comparison

---

## **Acknowledgements**
- The Boston Housing dataset was originally sourced from the Kaggle.
- Special thanks to our course **CS571 - Data Preparation and Analysis** for guiding us through this project.

---