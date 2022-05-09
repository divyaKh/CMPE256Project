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

## Dataset

Yelp Dataset: https://www.yelp.com/dataset

Yelp data is derived from Yelp Open Dataset. It contains 1.2 million business attributes,1,987,897 users and 131,930 businesses. we would be using the following json files from the dataset:

Data Dictionary:

Review dataset: Contains review text data consisting of id for user who wrote the review and the business the review is written for, as well the rating.
Business dataset: Contains information about the different business’s location, business type, attributes, categories, stars rated, etc.
User dataset: All the user data example user id, user name, reviews given, year, etc.

## System Design

![](/5.Archive/images/system_design.jpeg)

Step 1: Data Preprocessing:
Yelp's dataset is huge, so data preprocessing is the vital part of our project. Yelp dataset contains data files i.e., Business, Users and Reviews in JSON format. We did data preprocessing for all these files. Our data preprocessing includes data cleaning by filling the missing values, eliminating repeated values, data transformation by constructing new attributes from the given data and data reduction by filtering restaurant data only from the state of California. The cleaned data is then stored in separate CSV files for business, users, and reviews.
Step 2: Exploratory Data Analysis
EDA is one of the critical steps in our project. EDA helped us to discover patterns, spot anomalies in the data. We did EDA for business, users, and reviews separately. The processed files from data preprocessing are used for EDA. We have used python libraries like seaborn, Matplotlib, plotly and word cloud to visualize the data and to draw the conclusions from the data.
Step 3: Model Evaluation and Predictions
In this step, we divide the data into test and train and fed the data to different machine learning recommender models. We performed hyper parameter tuning to get the best parameters for the recommender models. We have used RMSE as a performance indicator of our models.

## Methodologies Used

## Conclusion

### Contributors

- [Archita Chakraborty](https://github.com/Archita22ind)
- [Divya Khandelwal](https://github.com/divyaKh)
- [Priyanka NAM](https://github.com/Priyanka-NAM)

## License
