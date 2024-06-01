# 2023-1-PSAT-team-timeseries
Topic Analysis by the P-SAT Time Series Data Analysis Team in the Statistical Analysis Society for the 1st Semester of 2023

## 💻 Project Introduction
<Stock Buy/Sell Recommendation Service for Risk Management for Beginner Investors>📈

For 'beginner investors'😢 who find it difficult to understand stock-related information and trends, our model recommends buying/holding/selling by learning from data that can affect stock prices, providing easy and simple insights into investment!😊

Data Used: Stock price trends, trading performance by investor type, foreign ownership, short selling volume, domestic news articles, English news articles, Naver Stock Forum posts, Naver search volume, KOSPI, Bitcoin trading, Economic Sentiment Index, News Sentiment Index, Industrial Production Index, Consumer Price Index, Consumer Confidence Index, Consumer Sentiment Index, Unemployment Rate, Bank of Korea base rate, exchange rate

Data Sources: Korea Exchange, Bank of Korea Economic Statistics System, KOSIS, invest.com, Naver Stock, Naver Data Lab, Big Kinds, CNN

Development Period: April 16, 2023 ~ May 19, 2023

## ❤️ Team Members and Roles

- Kim Min (Team Leader): Data collection, data preprocessing, Y~X EDA, variable selection (KS test), XGB, LSTM-CNN, LGBM
- Kim Dong-hwan: Rate of change labeling, data preprocessing, Y~X EDA, variable selection (causality test), VAR, LGBM, SVM, log reg
- Seo Yoo-jin: Data collection (+crawling), data preprocessing, X variable EDA, LSTM regression (threshold automation)
- Lee Soo-rin: X variable EDA, variable selection (PCA, factor analysis, VIF, importance), XGB, Naive Bayes
- Jang Da-yeon: Data preprocessing, sentiment analysis of Korean/English articles, random forest, XGB, LGBM

## 🔍 Analysis Workflow

1. Data Collection
2. Data Preprocessing (Sentiment analysis of news articles, data merging, interpolation of missing values, standardization of data types to numerical, chronological sorting)
3. EDA (Exploratory Data Analysis) (EDA between X variables, EDA between Y~X variables)
4. Labeling Rate of Change (continuous) -> Buy/Hold/Sell (categorical)
5. Feature Selection (causality test, VIF, PCA, factor analysis, feature importance, KS test attempts)
6. Predictive Modeling of Labeled Y Variables (with imbalanced class problem😭)
7. Visualization and Analysis of Prediction Results

## 📈 Modeling Overview
![image](https://github.com/dongdo1999/ModelingStockBuySellPrediction/assets/47492780/29166469-140b-40f2-89ca-95737de88084)

## 🚨 Class Imbalance Problem
There is a significant class imbalance due to the higher number of predicted labels compared to buy/sell -> Poor prediction performance for buy/sell

## 💡 Efforts to Resolve:

- Selection of models suitable for the project's purpose through custom evaluation metrics rather than simple accuracy or f1-score (e.g., average of accuracy and precision for buy and sell / average accuracy for buy, sell, and hold, etc.)
- Reflecting sample weights for each class during model training
- Regression prediction of labels -> Determination of classification threshold with validation set -> Final classification
 
## 📃 Results
![image](https://github.com/dongdo1999/ModelingStockBuySellPrediction/assets/47492780/ebe7dddf-c617-4343-9e42-0238cd15ef28)
![image](https://github.com/dongdo1999/ModelingStockBuySellPrediction/assets/47492780/4d89a3e5-1140-4bef-b31c-a73482265fda)








