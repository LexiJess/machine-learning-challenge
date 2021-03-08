This project explores a dataset that represents celestial bodies that may or may not be appropriately classified
as exoplanets. The three categories are Confirmed, False Positive, and Candidate. The models train and then test
the dataset and make their predictions about which celestial body most likely belongs to each category. 

Model_1 uses MinMaxScaler to scale the data, then uses the model LogisticRegression. Tuning is done with
GridSearchCV.  Even with tuning and fitting, the model, the accuracy returns at just 61%. 

Model_2 uses the same style of data cleaning and processing, but switches to a neural network model with
TensorFlow and keras. The model includes multiple layers and is optimized with keras' Adam optimizer. The model
is fitted and trained and yields an accuracy of 87%, which is much better than Model_1. 

Model_2 is then used to predict the category of celestial bodies (the "new_data" variable that is fed into
the model is the prediction data). Because we needed to transform the categories (False Positive, Candidate, or
Confirmed) into integers in order to make them work in the model, we need to identify which integers correspond
to which categories. This is done using df.value_counts() and comparing the ranked order of each category
to the frequency of 0's, 1's, and 2's. 

# 2's are False Positives
# 1's are Confirmed
# 0's are Candidates


    

