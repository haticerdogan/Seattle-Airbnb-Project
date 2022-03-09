# Seattle Airbnb Booking Rate Prediction

Author: Hatice K. Erdogan 

![airbnb](https://user-images.githubusercontent.com/94992749/157332174-7778c589-747a-4112-ab0f-6ae54368acb8.jpeg)

## Overview 

Airbnb is an online platform that makes it easy to list and rent local homes by connecting hosts and guests. Seattle, WA is one of the most urban and modern cities in th United States. As many people visit Seattle, demand for searching and booking Airbnb listings increases but when and by how much. 

## Business Problem 

The goal of this project is to build a Machine Learning pipeline using regression algorithms that predicts the booking rate of Airbnb lisitings in Seattle area. Models predicts the mean booking rate for a given property listing for the year. The independent variables affecting the booking rate of listings consists of 3 components: 

1) Numerical columns such as cleaning fee, price and price for extra people.
2) Categorical columns such as whether host of a particular listing is a superhost or not, bed type, and property type.
3) Text columns that give an overview of each listing on Airbnb which are preprocessed and vectorized using Natural Language Processing (NLP). 


## Data & Methods 

The data source is Airbnb with 2 datasets:

- calendar: daily availability of each listing throughout the year 2016 to 2017 along with the listed prices per night.<br/>
  1.4 million rows & 4 columns
  
- listings: information about each listing such as descriptions and details of the property and host, review scores, location.<br/>
  3818 rows & 92 columns
 
## Results 

With my final model, the Mean Squared Error (MSE) is only making % 11 errors when predicting the booking rate. The best model was Extra Trees Regressor followed by Random Forest Regressor, with MSE score of % 12. The models were ran through a pipeline with RandomizedSearchCV to find the optimal hyperparameters with lowest MSE scores. 

The most important that affect the booking rate  are:
1) Listing Descriptions
2) Room Type
3) Host Response Time

## Installation & Requirements

The code is written in Python 3.8. To run the notebooks, you will need to install necessary libraries and packages: Seaborn, NLTK, Wordcloud, contractions, stopwords, wordnets and its dependencies using pip install or conda install. 

## References & Credits 

Below are the resources that helped me in some parts of this project. I would like to thank these authors for their work and articles. 

1) 
