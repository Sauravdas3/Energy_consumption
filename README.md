# Energy_consumption
my mail id : dassaurav4534@gmail.com
my wp number : 8116615954
if this notebook does not open then contact me...
OR you can Check the pdf of the same notebook.

# Energy Consumption Prediction Using Elastic Net Regression

## Introduction
This project aims to predict energy consumption based on various features like temperature, occupancy, HVAC usage, and kitchen usage. By understanding these patterns, we can optimize energy use, reduce costs, and contribute to sustainability efforts.

## Challenges
- **Data Quality**: Negative values and outliers in features such as occupancy and energy consumption.
- **Skewed Distributions**: Right-skewed energy consumption data, making it difficult to model extreme values.
- **Complex Relationships**: Non-linear correlations between temperature, energy consumption, and usage patterns.
- **Low R-squared**: Initial models showed low R² values, requiring more feature engineering and model tuning.

## Solutions
1. **Data Transformation**:
   - Calculated **Energy Consumption per Occupant** by dividing `Energy_Consumption_kWh` by `Occupancy` and setting it to zero where occupancy is zero.
   - Calculated **Temperature Difference** as the absolute difference between observed temperature and the mean temperature.
   
2. **Exploratory Data Analysis (EDA)**:
   - **Univariate Analysis**: Histograms and box plots revealed the distribution of key features.
   - **Bivariate Analysis**: Scatter plots showed relationships between energy consumption, temperature, and occupancy. A correlation matrix highlighted strong positive correlations with HVAC and kitchen usage.
   
3. **Elastic Net Regression**: Selected Elastic Net for its ability to handle multicollinearity and feature selection.

4. **Hyperparameter Tuning**: Performed cross-validation to optimize model parameters.

## Roadblocks
- **Outliers**: Some outliers in energy consumption affected model performance, particularly in high-consumption scenarios.
- **Residual Skewness**: Residuals displayed a slight positive skew, indicating that the model tended to underestimate energy consumption in some cases.

## Conclusion
- **Energy Consumption Trends**: Higher occupancy and temperatures are generally associated with increased energy consumption.
- **Feature Importance**: HVAC usage, kitchen usage, and temperature were the most significant predictors of energy consumption.
- **Model Evaluation Metrics**:
