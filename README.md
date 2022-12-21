# Bike-Sharing-Demand-Prediction

## Table of Content

1. Introduction
2. Problem Statement
3. Dataset Information
4.  Conclusion
*****
1. Introduction

  Bike sharing system is an innovative transportation strategy that provides individuals with bikes for their common use on a short-term basis for a price or for free.   Over the last few decades, there has been a significant increase in the popularity of bike-sharing systems all over the world. This is because it is an                 environmentally sustainable, convenient and economical way of improving urban mobility. In addition to this, this system also helps to promote healthier habits among   its users and reduce fuel consumption.
The goals of this project are:
    * Understand the trends in the data and identify key factors affecting the hourly demand for rental bikes.
    * Build an appropriate regression model to forecast the number of rental bikes required per hour.

2. Problem Statement

  With the growing demand and user base for bike-sharing system, providing the city with a stable supply of rental bikes could eventually become a challenging task. The success of bike-sharing system relies in ensuring that the quality of facilities provided, meets the needs and expectations of the users. Therefore, it is important to ensure that rental bikes are available and accessible to the users at right time ,as it reduces the waiting time. Forecasting the number of bikes required and identifying the key factors that influence the demand for rental bikes can greatly help in managing the bike-sharing system.

3.  Dataset information

  Dataset used in this project is the Seoul Bike Share program data.This dataset contains information about the total count of rented bikes at each hour, as well as the date of observation and meteorological information (Humidity, Snowfall, Rainfall, Temperature Season, and so on) for that hour. The observations in the dataset  were recorded during a span of 365 days, from December 2017 to November 2018.

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
        * Rented Bike count - Count of bikes rented at each hour (target variable)
      

4. Conclusions:

      * Temperature and Hour have a strong correlation with the count of rented bikes.
      * Dew point temperature is highly positively correlated to the Temperature.
      * Over the weekend and during holidays, rental bike demand decreases.
      * There is a significant drop in the number of rented bikes during Winters(Dec-Feb) because it's freezing cold!
      * The demand for bikes increases during warmer temperatures,which is why there's maximum count of rented bikes during the Summer season.
      * In all seasons,the peak demands for rental bikes occur on the opening (8-9 AM) and closing times (6-7pm) of offices and institutions.
      * Elastic net model understand data properly hence show very poor performance with data.
      * linear regression and lasso and ridge with or without hyperparameter tuning shows very poor performance with the data (all having almost same R2_score)
      * By using polynomial regression with degree 2, R2_score improve to 0.8 for train data and 0.77 for test data.Model performance is improved as compare to earlier model.
      * By using DecisionTreeRegressor with GridSearchCV, training R2_score is 0.99 and for test data R2_score is 0.89. Model performance is improved but slightly increase in overfitting.
      * By using RandomForest with GridSearchCV, training R2_score is 0.93 and test R2_score is 0.99. Model is slightly underfitting.
      * By using Gradient Boosting without hyperparameter tuning training R2_score 0.89 and test R2_score is 0.90, model is generalized very well.
      * By using Gradient Boosting with GridSearchCV training R2_score is 0.99 and test R2_score is 0.95 model performance is improved with a accuracy of 0.95.
