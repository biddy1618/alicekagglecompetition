# Jupyter Notebook for in-class Kaggle competition

## Description
This competition was a part of <h path='opendatascience.com'>ODS</h> course.

## Short description
Web-user identification is a hot research topic on the brink of sequential pattern mining and behavioral psychology.

Here we try to identify a user on the Internet tracking his/her sequence of attended Web pages. The algorithm to be built will take a webpage session (a sequence of webpages attended consequently by the same person) and predict whether it belongs to Alice or somebody else.

The data comes from Blaise Pascal University proxy servers. Paper "A Tool for Classification of Sequential Data" by Giacomo Kahn, Yannick Loiseau and Olivier Raynaud.

## Results and conclusion

As for 23.12.18, my current LB standing is 87th out of 2000ish.

So, for this competition the data was time-series session info regarding user browser history - we have to distinct between regular user and intruder user based on sites visitied and time of visit information. EDA, data wrangling and feature engineering was performed to achieve ROC-AUC score of 0.95856. Currently implemented features:

* Dummy hour feature of session start time (from now on start time)
* Sin-cos transformation of start time
* Active start hours of intruder
* Dummy weekday feature of start time
* Active weekday of intruder feature
* Dummy month feature of start time
* Sin-cos transformation of year day feature
* Session length
* Session sites stay standard deviation

__TODO__: add features based on site:

* Number of unique sites visited feature
* Features based on most intruder visited sites
* Data wrangling on names of features (like www.google.com and google.com are the same)
* Somehow perform polynomial features

Let's move further now. We will revisit this notebook once I have more experience with Time-series data.
