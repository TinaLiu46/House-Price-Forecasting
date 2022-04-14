# House-Price-Forecasting

## Table of Contents
1. [Data Description](#data-description)
3. [Objective](#objective)
4. [Initial Exploration](#initial-exploration)
5. [Models](#models)
    1. [Univariable Model](#univariable-model)
    2. [Multivariable Model](#multivariable-model)
7. [Conclusion & Lesson Learned](#conclusion-and-lesson-learned)

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

## Models

### Univariable Model
C
### Univariable Model
### Univariable Model
- Step1 : Keep differencing the data until it reaches stationary.
- Step2 : Choose best ARIMA model candidate based on BIC score
- Step3 : Grid-search

### Multivariable Model
