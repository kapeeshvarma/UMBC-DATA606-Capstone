# Appliances Energy Prediction

### A Regression Analysis and Prediction Project on the Energy Consumption of Home Appliances

#### Vinay Kapeesh Varma Gottumukkala

[Link to YouTube Video](https://youtu.be/-As_m2lnUD4)  
[Link to Project PPT](https://github.com/kapeeshvarma/UMBC-DATA606-Capstone/blob/main/docs/Project%20PPT.pptx)  
[Link to GitHub Project Repo](https://github.com/kapeeshvarma/UMBC-DATA606-Capstone)

---

## Background

In the current era of global uncertainty, the world needs increasing amounts of energy to support economic and social progress and improve the quality of life, particularly in developing countries. However, many regions still face constant power outages, often due to the excessive load consumed by home appliances.

Predicting energy consumption can save money for end users and potentially generate revenue by returning excess energy to the grid, especially with the use of solar panels. This project aims to perform regression analysis to predict appliance energy usage based on data collected from various sensors.

## Description of Data Sources

The dataset used in this project consists of sensor data collected at 10-minute intervals over 4.5 months, sourced from Kaggle. Additional weather data was downloaded from a public dataset provided by Reliable Prognosis (rp5.ru) and merged with the experimental datasets using the date and time columns. The dataset includes two random variables for testing regression models and filtering out non-predictive attributes.

### Data Details

- **Data Source**: Kaggle
- **Data Link**: [Appliances Energy Prediction Dataset](https://www.kaggle.com/datasets/loveall/appliances-energy-prediction/data)
- **Data Size**: 11.98 MB
- **Data Shape**: 19735 rows, 29 columns
- **Time Period**: January 2016 to May 2016

### Columns

- **Date**: Timestamp of the observation
- **Appliances**: Energy consumption of appliances (target variable)
- **Lights**: Energy consumption of lights
- **T1, T2, ... T9**: Temperature measurements from different sensors
- **RH_1, RH_2, ... RH_9**: Humidity measurements from different sensors
- **T_out**: Temperature outside
- **Press_mm_hg**: Atmospheric pressure
- **RH_out**: Humidity outside
- **Windspeed**: Wind speed
- **Visibility**: Visibility in meters
- **Tdewpoint**: Dew point temperature
- **rv1, rv2**: Random variables for testing

## Exploratory Data Analysis (EDA)

EDA was conducted to understand the dataset and uncover significant patterns and relationships:

1. **Distribution of Appliances Energy Consumption**: The energy consumption of appliances showed a right-skewed distribution, indicating that most values were low with a few high consumption points.
2. **Correlation Analysis**: Though the appliance energy consumption isn't strongly correlated with any individual variables such as temperature and humidity, the variables altogether affect the energy consumption.
3. **Time-Series Trends**: Analysis of time-series data revealed daily and weekly patterns in energy consumption, such as the consumption was high during evenings and on weekends.
4. **Outliers**: Identified and analyzed outliers to understand unusual consumption patterns, which were largely due to extreme weather conditions or specific high-energy-use activities. 5% of the outliers have been removed for better analytics.

## Machine Learning (ML) Models

Several regression models were trained, improved through hyperparameter tuning and evaluated to predict the energy consumption of appliances:

1. **Linear Regression**: Provided a baseline model with moderate performance. It was straightforward but struggled with capturing non-linear relationships.
2. **Ridge Regression**: Improved upon linear regression by adding regularization to reduce overfitting and handle multicollinearity among the predictor variables.
3. **XGBoost Regressor**: Highly improved performance by using gradient boosting techniques, capturing complex patterns in the data and providing robust predictions.
4. **Random Forest Regressor**: Achieved highest performance by handling non-linearities and interactions between features. Reduced overfitting through ensemble learning.

### Model Performance Metrics

- **Linear Regression**: R² = 0.922, MSE = 0.017
- **Ridge Regression**: R² = 0.925, MSE = 0.016
- **XGBoost Regressor**: R² = 0.981, MSE = 0.004
- **Random Forest Regressor**: R² = 0.997, MSE = 0.0005

## Conclusion

The project successfully captured key insights through data analysis. It also demonstrated that machine learning models could predict the energy consumption of home appliances with reasonable accuracy. The Random Forest Regressor emerged as the best-performing model, handling non-linearities and interactions between features.

## Future Research

Future research could explore the following areas to enhance prediction accuracy and applicability:

1. **Integration of Real-Time Data**: Incorporate real-time sensor and weather data to provide more accurate and timely predictions.
2. **Advanced Feature Engineering**: Develop more sophisticated features to capture interactions and non-linear relationships more effectively.
