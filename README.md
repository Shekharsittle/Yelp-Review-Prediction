# Yelp-Review-Prediction
## Problem Statement
Use a Yelp Review dataset to build and deploy a machine learning model
that predicts review ratings based on review text.
## Dataset
https://www.kaggle.com/datasets/omkarsabnis/yelp-reviews-dataset/download?datasetVersionNumber=1
## Exploratory Data Analysis
* Dataset consist of 10000 rows and 10 columns, there are no null value in dataset.
![image](https://github.com/Shekharsittle/Yelp-Review-Prediction/assets/127113185/f7c3ec51-dcac-4934-8d7a-f65c6fecb34d)
* There are more text with 4 star ratings and 1 star rated text are least.
![image](https://github.com/Shekharsittle/Yelp-Review-Prediction/assets/127113185/99a2632a-2bd7-4fba-a12e-1b864e28f2a3)
* If you observe in the above graph , you can infer that 1,2 and 3 star rating are showing same trend , also 4 and 5 are having similar pattern.
![image](https://github.com/Shekharsittle/Yelp-Review-Prediction/assets/127113185/2e7d717c-8b06-4e81-a4bd-36ec06376b0e)
From the given boxplot we can see that all median of text length for ratings are similar , so there is very less dependency of rating on length of text. By calculating correralatipn we found that rating is minutely negatively correlated with text length.
![image](https://github.com/Shekharsittle/Yelp-Review-Prediction/assets/127113185/248a14af-58ff-4027-aeed-bf91cdff29ea)
## Data Cleaning and Preprocessing
Renmoval of stop words are done and defined a fnction to remove punctuation and special characters from the text , lemmatized the word for preparing it for model development.
![image](https://github.com/Shekharsittle/Yelp-Review-Prediction/assets/127113185/81f6f974-ccbe-4258-8ac7-0ff9e89a73c9)
## Model development and evaluation
First built a regressor models ,but the r square value are very low so decided to go with classifier . Built a Naive Bayes , Logistic and XGBoost classifier model .

When we used all rating i.e, 1,2,3,4,5 as target then our models doesnot performed well so in order to boost our model , decided to use two unique value for classification i.e grouped  1,2 and 3 rating as bad and 4,5 as good. 

When we built a same model on it , we could see the steep increase in the accuracy of the model.
![image](https://github.com/Shekharsittle/Yelp-Review-Prediction/assets/127113185/9f434126-f6c5-4f95-823c-f627143a9325)



 
