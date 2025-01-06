# TechETFCryptoCorrelations

Short study to review any correlation between major technology ETF index vs Cryptocurrency


# Libraries Used: 

    pandas

    numpy

    yfinance

    datetime

    matplotlib

    sklearn

    seaborn



# Project Brief:

// Predicitng the stock market (or our chosen securities): //

Where predicting the direction of a stock is a binary decision: 

    Will it go:
        
        Up?
        
        Down? 

Naturally we are trying to buy low and sell high -- possibly Machine Learning can help us here.



This is an oversimplification, however where we consider that flipping a coin is a binary decision, 

statistically, where flipped enough times, we will see heads and tails equally appear 50% of the time. 

    - This gives us 50% accuracy as our baseline for 0.

Given that, an accuracy of 50% is the same as if we were to assign Heads = Up and Tails = Down and apply that logic to whether we invest or not. 


# The Purpose:

Can:

A: Predict whether our chosen securities will be up/down after 14 days if presented with ~10 years of historical data for each. 

B: Use the relationships across VIT (yfTicker: 'VGT') and BTC (yfTicker: 'BTC-USD' - Cryptocurrency known for volatility) to better predict the direction of either in any way. 



The goal then is for our models to be able to predict the direction of either stock >50% of the time 14 days into the future. 


# The Method:

Therefore this project seeks to determine whether a simple LinearRegression model: 

    - Using ~10 years of historical data acquired via Yahoo Finance .api (yfinance).

    - For BTC (Cryptocurrency known for volatility)

    - For VIT (Vanguard Information Technology Index Fund ETF -- Based on US IT company stock values)


# The Outcome: 

As stated, predictions on stock direction must be at least 50% accurate to be considered more useful than guessing.

We can see that individual analyses yield around a ~65% accuracy for each separately, which implies that this model is able to guess accurately the majority of the time. 

When we bring the datasets for each stock together to train we can see equally that the model is confused given the variance in values, with <50% accuracy.

However, when we normalise the stock movements on percentages, where the minimum values = 0% for each and the maximum values = 100% we see > 70% accuracy.

This implies that the datasets can inform each other, and that training the model on both, despite the volatility of BTC, can provide more accurate predictions that a guess.


# Further Research:

The methodology, technology applied in this research is very basic.

I believe more advanced methodology could yield much more impressive results. 

Recommendations for future research: 

- Include more, different stock data
- Review timescales analysed, reduce the amount of time series data used to train
- Use different technologies, such as more advanced modelling and neural networks


# Contributing: 

This project was completed as part of an academic course and there is no intention to update. 

You are free to use any of the content from this Repository that may be useful, or build on it as you please. 

There is no intention to include any contributions to this project. 
