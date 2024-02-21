# Project Name
> Duild a predictive regression model for Australian house prices, emphasizing regularization, robustness, and generalizability.


## Table of Contents
* [Technologies Used] : Python, Jupyter notebook

## General Information
# Requirement Summary
## 1. Background:

- "Surprise Housing", a US-based company, is entering the Australian housing market.
- They want to use data analytics to buy houses below actual/market value and flip them for profit.
- They have collected a dataset of house sales in Australia.

## 2. Business Goal:

- Build a regression model with regularization to predict the actual value of prospective properties.
- Use the model to decide whether to invest in those properties.
- Gain insights into how house prices vary with different variables.

## 3. Data:

- CSV file [train.csv](https://ml-course3-upgrad.s3.amazonaws.com/Assignment_+Advanced+Regression/train.csv) containing data on past house sales in Australia.
- Field definitions provided in [Data Definition File](https://cdn.upgrad.com/UpGrad/temp/87f67e28-c47e-4725-ae3c-111142c7eaba/data_description.txt)

## 4. Requirements:

### Part-1 - A. Identify significant predictor variables:

- Determine which variables in the data are most important for predicting house price.
- Use appropriate statistical methods for variable selection.

### Part-1 - B. Assess model performance:

- Measure how well the chosen variables describe house price using R-squared, mean squared error, and other relevant metrics.

### Part-1 - C. Optimize regularization parameters:

- Find the optimal values of lambda for both ridge and lasso regression.
- Usr techniques like cross-validation and grid search.

### Q-1. Figure the Optimal value of regularization parameters:
- What is the optimal value of alpha for ridge and lasso regression?
- What will be the changes in the model if you choose double the value of alpha for both ridge and lasso? 
- What will be the most important predictor variables after the change is implemented?


### Q-2. Interpret and compare models:

- Explain the impact of changing alpha on the model and the most important predictor variables.
- Choose the best model (ridge or lasso) based on performance and explain the rationale.

### Q-3. Handle missing important predictors:

- Develop a new model excluding the five most important predictors unavailable in new data.
- Identify the new most Five most important predictors in new model.

### Q-4. Ensure robustness and generalizability:

- Implement techniques like data augmentation and k-fold cross-validation to ensure the model performs well on unseen data.
- Explain the implications of robustness and generalizability for model accuracy.

## 4. Key Constraints:

- Five most important predictors from the lasso model might be unavailable in new data.
- The model needs to be robust and generalizable to unseen data.

## 5. Key Outcomes:

- A regression model for predicting house price in Australia.
- Identification of significant predictor variables for house price.
- Insights into how house price varies with different variables.
- Understanding of the impact of regularization and missing data on the model.


# High Level Approach:

## 1. Data Exploration and Cleaning:

- Visualize distributions of numerical features and relationships between features.
- Check for missing values and outliers.
- Handle missing values with appropriate imputation techniques (e.g., mean/median imputation, k-nearest neighbors).
- Address outliers winsorizing or capping if they don't represent noise.
- Encode categorical features using label encoding, one-hot encoding, or target encoding as appropriate.

## 2. Feature Engineering:
- Create new features based on domain knowledge and exploratory analysis (e.g., age of house, total living area, price per square foot).
- Select the most informative features using techniques like correlation analysis or feature importance methods.

## 3. Model Selection and Tuning:

- Implement and compare different linear regression models (OLS, ridge, lasso).
- Use cross-validation or grid search to find optimal hyperparameters for each model.
- Evaluate models based on R-squared, mean squared error, and other relevant metrics.

## 4. Regularization for Robustness:

- Choose the best model and apply regularization (ridge, lasso, or elastic net) to prevent overfitting.
- Fine-tune regularization parameters for optimal performance.

## 5. Addressing Missing Predictors:

- If the five most important predictors from the lasso model are unavailable, create a new model without them.
- Analyze which variables are still available and select the most promising ones based on feature importance or expert knowledge.
- Reiterate steps 3-4 with the new feature set.

## 6. Generalizability and Testing:

- Use k-fold cross-validation to assess model generalizability on unseen data.
- Monitor model performance across different data subsets to detect potential biases.
- Consider non-linear models if necessary based on performance and data characteristics.

## 7. Interpretation and Communication:

Provide visualizations, feature importance analyses, and confidence intervals to explain model predictions and limitations.
Clearly communicate the key findings and insights for actionable decision-making.

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->

## Conclusions

### The optimal lambda value in case of Ridge and Lasso is as below:

- Ridge - 6
- Lasso - 0.0001

### The Mean Squared error in case of Ridge and Lasso are:

- Ridge - 9.23
- Lasso - 9.22

### The Mean Squared Error of Lasso is slightly lower than that of Ridge

- Also, since Lasso helps in feature reduction (as the coefficient value of one of the feature became 0), Lasso has a better edge over Ridge.

- Hence based on Lasso, the factors that generally affect the price are the Zoning classification, Living area square feet, Overall quality and condition of the house, Foundation type of the house, Number of cars that can be accomodated in the garage, Total basement area in square feet and the Basement finished square feet area

Therefore, the variables predicted by Lasso in the above bar chart as significant variables for predicting the price of a house.


## Technologies Used
- NumPy version: 1.24.3
- Pandas version: 2.0.3
- Matplotlib version: 3.7.2
- Seaborn version: 0.12.2
- Scikit-learn version: 1.3.0
- Python version: 3.11.5


## Acknowledgements
- This project was inspired by our Upgrad Team. 


## Contact
Created by [@khanna-vijay]

