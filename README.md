[![forthebadge](https://forthebadge.com/images/badges/made-with-python.svg)](https://forthebadge.com)

# Restaurant Recommendation System

## CMPE 256 Group Project

![](/5.Archive/images/restaurant_image_header.jpeg)

## Contents

- [Understanding recommendation system](#understanding-recommendation-system)
- [Quick start](#quick-start)
- [Folder Structure](#folder-structure)
- [Installation](#installation)
- [Steps to run the project](#steps-to-run-the-project)
- [Dataset](#Dataset)
- [System Design](#system-design)
- [Methodologies Used](#medthologies-used)
- [Conclusion](#Conclusion)
- [Contributors](#Contributors)
- [License](#License)

## Understanding recommendation system

## Quick start

### Folder Structure

### Installation

Installation of below packages required before running the project

- `pip install -r requirements.txt`

### Steps to run the project

1. Create a folder in local for Above Git Repo and open in termianl to execute below commands-

$ git clone https://github.com/divyaKh/CMPE256Project.git

2. Navigate to folder EDA and run all ipynb file for business, reviews and users dataset in jupyter notebook or google colab

3. Navigate to folder Data_Cleaning and all ipynb in jupyter notebook or google colab

4. Navigate to folder Recommdation_System and run all ipynb in jupyter notebook to execute different recommendationsystem models


## Dataset

Yelp Dataset: https://www.yelp.com/dataset

Yelp data is derived from Yelp Open Dataset. It contains 1.2 million business attributes,1,987,897 users and 131,930 businesses. we would be using the following json files from the dataset:

Data Dictionary:

Review dataset: Contains review text data consisting of id for user who wrote the review and the business the review is written for, as well the rating.
Business dataset: Contains information about the different business’s location, business type, attributes, categories, stars rated, etc.
User dataset: All the user data example user id, user name, reviews given, year, etc.

## System Design

![](/5.Archive/images/system_design.png)

Step 1: Data Preprocessing:
Yelp's dataset is huge, so data preprocessing is the vital part of our project. Yelp dataset contains data files i.e., Business, Users and Reviews in JSON format. We did data preprocessing for all these files. Our data preprocessing includes data cleaning by filling the missing values, eliminating repeated values, data transformation by constructing new attributes from the given data and data reduction by filtering restaurant data only from the state of California. The cleaned data is then stored in separate CSV files for business, users, and reviews.

Step 2: Exploratory Data Analysis:
EDA is one of the critical steps in our project. EDA helped us to discover patterns, spot anomalies in the data. We did EDA for business, users, and reviews separately. The processed files from data preprocessing are used for EDA. We have used python libraries like seaborn, Matplotlib, plotly and word cloud to visualize the data and to draw the conclusions from the data.

Step 3: Model Evaluation and Predictions:
In this step, we divide the data into test and train and fed the data to different machine learning recommender models. We performed hyper parameter tuning to get the best parameters for the recommender models. We have used RMSE as a performance indicator of our models.

## Methodologies Used

For the recommendation models, we preprocessed and split the dataset into test and training sets. Based on the  below table, we are able to pick the top performing for our hybrid model and then used GridSearchCV function from the surprise library that provides an easy way to tune and select the best hyperparameters to achieve best RMSE Scores.For the GridSearchCV, we provided a set of options for each model parameter and the function checks all the parameter combinations for the best parameters.  We evaluated three different KNN models namely, KNNBasic, KNNWithMeans, KNNBaseline, BaselineOnly, SVD and SVDpp for the restaurant recommendation system. We are using the K-Fold validation technique to eliminate any bias in test and training set choices. 

### Sentiment Analysis

We also performed sentiment analysis of the reviews rather than just taking their star ratings for the restaurants. We used the textblob library for sentiment analysis which gives two types of scores for every user review. One is the sentiment score and the other is the subjectivity or polarity score. The sentiment score is in the range of -1 to 1, where -1 represents a very negative sentiment and vice versa. The polarity scores are in the range of 0 to 1, where 1 means the review is very subjective. We filtered out the reviews that have more than 0.6 polarity and with sentiment scores between -0.2 to 0.2. The intuition is that reviews with too much polarity are biased and reviews that are mostly neutral will not have much value in the recommendation model. 


## Conclusion

1. Without hyperparameter tuning, the top performing model was BaselineOnly with RMSE as 0.941.
2. With hyperparameter tuning, the top performing model was also BaselineOnly with RMSE as 0.916. It was observed that SVD also gave a good RMSE score of 0.921.
3. Sentiment analysis of user reviews give better performing models than simply relying on user star ratings.


### Contributors

- [Archita Chakraborty](https://github.com/Archita22ind)
- [Divya Khandelwal](https://github.com/divyaKh)
- [Priyanka NAM](https://github.com/Priyanka-NAM)

## License
