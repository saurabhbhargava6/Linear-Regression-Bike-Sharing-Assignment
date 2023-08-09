# Linear-Regression-Bike-Sharing-Assignment
This assignment is a programming assignment wherein you have to build a multiple linear regression model for the prediction of demand for shared bikes. You will need to submit a Jupyter notebook for the same.


## Table of Contents
* [Bike Sharing Assignment Intro](#bike-sharing-assignment-intro)
* [Business Goals](#business-goals)
* [Data Preparation](#data-preparation)
* [Model Building](#model-building)
* [Model Evaluation](#model-evaluation)
* [Conclusions](#conclusions)
* [Technologies Used](#technologies-used)
* [Contact](#contact)
* [Acknowledgements](#acknowledgements)

<!-- You can include any other section that is pertinent to your problem -->
## Bike Sharing Assignment Intro
This is an assignment wherein a multiple linear regression model is expected to be built, to predict demand for bikes depending on the current trend.

In this programming task, you will create a multiple linear regression model that can estimate the demand for shared bikes based on the current trend. Shared bikes are bikes that people can rent and use for a short time, either for free or for a fee. They can pick up a bike from a computerized station, where they enter their payment information and get a code to unlock the bike. They can then drop off the bike at another station that belongs to the same system.

## Business Goals
The primary aim of this project is to create a multiple linear regression model that can forecast the demand for shared bikes using the available explanatory variables. This predictive tool will assist management in understanding how demand fluctuates in response to various factors. Consequently, they can adapt their business strategy to align with demand patterns and enhance customer satisfaction. Additionally, the model will prove invaluable for management in comprehending demand patterns in new markets.

##  Data Preparation
Within the dataset, certain features such as 'weathersit' and 'season' are represented by numerical values 1, 2, 3, and 4, corresponding to different categories (refer to the data dictionary for explanations). However, it's important to note that these numbers do not imply any inherent order or ranking among the categories (inspect the data dictionary to understand why). Therefore, it's advisable to convert these numerical values into categorical text labels before constructing the model. Be sure to review the data dictionary for a more comprehensive understanding of all independent variables. Additionally, observe the 'yr' feature, which assumes values 0 and 1 representing the years 2018 and 2019 respectively. While it might seem logical to omit this feature due to its binary nature, it's worth considering that the demand for these bike-sharing systems is growing annually. Thus, the 'yr' feature might serve as a valuable predictor.



## Model Building
The dataset encompasses three features: 'casual', 'registered', and 'cnt'. 'Casual' signifies the count of non-registered users who rented a bike, while 'registered' corresponds to the count of registered users who reserved a bike on a given day. The 'cnt' feature aggregates the total number of bike rentals, encompassing both casual and registered users. Your model-building efforts should revolve around predicting this 'cnt' variable.

## Model Evaluation
After you have built the model and analyzed the residuals and made predictions on the test set, please make sure you use these two lines of code to find out the R-squared score on the test set:

```python
from sklearn.metrics import r2_score
r2_score(y_test, y_pred)
```

where y_test is the test data set for the target variable, and y_pred is the variable containing the predicted values of the target variable on the test set.


## Conclusion

Significant variables to predict the demand for shared bikes

- holiday
- temp
- Season
- months(January, July, September, November, December)
- Year (2019)
- weathersit( Light Snow, Mist + Cloudy)

We can see that the equation for best fitted line is:
```cnt = 0.0750 + 0.2344 * year + 0.0555 * workingday +  0.4796 * temp  + 0.0873 * sep + 0.0667 * sat + 0.1180 * summer + 0.0554 * fall + 0.1512 * winter - 0.0804 * Misty -0.2893 * Light_snowrain - 0.1500 * windspeed```

**Comparison between Training and Testing dataset:**

| **Item**              | **Train Data Set** | **Test Data Set** |
| --------------------- | -------------------| -------------     |
| Train R-squared:      | 0.835              |  0.7961           |
| Train Adj. R-squared: | 0.832              |  0.7864           |


## Technologies-Used
- pandas - version 1.5.3
- seaborn - version 0.12.2
- scikit-learn - version 1.2.2
- numpy - version 1.23.5
- matplotlib - version 3.7.1
- statsmodels - version 0.13.5
- Python Version - version  3.10.12

## Contact
Created by [@saurabhbhargava6] - feel free to contact me!

## Acknowledgements
Give credit here.
- https://seaborn.pydata.org/
- https://pandas.pydata.org/
- https://learn.upgrad.com/
- https://github.com/ContentUpgrad/Linear-Regression/tree/main 

