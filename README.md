![image](cover.jpg)
# Property Rental Price Prediction: Overview

- Create a tool that functions to provide rental price predictions for various properties based on the features possessed by the property.
- Machine learning regression model is used to predict property rental rates.
- Using data sets of San francisco,CA property rental price.

## Code and Resources Used
**Python Version:** 3.10.3  
**Packages:** pandas, numpy, sklearn, math    
**Dataset source:** Datacamp case study

## Processing Data
After collect Dataset, I need to check and clean up the dataset to makesure no missing and anomaly values on Dataset before creating a Machine Learning model. I made the following changes and created the following variables:

- Import Dataset to Data Frame with pandas.
- Fix datatype of every feature.
- Check and dealing with missing values.
- Cleaning object columns and labeled.
- Analyze and resolve anomaly values.

### Result
*Before resolve anomaly*
![image](https://user-images.githubusercontent.com/98052588/180590704-af36251a-1d7d-456a-9499-5ed354d8a1a6.png)


*After resolve anomaly*
![image](https://user-images.githubusercontent.com/98052588/180590751-9294452c-ff67-40e7-bf53-0f68d54b4679.png)

## Property Location
![Rentals location](https://user-images.githubusercontent.com/98052588/180590896-f675b288-4884-43c8-848a-a8b6930cc2e2.png)
Color represents rental price.

## Data Engineering
From property location we can calculate the distance of property location to downtown. So, i add new feature 'distance'.
Here the heatmap of linear correlation.

![image](https://user-images.githubusercontent.com/98052588/180593158-3d8d1768-b54a-4e74-879a-3cdf2f0d2bcf.png)

## Model Machine Learning
Rank |Model |Score |MAE |RMSE
-----|------|------|----|----
1|RandomForestRegressor|0.575|72.24|132.62
2|GradientBoostingRegressor|0.570|73.16|133.41
3|LinearRegression|0.445|84.19|151.52|
4|Ridge|0.445|84.19|151.51
5|Lasso|0.445|83.69|151.59
6|DecisionTreeRegressor|0.225|91.96|179.02

From several models, RandomForestRegressor obtained the highest accuracy score, with score 57.5%.
and with optimization get results:

Model |Score |MAE |RMSE
------|------|----|----
RandomForestRegressor|0.622|69.23|125.13

## EDA
Feature importance

![image](https://user-images.githubusercontent.com/98052588/180596345-b4527d65-3e5b-4fde-8018-557a872dbfcb.png)

Here we can see that the high and low price of property rental is strongly influenced by the number of rooms and sligly influenced by properti location. 

**More rooms, more prices**.

![image](https://user-images.githubusercontent.com/98052588/180601503-85d0aa71-e70f-459d-9291-9d573647d363.png)

Here sample distribution of predict and actual price rent.

![image](https://user-images.githubusercontent.com/98052588/180601573-beac0b0a-b885-4e55-a8fa-d1538baaeaff.png)
