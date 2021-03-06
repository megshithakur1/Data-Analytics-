# Data-Analytics

## 1. Introduction
My application is inspired by the rising crime throughout the USA. A question to ask: Is there a proper pattern every time a crime happens? If the answer is yes, it means there is a repeating pattern which can be present and there could be a way to prevent the next crime before it happens. In 2016, the violent crime rose in United States for the second consecutive year. Over previous years, this year the rate is increased by 4.1%. In Chicago, itself the reported murders last year was 765 in total, which is nationwide 22% increase.  Making this world a better place to live is the agenda of most of the communities. But I really want to step into the process and take a measure to help. The better understanding of the crime can be gained by identifying patterns that are responsible for that particular crime 
The aim of this project is to do model the time series data by applying various techniques in order to get the best fit model for the future predictions. We will be predicting the number of street crimes in Chicago for October and November 2016<br />

## 2.	Data Sets
I got the data from Kaggle: https://www.kaggle.com/umeshnarayanappa/forecasting-chicago-	crimes-2017-2020/data
We will be working on the following attributes of the data set: longitude, latitude, time, date, and type of crime. The dataset consists of 6 million records approx., starting year is 2001. We will clean the data and eliminate outliers from the above fields of the dataset. Once the data is processed, we will be able to create time-series over count of crime and other variables too. <br />

## 3.	Problems to be solved
In this project, I will try to interpret the number of street crimes that happens over the past years. The problems that we will try to solve are:<br />
•	What percentage of crime is committed on the streets of Chicago?<br />
•	Can the future prediction of the same will help in reducing the crime?<br />
•	How accurate can the forecasting be done? <br />

## 4.	Methods and Processes

In this project, our main is to apply different techniques to model the time series data for ‘Number of street crimes in Chicago’ in order to evaluated their fit and choosing the best model which can forecast values for October and November 2016. <br />
Below is the given data: 
![My picture](https://github.com/megshithakur1/Crime-In-Chicago/blob/master/Graphs/1.png)

### Model 1: Using moving average decomposition model
Starting with the moving average decomposition model which is also smoothing model. This model has two types: additive and multiplicative. We will apply both the models and then compare their results. The models applied are indicated with red line on the plotted data: <br />

Decomposition moving average- Additive
![My picture](https://github.com/megshithakur1/Crime-In-Chicago/blob/master/Graphs/2.png)

Decomposition moving average- Multiplicative
![My picture](https://github.com/megshithakur1/Crime-In-Chicago/blob/master/Graphs/3.png)

From the above plots, we cannot infer which models fits the best. That’s why we will use the mean root square error(RMSE) to find out the best fit model. <br />
1.	Finding the best model from the above two.<br />
By comparing the RMSE of both the models, we can conclude which model fits the data best. Below is the RMSE value for both the models:<br />

RMSE additive	<br />
12.91045<br />

RMSE multiplicative	<br />
0.9826991<br />

As we know that the model with lower RMSE is better fit for the data. In this case the multiplicative model has lower RMSE value it means it fits the data better than the additive model. <br />

The other reason is that in our time series the season effect increases as the trend increases which can be seen in the above plotted graph.  <br />
2.	Fit trend line to smoothed deseasonalized series in order to get forecasting. <br />
Linear Regression- Decomposition Trend<br />
![My picture](https://github.com/megshithakur1/Crime-In-Chicago/blob/master/Graphs/5.png)<br />

3.Obtaining forecast for Oct and Nov 2016 using the multiplicative model.<br />
From the above liner model, we have got the forecast values for Oct and Nov 2016. <br />

Oct 2016	<br />
134.1644<br />

Nov 2016	<br />
136.2500<br />








