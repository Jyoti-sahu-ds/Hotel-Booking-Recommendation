# Hotel-Booking-Recommendation

## Business Problem
This case study investigates a dataset that includes details on hotel reservations and related attributes. In this study, we will examine the features that are available to hotel owners and how they may use them to estimate the outcome of a booking. If hotel owners used the knowledge gained from this research, they might be able to better organize their businesses and comprehend how they can make money in these challenging times. Based on the characteristics of each hotel reservation, my algorithm will determine whether or not a booking will be canceled. Based on the remaining features in the dataset, my goal is to identify the optimal model to use tree-based algorithms to forecast cancellations of hotel reservations.

## Objective
• What does the analysis/model building tell you?
• What are your recommendations?
• How would you pitch this business problem to a group of stakeholders to gain buy-in to proceed?
• Why should someone in the business care about this solution?
• What are some of the potential challenges or additional opportunities that need to be explored?

## Scope
The scope of the project is based on dataset contains 31 features about booking information such as Average Daily Rate, Arrival Time, Room Type, Special Request, etc. between 2015 and 2017 years. 
Below is the scope of the effort:
•	Data Selection
•	Identify relevant attributes
•	Data Preparation
•	Feature Selection/Feature Engineering
•	Exploratory Data Analysis
•	Data Visualization
•	Model Selection
•	Model Evaluation
•	Expected Results / Outcome

## Approach
 EDA-
 Topics covered and questions to answer from the data:
•	Where do the guests come from?
•	How much do guests pay for a room per night?
•	How does the price per night vary over the year?
•	Which is the busiest month?
•	How long do people stay at the hotels?
•	Bookings by market segment
•	How many bookings were canceled?
•	Which month have the highest number of cancelations?

## Feature Enginnering
There is no obvious difference between children and babies these features gathered under the one feature which name is all_children.Another part is analyzing categorical features. Categorical labels converted into numerical form. This will help to be more understandable and implementable into machine learning algorithms. Some features are not ordinal such as country. In that case, One-Hot Encoding could be chosen. Due to the high number of categories, this method could incur higher computational cost. To help reducing that, Label Encoding method will be used.

We are going to create two data frames here. One data frame has solely category information, whereas the other contains numerical information. A correlation matrix will be created using these two separate data sets. 
For categorical data correlation matrices, the Spearman approach will be utilized, and for numerical data correlation matrices, the Pearson method will be used.
We are going to employ three different methods here to select features.
•	Spearman Method
•	Pearson coefficient
•	Probability Density function 

### Correlation Matrix with Spearman method

![image](https://user-images.githubusercontent.com/70611285/177247366-1209262e-de20-482f-ab08-e00b10583cb9.png)

### Correlation Matrix with Pearson Coefficient method

![image](https://user-images.githubusercontent.com/70611285/177247446-075682f9-e85f-4987-a856-63e5c8803e46.png)

## Model Creation

Before model building, data will be split to train and test respectively 70% and 30% ratio. X_train and X_test data will be standardized with the Standard Scaler technique. After that, the Stratified K-Fold Cross Validation method will be used for resampling. Cross-validation is an important implementation to avoid overfitting. Stratified K-Fold Cross Validation method provides train/test indices to split data into train/test sets. Model parameters have been defined in the previous part.

![image](https://user-images.githubusercontent.com/70611285/177247550-524c0af9-29d8-4415-b291-3b1a77569e10.png)

### Confusion Matrix
![image](https://user-images.githubusercontent.com/70611285/177247576-6e5abdc6-8efb-4c3c-abe9-24fe39c3ba5f.png)

## Model Evaluation
![image](https://user-images.githubusercontent.com/70611285/177247596-4f8ad41e-bb1e-4f46-a274-367859e602c4.png)
![image](https://user-images.githubusercontent.com/70611285/177247599-92a219ff-431a-4add-b220-bee65e7b4d6f.png)

## Conclusion/Recommendation

From the above scores, Random Forest Classifier is the best algorithm for this dataset and I would like to test my model by above methods because of higher accuracy than other models and Hotel should rely on random forest model to predict the hotel cancellation.

From our EDA, we have observed that the top 5 most important features in the data set which helps in predicting Cancellations from the guests are:
1.	Lead Time
2.	adr
3.	Deposit Type
4.	Arrival Day of the Month















