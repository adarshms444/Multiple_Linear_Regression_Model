# Multiple Linear Regression Model for Predicting Highway MPG

This project involves building a multiple linear regression model to predict the Highway MPG (Miles Per Gallon) of vehicles based on various engine, fuel, and dimension-related features. The data used in the model comes from a CSV file (cars.csv) that contains information about different car specifications. The model is preprocessed through various steps such as data cleaning, encoding categorical variables, handling missing values, and feature selection. After cleaning and feature engineering, the model is trained using polynomial features, and the performance is evaluated on the test set.

## Steps

Data Loading and Exploration The dataset is loaded using pandas.read_csv() from a specified path (/content/cars.csv). 
The shape of the dataset is printed, followed by the first few rows using df.head(). The dataset is analyzed for numerical and categorical variables, and the number of duplicates is checked.
Data Cleaning and Preprocessing Missing values are dropped using dropna().
Categorical variables are encoded using LabelEncoder for converting non-numeric values to numeric representations. A correlation matrix is computed to identify the relationship between different features and the target variable (Highway MPG).
Features with high multicollinearity are identified and excluded based on the Variance Inflation Factor (VIF) greater than a specified threshold (5 in this case). 
Outliers are removed using the Interquartile Range (IQR) method.
## Feature Engineering 
Polynomial features are created to capture nonlinear relationships between the features and the target variable. 
The data is split into training and testing sets (15% test data) using train_test_split().
Model Training The training data is standardized using StandardScaler() to ensure that all features are on the same scale. A linear regression model is trained on the scaled training data.
Model Evaluation The model's performance is evaluated using metrics such as:
Mean Squared Error (MSE) 
Root Mean Squared Error (RMSE) 
R² Score (Coefficient of Determination) Model accuracy (R² Score as percentage)
## Visualizations include:

A scatter plot comparing actual vs. predicted highway MPG. A histogram of residuals to check the normality of errors.
A scatter plot of residuals vs. predicted values to check for homoscedasticity.

Model Performance Mean Squared Error (MSE): Measures the average squared difference between actual and predicted values. 
Root Mean Squared Error (RMSE): The square root of MSE, providing error magnitude in the same units as the target variable. 
R² Score: The proportion of the variance in the target variable that is predictable from the features.
## Model Accuracy: 
The accuracy of the model, calculated as R² Score percentage. 
## Conclusion 
This model provides an estimation of the highway miles per gallon of vehicles based on a variety of attributes related to the engine, fuel, and dimensions. The final model has been optimized to handle multicollinearity, missing data, outliers, and other preprocessing steps to enhance its predictive power.
