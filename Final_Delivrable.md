# EDA Final Delivrable
Raed Altuwaijri
Email/Github: Altuwaijriraed@gmail.com

Fahad Alharbi
Email/Github: Fa7adBinA@gmail.com


## Abstract

The goal of this project was to use linear regression models to predict the total subscription for the top five YouTube channels in the Kingdom of Saudi Arabia in terms of the growth rate in the number of subscriptions for each channel to find out the most influential channel in a short period, through scraping more than one stats site YouTube to extract data set for each YouTube channel, and using Time Series Prophet to predict the number of subscribers in the next two years for each channel through the available data and to know the most growth channel in terms of the number of subscribers for each channel

## Design

* Company info:\
We are a sponsorship company to sponsor the most trending channels in Saudi Arabia.
The sponsership company is a company that sponsors YouTube celebrities to market the company's
products through YouTube channels.

* Value for the company (solve/ investigate problem), recommendations (money, service, decision support, cutting cost, health benefit):\
The value for the company is to predict the channel with greatest growth in subscribers to know the best
YouTube channel to sponsor.

## Data
Data obtained from [Social Blade](https://socialblade.com/youtube/) and [Web Archive](https://wayback.archive.org/).

## Field Description:

| Field Name        | Description                                                                     |
|-------------------|---------------------------------------------------------------------------------|
| Date              | Represents the date (MM-DD-YY)                                                  |
| Daily Subscribers | Channel Daily Gained Subscribers                                                |
| Total Subscribers | Channel Total Subscribers                                                       |
| Daily Video Views | Channel Daily Gained Video Views                                                |
| Total Video Views | Channel Total Video Views                                                       |

* Data size Five Years from 2016 to 2021 with five data sets

* the number of rows is 5700, and the number of columns is 5

## Algorithms

#### Data Scraping:-
* Python Requests and urllib library to send http requests and get response
* beautifulsoup to parse http response and get HTML DOM elements
* regex to extract data from HTML DOM elements
* JSON to parse string -data gained by regex- to list


#### Data Cleaning:-
* drop duplicate rows 
* drop zeros
* convert Timestap to Date
* convert columns from Object to Float
* Total Subscribers imputation
* validate Total Subscribers with Daily Subscribers

#### Regression Model:-
* Facebook Prophet library for time series forecasting
* The target variable is Total Subscribers
* R-Sequared score for training and cross validation


| Channel Name | Training R-Squared | Cross Validation R-Squared |
|---|---|---|
| mmoshaya | 0.99888 |  0.98599 |
| ARAB GAMES NETWORK | 0.99930 | 0.99222 |
| Anasala | 0.99972 | 0.97738 |
| BanderitaX | 0.99984 | 0.98070 |
| Rawan and Rayan | 0.99906 | 0.98390 |




## Tools:
* Technologies: Python, Jupyter notebook.
* Libraries: Numpy, Pandas, Matplotlib, Seaborn, Sklearn, Plotly, Prophet, Requests, BeautifulSoup, Regex, Urllib, json, Plotly dash.

## Communication
[](TOP5.png)

[](Dash.png)
