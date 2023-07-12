# LSTM_testing






Python environment Set-up:
The course work is Jupyter Notebook as it is an open source web application that you can use to create and share documents that contain live code, equations, visualizations, and text. In this section the necessary libraries and dataset has been loaded.
 
 Data Loaded and described:
   
					





Task A
a) Data Visualisation:
	Below graph is crafted to demonstrate that the Stock Price is derived for the 20 years as per the data set which is tailed until 2019 September. The visualization helps us understand that the oil price was high from 2011 and attained a peak on 2013. But currently the price drop can be seen on 2019.
stock price change Brent oil price information for the last 20 Years.       
B) Explanatory Variables:
	The normally used technical analysis strategy the moving average(MA)  has been used to define this problem with a steady update in mean value of the stock price.                                                                        Price Prediction with Moving average of 9 
  Price Prediction with an moving average of 3
		
c) Defining the Train and Test Data:
	Forecasting the stock price with the data demands a train and test data due to the nature of the regression model being built. The model is built with an function that creates the label column and expanding the dataset by a given number of rows having value NaN(not a number). Creating the feature array by function creation by returning the list of lists : list comprising of training i/p, test set, training o/p, test o/p, final 10 days that we need to predict as forecasting values.
D) Build a Linear Regression Model (LR):
	Learning happens here when the model is trained (training input and output variables), function in the LR equation is given by learner.fit(x_train,y_train).
Prediction: We'll predict for a given set of dates including the data until and available and we forecast for dates which are in Future i.e, with the MA3 and MA9 inputs that we have already developed. 
 
e) Prediction function result:
	Thus flowing down from all the above process the prediction function result is scored to 0.733 which is calculated to be 73% average. A 73% is RMSE (lesser the RSME, closer to 0, better the results) Practically we'll not be able to predict exactly similar value Any number can have infinite decimal values.
 

f) Alpha and betas value:
	Here the alpha and beta value is calculatied on the Linear equation y = b0 + b1*x and it retrieves the Intercept coefficient of alpha which is 1.25 as well as the with alpha, the coefficient of Linear equation i.e, Beta is derived to be a value approximately 10.
 
Conclusion with Linear Regression:
yhat = learner.intercept + learner.coef_ * X¶
Interpretation 1
Sign of slope is +ve, with increase in values of X, y_hat will increase
Sign of slope is -ve, with increase in yesterday's, today's value is likely to decrease
Interpretation 2
With increase in 1 unit or 1$ in price, the chances of increase in today's value is an increase by 10.00
Task B
Predicting the Brent oil price Stock with LSTM Neural Networks  
A)	Train and Test Brent oil price time series data set.
             Importing Libraries and preparing the libraries for a LSTM is adverse than that of the Linear Regression method. The TensorFlow accepts only Float values and the datetime frame to float conversion must be carried away with lambda function to avoid any adverse effect of value errors. 
      
Libraries for LSTM Model
 
			Dtype formation for LSTM Model
	Splitting the values into testing and train by usual data frame model has been carried out with the minmax scaler normalization of the data, to make sure the fit is perfect for an Lstm model. The data then is converted from array to matrix dataset as the data set is ready for an reshape to fit the model for the algorithm.  
 
B) Building the Model:
	Once the test and train model is ready the data is then set into the Lstm network regressor. Long Short-Term Memory (LSTM) neural network belongs to Recurrent Neural Network (RNN), which is specialized in training time-series/sequential data. LSTM neural networks is structured in a similar way as RNN in a chain structure as the model is sequentially uploaded with the value count set to 60 with dropout rate of 0.1. For this model the iteration is set to 20 as the epoch and the model is set to validate the trained data.	 				LSTM Network Regressor

C)	Prediction Function and Result:  							Post a complete modelling the following results are assessed:
Train Mean Absolute Error: 0.018686968774323624
Train Root Mean Squared Error: 0.02266653380226051
Test Mean Absolute Error: 0.026566493377236357
Test Root Mean Squared Error: 0.03437048585788954
	
 

 


Conclusion: 
		Thus, the prediction for using an LSTM model gives out an 0.01 of Mean absolute error and an RMSE of 0.02 which is very well considered for an model success. This the LSTM model of development serves as very well than that of the Linear Regression model for this data set with exceptional data. 
