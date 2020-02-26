# Data_Wrangling_Project
Udacity Data Analysis Nanodegree project on data wrangling

## Skills
- Download a file programmatically via the requests library.
- Query the twitter API via the tweepy library and save the json data to a file.
- Read csv files with pandas.
- Read a json lines file with pandas.

## Introduction
This project is part of the Udacity’s Data Analyst Nanodegree. The goal of the project is to apply all our knowledge in data wrangling. All the data is from the twitter account called WeRateDogs that gives rates to people’s dogs.  The project steps include:

- Data wrangling, which consists of:
1) Gathering data
2) Assessing data
3) Cleaning data.
- Storing, analyzing, and visualizing the wrangled data.
- Reporting on the data wrangling efforts (this report) and the data analyses and visualizations.

## Gathering data
The data has been gathered from three different sources:
- The WeRateDogs Twitter archive which is given to us by Udacity in a csv file (twitter-archive-enhanced.csv). This archive contains basic information for more than 5000 tweets and we download it manually. 
- The prediction data contains the breed prediction (the first three) from a neural network for a big part of the archive tweets. This file (image-predictions.tsv) was provided by Udacity via a url and has to be downloaded programmatically via a request.
- All the data provided from Twitter for each tweet has been gathered via the Twitter API using the Tweepy library. Each tweet’s entire set of JSON data is stored in a line of a .txt file (tweet_json.txt).

All three files are then readed into a DataFrame.

## Assessing data
The data was assessed in two ways:
- Visual Assessment: the DataFrames were printed in the Jupyter notebook with the head, tail and sample methods.
- Programmatic Assessment: DataFrames were assessed with a variety of methods such as info, describe, value_counts, duplicated, among others and attributes like dtypes.

The assessment ends with a detailed list of the issues found in the data. This issues are group in two groups:
- Quality issues
- Tidiness issues

## Cleaning data
The cleaning process was done in three steps (with a few exceptions needed to continue):
- Make a copy of the original DataFrames.
- Handle the missing data.
- Solve the tidiness issues.
- Address the remaining quality issues.

This process involved a lot of methods such as drop, merge, melt and replace.

## Storing data
The two final DataFrames were stored in csv files: twitter_archive_master.csv and twitter_archive_tweetdetails.csv. 

## Inclusion criteria
Is important to clarify that not all the original data in the twitter-archive-enhanced.csv was used.  We only keeped the tweets with this requirements:
- Original tweets (no retweets).
- Tweets with a dog stage prediction in the image-predictions.tsv file.
- Tweets with the JSON data obtained via the API. 
