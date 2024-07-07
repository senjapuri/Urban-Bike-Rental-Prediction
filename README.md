
# Project Title

Urban Bike Rental Prediction

# Description

This project predicts hourly rental bike demand to improve urban mobility. Ensuring a steady bike supply reduces waiting times and enhances accessibility. By forecasting bike availability needs, it provides a reliable and convenient service to the public.

# Data Description

The dataset contains weather information (Temperature, Humidity, Windspeed, Visibility, Dewpoint, Solar radiation, Snowfall, Rainfall),
 the number of bikes rented per hour and date information.

# Attribute information

*  Date : year-month-day
*  Rented Bike count - Count of bikes rented at each hour
* Hour - Hour of he day
*  Temperature-Temperature in Celsius
*  Humidity - %
*  Windspeed - m/s
*  Visibility - 10m
*  Dew point temperature - Celsius
*  Solar radiation - MJ/m2
*  Rainfall - mm
*  Snowfall - cm
*  Seasons - Winter, Spring, Summer, Autumn
* Holiday - Holiday/No holiday
* Functional Day - NoFunc(Non Functional Hours), Fun(Functional hours)


# Summary

Rental bikes have been introduced in many urban cities to enhance mobility. By analyzing the hourly rental data, we observe that demand varies significantly with specific times, seasons, and weather conditions. We have data, including records of different seasons, weather, temperature, rented bike counts, hours, humidity, visibility, solar radiation, rainfall, snowfall, holidays, and functioning days.

First, I performed data preprocessing and exploratory data analysis (EDA). I extracted features from the 'Date' column to obtain the month, day of the week, and whether it was a weekday or weekend. During EDA, I plotted heatmaps for correlation, and conducted univariate and bivariate analyses to gain insights from the data.

After preprocessing, the data was ready for modeling. I used various models to achieve the best accuracy, including Linear Regression, Lasso, Ridge, and ElasticNet Regression, as well as Decision Trees and Random Forest models.

Next, I performed hyperparameter tuning using GridSearchCV on the regularization techniques (Lasso, Ridge, and ElasticNet) to improve accuracy and shrink coefficients. However, this did not yield a significant accuracy improvement.

To gain more insights from the data, I examined feature importance. I found that 'temperature' and 'hour' were the most important variables for the Decision Tree and Random Forest models. 'Solar Radiation' and 'Functioning Day' also showed importance. 'Temperature' emerged as the most crucial feature overall.

Finally, I evaluated the models' performance. Linear Regression, Lasso, Ridge, and ElasticNet Regression showed an accuracy of 56%. The Decision Tree and Random Forest models achieved adjusted R² scores of 77% and 84%, respectively.

Thus, the best model for this dataset achieved an accuracy of 84%. This performance may be influenced by various factors, including data patterns, possible noise in the data, and the varying accuracy of different models.

# Machine Learning (Regression) Data Pipeline

1.	Data Preprocessing

2.	Exploratory Data Analysis

•	Univariate Analysis on numeric features

•	Bivariate Analysis

•	Analysis from categorical variables
                                
3. Fitting different models
                
•	Linear Regression

•	Building Lasso, Ridge and ElasticNet Regression

•	Decision Trees

•	Random Forest

4. Finding best parameters by GridSearchCV in Lasso, Ridge and ElasticNet
   Regression

5. Getting Feature Importance on Decision Tree and Random Forest model

6.    Model Evaluation Metrics

•	Mean square error

•	Root mean square error

•	R2

•	Adjusted R2


# Conclusion

* On holidays or non-working days, there is increased demand for rented bikes.

* In Seoul, people prefer renting bikes at 8 AM and 6 PM, likely commuting to work in the morning and returning home in the evening.

* Among various models tested, the Random Forest model is the best for predicting bike-sharing demand. It shows lower performance metrics (MSE, RMSE) and higher values (R2, adjusted R2).

* People are less likely to rent bikes during rainfall. Similarly, during the winter season with continuous snowfall in Seoul, cold weather negatively impacts bike rentals.

* Temperature, hour, and humidity are the most important features that positively influence the total rented bike count.

* For future predictions, the Random Forest model is recommended over other models.


