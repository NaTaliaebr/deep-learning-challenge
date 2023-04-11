# deep-learning-challenge

Overview:

Using machine learning and neural networks and the features in the dataset provided we will build a binary classifier that can predict if applicants will be successful if they are fuded by Alphabet soup.


##  Final Results: 
Loss: 0.6487845182418823, Accuracy: 0.7309614419937134


## Data Preprocessing Work Flow: 

* The IS_Successful variable is the target variable,while the remaining variables are the features
* To decrease the number of unique values in APPLICATION_TYPE and CLASSIFICATION features, we created another category for both of them.
* Numeric features were normalized using the Standard Scaler in both the training and test datasets.



## 
* Compiling: chose Adam as an optimizer, learning_rate as 1e-3, and  metrics as accuracy.
* Training: Created a callback that saves the model's weights every five epochs, trained the model at 100 epochs.
* Model Optimization: Three different approach were used to optimize the model performance.
  * Removed the outliers from ASK_AMT feature
  * Removed the STATUS feature as there was high imbalance in this feature ( 1=33608, 0=5)
  * Added one more hidden layer
* Evaluating the Model: for the training dataset, loss: 0.5139 - accuracy: 0.7506. Versus, for the testing dataset,Loss: 0.6487845182418823, Accuracy: 0.7309614419937134. The result is sligthly better on training dataset.


## Summary: 
Since this model has an accuracy of 0.73, I would not recommend moving it to production. Due to the fact that there are 83 features in the model and the dataset is structured, I recommend decision tree based models, especially Randon Forest models, to better predict the outcome.


