# Predicting-Stock-Movement-with-NLP-and-Twitter
Create sentiment analysis scores using NLP on tweets related to stocks to predict a stock’s 1 day return

Kyle Johnson

### Project Motivation
The price of a financial asset can be seen as the sum of every market participant's sentiment about that asset.  With the advent of Twitter, we have the largest database of opinions ever seen in human history and in theory, being able to quantify those opinions should give insights into how the future will play out regarding the subject of those opinions.  This project uses Natural Language Processing to quantify the sentiment of tweets about a particular stock while the market is closed in order to predict what the stock will do when the market re-opens for trading.

Please see the notebook titled "Summary_Start_Here" for a detailed road map through this project in order fully understand the process.

### Process Overview
The Twitter data for this project was gathered from an online database along with using the Twitter API.  The tweets were then given a sentiment score using the TextBlob and Vader NLP algorithms and used to make predictions about the given stock.  The stock price data was gathered using the Yahoo Finance API. 



An important thing to note is that only tweets from when the market was closed were used and only stock movement from when the market was open was used. I chose this set up in order to have a clearly defined predictor (overnight Twitter sentiment) and target (intra-day stock price movement). I do not include any tweets from the previous day's market hours because Efficient Market Hypothesis dictates that those sentiments would be priced into the previous day's stock price. I also do not include any overnight stock price movement because that would be using the future to predict the future. For example, if a stock rises during after-hours trading and then the next morning there is positive Twitter sentiment about that stock, then the target would be determining the predictor which leads to a completely useless result.

# Findings

### Abnormally high Tweet volume led to more profitable trades



### Isolating tweets from Twitter users who have predicted well in the past can lead to more profitable trades



# Conclusions:
-Both TextBlob and Vader sentiment analysers show the ability to give useful insight into stock movement.

-Using sentiment analysis on trades with a high tweet volume relative to each stock's average is a consistently effective strategy.

-Forming sentiment scores using only tweeters with high recent accuracy is an effective strategy.

-The data used for this project has two main limitations that would need to be addressed before deploying these strategies into the live capital markets.

    -Majority of data is significantly out of date.
  
    -Recent data is of very limited scope due to limitations on the use of the free version of the Twitter API connection.
# Further Exploration:
-Acquire a paid Twitter Developer subscription in order to gather much more recent data.

-Explore other sentiment engines such as Google's to find the best performing one.

-Create a "voting" system that consideres sentiment scores of several different algorithms into a single score.
