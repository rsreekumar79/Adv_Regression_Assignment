# US realtor in Australia - predict value of properties to decide whether to invest or not.
> The aim of the project is to arrive at a multiple linear regression model with regularization using python and associated data analysis/regression/statistics libraries to predict actual value of the prospective properties and decide whether to invest in them or not. The analysis and model building is to be done for a US based realtor with prospects of investment in Australia. A data set with the data dictionary with around 1400+ data points are provided for the analysis with 80 feature variables. The goal is to arrive at a regression model with regularization and with an r2 score on the test data almost equal to the r2 score on the training data. 


## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)
* [Acknowledgements](#acknowledgements)

<!-- You can include any other section that is pertinent to your problem -->

## General Information
- General Info: The project is to arrive at a reasonably good linear regression model able to predict the actual value of prospective properties. This value is used to decide whether to invest or not in the property. The exercise is for a US based housing company Surprise Holding. They have decided to enter the Australian market. Their plan is to buy houses at low prices and re-sell for a profit. The company uses data analytics to predcit the value of houses it plans to buy. A data set is provided with a datakey based on a survey. Predictive analysis to to be done to arrive at a best possible linear regression model considering the influential predictor variables from the data set. 
- Background: A US based realtor Surprise Holding is entering the Australian housing market. Their business plan is to buy properties at a low price and re-sell for a profit. The company wants to have a linear regression model to predict the house price based on various factors.
- Business Problem: it is required to model the value of the property (target variable) with the available independent variables(predictor variables). The model will help to predict house price based on various factors available. The company wants to know 
    - Which variables are significant in predicting the price of a house, and
    - How well those variables describe the price of a house. 
- Dataset being used: Data set provided has variables pertaining to the property like the locality, quality of various aspects like the garage, fireplace, how many rooms, quality of the property, basement details, year of build, year of modification etc. The target variable is the property value.

<!-- You don't have to answer all the questions - just the ones relevant to your project. -->

## Conclusions
### Conclusions:<br>
- It can be seen that r2 score and other metrics of test and train data in case of linear regression model is not at all comparable hinting at overfitting.<br>
- Both Ridge and Lasso models yielded comparable metric values for r2 score and other metrics for training and test data. This implies a better well fit trustworthy model.<br>
- Though values of metrics of Ridge and Lasso are comparable, Ridge model is marginally better since the r2 scores are better for Ridge model as can be seen from the above table.<br>
- 4 nos features are commonly found to be having high influence in both ridge and lasso models, those are<br><br>
    - 'BsmtFinSF1',<br>
    - 'Neighborhood_StoneBr',<br>
    - 'OverallQual_9',<br>
    - 'GrLivArea'<br>
- Considering model simplicity LASSO is the preferred one, explanation is given below.<br>
	It has reduced the coefficients of 135 nos of variables to zero. Lasso regression model	inherently is a feature selection model when compared to ridge model. In this specific case of 	assignment, ridge model reduces the number of features only by 11, in comparison to lasso 	where 135 nos were reduced.
    
    - Total number of non-zero feature coefficients in Lasso model: 237 – 135 = 102 features<br>
    - Total number of non-zero feature coefficients in Ridge model: 237 – 11 = 126 features<br>
- Looking at the complexity of the models, lasso model is much simpler, and has comparable 	metrics too. The Lasso model with the chosen variables describes almost 89.5% of the predictions which is a good score.<br>
So, giving an upper hand to simpler models and also considering the metrics, LASSO model is the preferred on this use case.
- The five most influential variables from the Lasso model are given below.
    - TotalBsmtSF
    - BsmtFinSF1
    - Neighborhood_StoneBr
    - OverallQual_9
    - GrLivArea


<!-- You don't have to answer all the questions - just the ones relevant to your project. -->


## Technologies Used
- Python version 3.8.10
- pandas version 2.0.3
- numpy version 1.23.5
- seaborn version 0.13.0
- matplotlib version 3.5.3
- sklearn-crfsuite version 0.3.6

<!-- As the libraries versions keep on changing, it is recommended to mention the version of library used in this project -->

## Acknowledgements
- https://pandas.pydata.org/pandas-docs/stable/index.html
- https://numpy.org/doc/
- https://seaborn.pydata.org/
- https://plotly.com/python/plotly-express/
- https://matplotlib.org/
- https://scikit-learn.org/stable/index.html

## Contact
Created by Sreekumar R (https://github.com/rsreekumar79)


<!-- Optional -->
<!-- ## License -->
<!-- This project is open source and available under the [... License](). -->

<!-- You don't have to include all sections - just the one's relevant to your project -->