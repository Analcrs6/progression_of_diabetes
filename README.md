# Diabetes Progression Analysis

## Project Overview
This project aims to analyze the progression of diabetes using a dataset containing various features such as age, BMI, blood pressure, and other physiological measurements. The primary goal is to identify key factors that contribute to the progression of the disease, providing insights that could aid in better understanding and managing diabetes.

## Data Collection and Preprocessing

The dataset `progression_of_diabetes.csv` was loaded and preprocessed. Key steps included:
- **Importing Libraries**: Utilized `numpy`, `pandas`, `matplotlib`, and `seaborn` for data manipulation, analysis, and visualization.
- **Data Loading**: Loaded the dataset from `/content/progression_of_diabetes.csv`.
- **Data Cleaning**: Performed checks for duplicated rows and missing values, ensuring data integrity. It was confirmed that there were no duplicates or missing values.
- **Column Renaming**: Columns were explicitly renamed for consistency and ease of use (e.g., 'AGE', 'SEX', 'BMI', 'BP', 'S1', 'S2', 'S3', 'S4', 'S5', 'S6', 'Y').
- **Outlier Identification**: Outliers were identified using the IQR method for the 'AGE' column.

## Exploratory Data Analysis (EDA)

Extensive exploratory data analysis was conducted to understand the dataset's characteristics and relationships between variables. Key analyses and visualizations include:

- **Correlation Matrix**: A heatmap of the Pearson correlation matrix was generated to visualize the relationships between all features and the target variable 'Y' (diabetes progression). This helped in identifying both strong positive and negative correlations.
- **Target Variable Correlation**: Specifically analyzed correlations of all features with the target variable 'Y'. Features like 'BMI' (0.586) and 'S5' (0.566) showed strong positive correlations with 'Y', suggesting they are significant predictors of diabetes progression.
- **Feature Importances**: Used a RandomForestRegressor model to determine and visualize the importance of each feature in predicting 'AGE', providing insights into feature relevance.
- **Histograms and KDE Plots**: Visualized the distribution of numerical features using histograms and Kernel Density Estimate (KDE) plots to understand their patterns and identify any skewness.
- **Boxplots**: Used boxplots to visualize the distribution of 'AGE' by 'SEX' and to detect outliers across all features, confirming data cleanliness.
- **Pairplot**: Generated pair plots to visualize pairwise relationships between variables, offering a comprehensive view of scatter plots and distributions.

## Key Findings

Based on the EDA, the following key insights were observed:
- **BMI and Diabetes Progression**: There is a strong correlation between Body Mass Index (BMI) and diabetes progression ('Y'), indicating that individuals with higher BMI tend to experience more severe progression.
- **Age and Diabetes Progression**: Younger individuals generally show less severe diabetes progression. The analysis also suggested that individuals around 50 years old might have a higher likelihood of developing diabetes.
- **Feature Importance**: 'BMI' and 'S5' are among the most strongly correlated features with diabetes progression, making them critical for further predictive modeling.

This analysis provides a foundational understanding of the diabetes progression dataset, highlighting important features and relationships that can be further explored in predictive modeling or deeper statistical studies.
