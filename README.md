# Predicting-Stock-Movement-with-NLP-and-Twitter
Create sentiment analysis scores using NLP on tweets related to stocks to predict a stock’s 1 day return

Kyle Johnson

Flatiron School Final Project

## Objective:
The precise objective of this project is to predict a stock's price movement from the open to the close of the current trading day based only on tweets from the previous close of trading until the opening bell of the current day. I chose this set up in order to have a clearly defined predictor (overnight Twitter sentiment) and target (intra-day stock price movement). I do not include any tweets from the previous day's market hours because Efficient Market Hypothesis dictates that those sentiments would be priced into the previous day's stock price. I also do not include any overnight stock price movement because that would be using the future to predict the future. For example, if a stock rises during after-hours trading and then the next morning there is positive Twitter sentiment about that stock, then the target would be determining the predictor which leads to a completely useless result.

This project breaks down into two parts. Part 1 uses a database of tweets from 2016 and part 2 uses current tweets gathered from Twitter's API. Please follow along with these notebooks that detail this process:

# Part 1 - Archived Tweets
### Notebook 1 - Data Gathering of Archived Tweets
In this notebook I source tweets about the stocks in the NASDAQ 100 Index for a period of 90 days in mid 2016.

### Notebook 2 - Archived Tweet Analysis
In this notebook I use the data frames created in the previous notebook to determine the usefulness of using Natural Language Processing in the aim of predicting stock price movements.

### Notebook 3 - Isolating the Best Tweeters
In this notebook I give each tweeter (username) a score based on their sentiment's ability to accurately forcast stock price movement. I then isolate those tweeters with the highest scores and make new predictions

# Part 2 - Live Tweets
### Notebook 4 - Gathering Live Tweets
In this notebook I use the Twitter API to gather tweets from the last two weeks until the current moment. Unfortunately the free version of Twitter's API only allows the gathering of 1 week's worth of data, however the code would be the same for a paid version that could gather more data.

### Notebook 5 - Live Tweet Analysis
In this notebook I perform the same analysis on live tweets as was performed on the archived tweets in Notebook 2.

### Notebook 6 - Isolating the Best Live Tweeters
In this notebook I perform the same analysis on live tweets as was performed on the archived tweets in Notebook 3.

# Conclusions:
-Both TextBlob and Vader sentiment analysers show the ability to give useful insight into stock movement.

-Using sentiment analysis on trades with a high tweet volume relative to each stock's average is a consistently effective strategy.

-Forming sentiment scores using only tweeters with high recent accuracy is an effective strategy.

-The data used for this project has two main limitations that would need to be addressed before deploying these strategies into the live capital markets.

  -Majority of data is significantly out of date.
  
  -Recent data is of very limited scope.
# Further Exploration:
-Acquire a paid Twitter Developer subscription in order to gather much more recent data.

-Explore other sentiment engines such as Google's to find the best performing one.

-Create a "voting" system that consideres sentiment scores of several different algorithms into a single score.
