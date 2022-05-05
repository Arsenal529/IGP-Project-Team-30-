# IGP-Project-Team-30-
This is a repository for our Interdisciplinary Group Project

Random Forest Classifier
Random Forest Classifier is  a supervised machine learning technique that is used to solve classification and regression problems. (Liu, Wang and Zhang, 2012)  According to Liu et.al, accuracy of random forest is good, it is easier to execute and faster. (Liu, Wang and Zhang, 2012) This was the main reason of chosing random forest classifier. Random Forest Classifier is an ensemble of decision trees that has low bias and moderate variance as it averages the variance.  This machine learning technique takes bagged decision trees to incorporate the various features of importance of a classification to help with predicting the best fit model to classify. 

(Kho, 2018), explains Random Forest Classifier as a good model for classification and regression tasks as it takes into consideration binary, categorical and numerical features. Also, there is little preprocessing of data that needs to be done. 

This classifier is recommnded for big data for its low processing time and higher accuracy. It is also good at handeling outliers in data. (Kho, 2018)

Execution
We adopted a Random forest Classifier model by using features of importance of our dataset(mobility speed average,mobility speed maximum, distance, trip length) to predict the target variable "Fuel Type".  f

The dataset was split into train and test data using the train_test_split from Sk.learn. (Pedregosa et al., 2011)

The classifier was sent to to a gridsearchcv (Pedregosa et al., 2011) to find the best fit parameters for the training of the model. 

The gridsearch CV algorithm found the best fit forest for accuracy to have two layers of decision tree (max_depth = 2), minimum nodes to be 2, number of trees before taking the average to be 10 with the random seed state set as 50. These parameters can be tuned for better accuracy. However, since MLP Classifier permformed more accurately, time was not set for fine tuning these parameters.

Evaluation of the Model
The models found that the most important feature in evaluation to be average speed of the vehicle followed by the trip distance. This insight can be used to find the cluster in k-means Clustering.

This model performed well with an accuracy scoring of 75% on the test data. Followed by this, the model was used to precidt the trips made exclusively by ICE vehicles and create a dataset with the predictions. Upon analysing the predictions, it was found that 16% of ICE trips were wrongly predicted as EV and these vehicles can switch based on their driving behaviours.








