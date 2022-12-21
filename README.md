# Hotel Booking Analysis

## Table of Content

1. Introduction
2. Problem Statement
3. Dataset Information
4. Conclusion
*****
1. Introduction

  Bike sharing system is an innovative transportation strategy that provides individuals with bikes for their common use on a short-term basis for a price or for free. Over the last few decades, there has been a significant increase in the popularity of bike-sharing systems all over the world. This is because it is an environmentally sustainable, convenient and economical way of improving urban mobility. In addition to this, this system also helps to promote healthier habits among its users and reduce fuel consumption.
  
2. Problem Statement

  Bike sharing system is an innovative transportation strategy that provides individuals with bikes for their common use on a short-term basis for a price or for free. Over the last few decades, there has been a significant increase in the popularity of bike-sharing systems all over the world. This is because it is an environmentally sustainable, convenient and economical way of improving urban mobility. In addition to this, this system also helps to promote healthier habits among its users and reduce fuel consumption.

3.  Dataset information

  Dataset used in this project is the Seoul Bike Share program data.This dataset contains information about the total count of rented bikes at each hour, as well as the date of observation and meteorological information (Humidity, Snowfall, Rainfall, Temperature Season, and so on) for that hour. The observations in the dataset were recorded during a span of 365 days, from December 2017 to November 2018.

  The Seoul Bike Dataset contains the following information:

    * Date - The date of each observation in the format 'year-month-day'
    * Hour - Hour of the day
    * Temperature - Temperature recorded in the city in Celsius (°C).
    * Humidity - Relative humidity in %
    * Wind speed - Speed of the wind in m/s
    * Visibility - measure of distance at which object or light can be clearly discerned in units of 10m
    * Dew point temperature - Temperature recorded in the beginning of the day in Celsius(°C).
    * Solar radiation - Intensity of sunlight in MJ/m^2
    * Rainfall - Amount of rainfall received in mm
    * Snowfall - Amount of snowfall received in cm
    * Seasons - Season of the year (Winter, Spring, Summer, Autumn)
    * Holiday - Whether the day is a Holiday or not (Holiday/No holiday)
    * Functional Day -Whether the rental service is available (Yes-Functional hours) or not (No-Non functional hours)

4. Conclusions:

    * Elastic net model understands data properly and hence shows very poor performance with data.
    * linear regression and lasso and ridge with or without hyperparameter tuning show very poor performance with the data (all having almost the same R2_score)
    * By using polynomial regression with degree 2, R2_score improve to 0.8 for train data and 0.77 for test data. Model performance is improved as compared to the earlier model.
    * By using DecisionTreeRegressor with GridSearchCV, training R2_score is 0.99 and for the test, data R2_score is 0.89. Model performance is improved but slightly increase in overfitting.
    * By using RandomForest with GridSearchCV, training R2_score is 0.93 and test R2_score is 0.99. The model is slightly underfitting.
    * By using Gradient Boosting without hyperparameter tuning training R2_score 0.89 and test R2_score 0.90, the model is generalized very well.
    * By using Gradient Boosting with GridSearchCV training R2_score is 0.99 and test R2_score is 0.95 model performance is improved with an accuracy of 0.95. The difference between the R2_score test and train data is so small that it can be neglected and we can deploy this model.

