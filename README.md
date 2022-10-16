# Predicting long short of stocks by indicators resonance
- Author: Li-Chun Huang
- Institute: Department of Computer Science at National Yang Ming Chiao Tung University
- Email: libao3128.cs08@nycu.edu.tw

## Introduction
This project using the multiple technical indicators in stock market to predict the tomorrow stock price. We also compare the performance of different machine learning algorithm, hyper-parameters setting and target. You can see the result in Report.html.

## Environment
The project is built with Python 3.10.4 on Visual Studio Code on Windows 10. You can directly download the project and run it on Visual Studio Code or you can download the code and including following dependencies on your own environment.

## Dependency
1. Basics
    - pandas==1.4.2
    - numpy==1.22.3
    - matplotlib==3.5.1
2. Stock Price Related
    - stockstats==0.4.1
    - yfinance==0.1.72
    - TA-Lib @ TA_Lib-0.4.24-cp310-cp310-win_amd64.whl
3. Machine Learning Related
    - sklearn==0.0

## Dataset
The dataset is provided by **yahoo finance** API **yfinance**. In the provided code, AAPL's stock price from 2012 to 2021 is used as an example. The dataset contain 5536 rows and 6 columns. The columns' information is shown below:
![](https://i.imgur.com/jrFpo0p.png =500x)

The chart of the close prices is shown below. 
![](https://i.imgur.com/8wSsARa.png =300x)

You can change it depending on your requirement.

## Objective
Our goal is to predict whether the next day's price will be higher than today's price. Therefore, the label of the dataset will be $Close_{t+1}-Close_{t}>0$, where $t$ is the date. After computing the trend of prices, the label distribution looks like:
| True | False |
| ---- | ----- |
| 2868 | 2634  |

,which means that along 5536 days, there are 2868 days' prices growing higher than yesterday and 2634 descending on the other hand.


## Methodology
As mentioned above, our dataset is the record of the stock price with the time series. It is very hard for us to predict tomorrow's trend directly by today's price. Therefore, I use the indicators which are commonly used in the field of technical analysis. You can see table 1 in appendix for more information.

## Result
For this experiment, I found out that with a few technical indicators, we can really predict the trend of tomorrow's price. In addition to this, I also find out that the more data doesn't mean the better performance. As you can see above, the best amount of data is around 5 years, neither more or less data is good for the prediction.
Besides the performance metrics I have done above, I also try to simulate the strategy based on model prediction.
![](https://i.imgur.com/7sTaiH8.png)

As you can see above is the return on investment based on random forest prediction given 2015~2020 train data. The strategy simply all in if the model predict that tomorrow will go up and do nothing if go down. As the result, the strategy can beat the long-term holding strategy.
