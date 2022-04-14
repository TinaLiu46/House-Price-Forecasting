# House-Price-Forecasting

## Table of Contents
1. [Data Description](#data-description)
3. [Objective](#objective)
4. [Initial Exploration](#initial-exploration)
5. [Models](#models)
    1. [Univariable Model](#univariable-model)
    2. [Multivariable Model](#multivariable-model)
7. [Conclusion](#conclusion)

## 📋Data Description
  The Zillow dataset (modified) recorded 
  - Feb 2008 - Dec 2015 monthly median sold price for housing in California
  - Feb 2008 - Dec 2016 monthly median mortgage rate
  - Feb 2008 - Dec 2016 monthly unemployment rate

## 📑Objective
  Explore the dataset and use time series analysis to find model to __forecast the monthly median sold price for Jan - Dec 2016__.

## 📉Initial Exploration

![Goal2](https://github.com/TinaLiu46/House-Price-Forecasting/blob/main/Images/time1.png?raw=true "Title")
![Goal2](https://github.com/TinaLiu46/House-Price-Forecasting/blob/main/Images/time2.png?raw=true "Title")

By plotting time series, ACF, and PACF plots as well as Augmented Dickey–Fuller test , we tried identify if the time series data is stationary or if it contains any seasonality. In next step, we will move to select our models based on the result of this step.

## 🚀Models

### Univariable Model

Three candidates of ARIMA models:
- Find best ARIMA model candidate for one-differenced data based on BIC - __ARIMA(0,1,0)__
- Grid search to find the best model using the original data set based on BIC - __ARIMA(0,2,4)__
- Auto_arima function to derive last model candidate based on AIC - __ARIMA(1,2,0)__

Then, we used cross validation with the train and validation set to determine the best ARMIA model based on __RMSE__
|  | RMSE | 
| ------------- | ------------- |
| ARIMA(0,1,0) | 8474 |
| ARIMA(0,2,4) | 10774 |
| ARIMA(1,2,0) | 10661 |

From the output above, we can concluded that first candidate ARIMA(0,1,0) has the best performance based on RMSE. Below is the forcast using this model
![Goal2](https://github.com/TinaLiu46/House-Price-Forecasting/blob/main/Images/time3.png?raw=true "Title")

### Multivariable Model
- VAR model
- SARIMAX model

|  | RMSE | 
| ------------- | ------------- |
| VAR | 33398 |
| SARIMAX | 9168 |

Below is the forcast using SARIMAX model
![Goal2](https://github.com/TinaLiu46/House-Price-Forecasting/blob/main/Images/time4.png?raw=true "Title")


## 💡Conclusion
We explored both univariable and multivariable time series model using consistent training, validation and test set. We found that multivariable had a better performance to forecast monthly median sell price from January to December 2016 based on both prediction graphs and RMSE. As SARIMAX model did consider other variables, (MedianMortageRate and UnemploymentRate) in the dataset to forecast the house sold price and had better performance than ARIMA model, it suggested that mortgage rate and unemployment rate might have some effect on the median house sold price in 2016.
