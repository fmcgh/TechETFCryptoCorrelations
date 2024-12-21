# TechETFCryptoCorrelations
Short study to review any correlation between major technology ETF index vs Cryptocurrency


Libraries Used: 

    pandas
    numpy
    yfinance
    datetime
    matplotlib
    sklearn
    seaborn


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



Therefore this project seeks to determine whether a simple LinearRegression model: 

    - Using ~10 years of historical data acquired via Yahoo Finance .api (yfinance).

    - For BTC (Cryptocurrency known for volatility)

    - For VIT (Vanguard Information Technology Index Fund ETF -- Based on US IT company stock values)

Can:

A: Predict whether our chosen securities will be up/down after 14 days if presented with ~10 years of historical data for each. 

B: Use the relationships across VIT (yfTicker: 'VGT') and BTC (yfTicker: 'BTC-USD' - Cryptocurrency known for volatility) to better predict the direction of either in any way. 



The goal then is for our models to be able to predict the direction of either stock >50% of the time 14 days into the future. 
