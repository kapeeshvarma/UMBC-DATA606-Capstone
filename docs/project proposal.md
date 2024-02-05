# Appliances Energy Prediction

### A Regression Analysis and Prediction project on the Energy consumption of Home Appliances.

#### Prepared for UMBC Data Science Master's Degree Capstone by Dr Chaojie (Jay) Wang

#### Vinay Kapeesh Varma Gottumukkala

#### Github Profile: [https://www.github.com/kapeeshvarma](https://www.github.com/kapeeshvarma)

#### LinkedIn Profile: [https://www.linkedin.com/in/kapeeshvarma](https://www.linkedin.com/in/kapeeshvarma)

```
```

### BACKGROUND

In this time of global uncertainty world needs energy and in increasing quantities to support economic and social progress and build a better quality of life, in particular in developing countries.
But even today there are many regions which face constant power outages.
These outages are primarily caused due to excess load consumed by home appliances.

Hence, the ability to predict energy consumption can not only save money for end user but can also help in generating money by giving excess energy back to Grid (in case of solar panels usage).
In this project, I perform regression analysis in order to predict appliance energy usage based on data collected from various sensors.

```
```

In this project, I analyse the data from different sensors along with other weather features in order to predict the power consumption of Home Appliances.
The dataset used consists of sensor data taken at 10 minute intervals for 4.5 months. The source of the dataset is Kaggle.
Weather data was downloaded from a public data set from Reliable Prognosis (rp5.ru) and merged together with the experimental data sets using the date and time column.
Two random variables have been included in the data set for testing the regression models and to filter out non-predictive attributes (parameters).
Regression will be performed on this data using different models such as Linear Regressor, Random Forests etc., and the performance of these models will be calculated to find the best fit.

```
```

### DATA

Data Source: Kaggle\
Data Source Link: [https://www.kaggle.com/datasets/loveall/appliances-energy-prediction/data](https://www.kaggle.com/datasets/loveall/appliances-energy-prediction/data)\
Data Size: 11.98 MB\
Data Shape: (19735, 29)\
Time Period: Jan 2016 to May 2016\
 \
Each row represents the sensor data at that particular time and there are multiple columns each representing different sensors and weather parameters.\
 \
Columns: [date, Appliances, lights, T1, RH_1, T2, RH_2, T3, RH_3, T4, RH_4, T5, RH_5, T6, RH_6, T7,\
RH_7, T8, RH_8, T9, RH_9, T_out, Press_mm_hg, RH_out, Windspeed, Visibility, Tdewpoint, rv1, rv2]\
 \
Data Type: Float values\
Target Variable: 'Appliances' column\
Predictor Variables: All sensor columns
