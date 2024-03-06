Data Science Project Proposal: Volatility Trading Strategy
Project participants: Christian Ingul, Anthony Navarro

Background Summary:
This project aims to leverage machine learning techniques to forecast the realized variance (RV) as a proxy for the implied volatility of options, particularly focusing on the SPY (S&P 500 ETF Trust). Accurately predicting RV will identify mispriced assets in the market, enabling the execution of profitable trading strategies.
Problem Statement: The challenge of identifying anomalies or mispricings in the listed options market has intensified. Traditional methods depend heavily on mathematical models. This project proposes a paradigm shift towards a data-driven approach, employing advanced ML models for more accurate volatility forecasting.
Technical Objective:

To develop, test, and deploy an automated trading strategy that utilizes advanced data science and machine learning techniques for forecasting volatility. This involves data extraction, preprocessing, exploratory data analysis (EDA), feature engineering, model development, backtesting, and deployment on a cloud platform for real-time trading.
Methodology:
Data Preparation and Exploration: Retrieve financial data, perform comprehensive EDA to identify patterns and correlations, and create a data dictionary for clarity.
Data Preprocessing and Feature Engineering: Apply data cleaning techniques, utilize dimensionality reduction methods like LASSO and PCA, and explore autoencoder structures for feature selection.
Model Development and Evaluation: Implement a sophisticated encoder-decoder architecture and other deep learning models, supplemented by shallow models for benchmarking. Conduct rigorous backtesting to evaluate model performance.
Deployment and Real-time Trading: Deploy the model and trading strategy on AWS using Amazon Sagemaker, with the potential for project sponsorship based on outcomes.
Timeline:
Week 1-2: Data extraction and initial EDA.
Week 3: Advanced preprocessing and feature engineering.
Week 4-5: Model development and backtesting.
Week 6: Cloud deployment and initial trading tests.
Expected Outcomes:
A fully functional automated trading system capable of predicting SPY option volatility with high accuracy, alongside practical experience in deploying and managing ML models for real-time applications.
Explanation of Target Variable: 22-day Forward Realized Variance (RV) with a 23-day Lead

Realized Variance (RV): This is a statistical measure of the variability of financial returns. Specifically, it is the sum of the squares of daily returns for a given period. Squaring daily returns emphasizes larger movements and provides a measure of volatility.

22-day Period: The timeframe of interest is 22 trading days, which approximates one calendar month of trading days. The RV is calculated over these consecutive 22 trading days to capture a monthly volatility profile.

23-day Lead: Instead of calculating this RV for the current or immediate past 22 days, we calculate it for a period starting 23 days ahead of the current date (the index date). This means that for any given day when the data is recorded, the RV we're targeting to predict is not for the past or present month but for the month that begins 23 days in the future.

Purpose of Leading: The 23-day lead time is essentially a forecasting step. It ensures that the RV we are trying to predict is not immediately influenced by the current day's price action, which provides a clearer predictive signal for future volatility that could impact trading decisions.

Application in Trading: In practical terms, a trader or a portfolio manager would use today's information to predict the level of volatility (using the RV) for a month that starts 23 days from today. This forward-looking forecast helps in planning trades and risk management strategies for that future period, rather than reacting to already known or current market conditions.


How RV Prediction Informs IV Analysis:
Predicting RV accurately provides an estimate of future market volatility. By comparing this with the current IV, we can identify potential mispricings in the options market. This insight is pivotal for developing trading strategies that capitalize on the spread between the predicted RV and the IV reflected in option prices, thereby securing potential profits.
