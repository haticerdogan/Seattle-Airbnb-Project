# Seattle Airbnb Booking Rate Prediction

Author: Hatice K. Erdogan 

![airbnb](https://user-images.githubusercontent.com/94992749/157332174-7778c589-747a-4112-ab0f-6ae54368acb8.jpeg)

## Overview 

Airbnb, which is short for "Air Bed and Breakfast", is an online platform that makes it easy to list and rent local homes by connecting hosts and guests. Seattle, WA is one of the most urban and modern cities in th United States. As many people visit Seattle, demand for searching and booking Airbnb listings increases. 


## Business Problem 

The purpose of this project is to predict the booking rates of listings based on their features and provide Airbnb hosts with insights that will increase both booking rates and guests' pleasure with valuable improvements.


## Data & Methods 

The data source is Inside Airbnb with 2 datasets:

- calendar: daily availability of each listing throughout the year 2016 to 2017 along with the listed prices per night.<br/>
  1.4 million rows & 4 columns
  
- listings: information about each listing such as descriptions and details of the property and host, review scores, location.<br/>
  3818 rows & 92 columns
 

The process starts with cleaning the data, pre-processing and vectorizing the text columns followed by a Machine Learning pipeline using regression algorithms that predict the booking rate of Airbnb listings in the Seattle Metro area. Models predict the mean booking rate for a given property listing for the year. Baseline regression models are evaluated first, then hyperparameters are tuned with RandomizedSeachCV to find the optimal hyperparameters with the lowest cross validated Mean Squared Error (MSE). The independent variables affecting the booking rate of listings consists of 3 components:

1) Text columns that provide an overview of each listing on Airbnb which are preprocessed and vectorized using Natural Language Processing (NLP).
2) Numerical columns such as cleaning fee, daily price and price for additional people.
3) Categorical columns such as whether host of a particular listing is a superhost or not, bed type, and property type.

## Results 

Support Vector Regression and Random Forest were the two best performing models on test data with Mean Squared Error of 10.8. Although Random Forest scored 0.11 on cross validation whereas SVR scored 0.10, it is important to evaluate what features contribute the most to booking rates with the two models.

We see that different features have various effects on different models. Price followed by room type and number of bedrooms were the top predictors in SVR model whereas descriptions (NLP text data describing listings), number of reviews and room type were the top predictors in Random Forest. Descriptions have very large effect on booking rates at 12% compared to other features in Random Forest model. However we see that price has less effect 9.5% in SVR compared to descriptions in Random Forest model. We also see that room type is one of the top predictors in both models.


The most important features with SVR model:   
1) Price
2) Room Type 
3) Number of Bedrooms


The most important features with Random Forest model:                 
1) Listing Descriptions
2) Number of Reviews
3) Room Type


As a result, we can conlude that listing descriptions, price, room type, number of reviews and number of bedrooms are the top contibutors to booking rate. To hosts who want to increase their booking rate, I suggest putting more emphasis on these features, such as being more descriptive on their listing summary, lowering price during peak times such as summer and also getting more positive reviews by providing their guests a pleasant experience.

## Installation & Requirements

The code is written in Python 3.8. To run the notebooks, you will need to install necessary libraries and packages: Seaborn, NLTK, Wordcloud, contractions, stopwords, wordnets and its dependencies using pip install or conda install. 

## References & Credits 

Below are the resources that helped me in some parts of this project. I would like to thank these authors for their work and articles. 

1) 
