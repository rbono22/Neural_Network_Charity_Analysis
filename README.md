# Neural_Network_Charity_Analysis

## Overview
Bek’s come a long way since her first day at that boot camp five years ago—and since earlier this week, when she started learning about neural networks! Now, she is finally ready to put her skills to work to help the foundation predict where to make investments.

With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to help Beks create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

### What You're Creating

This new assignment consists of three technical analysis deliverables and a written report. You will submit the following:

* Deliverable 1: Preprocessing Data for a Neural Network Model
* Deliverable 2: Compile, Train, and Evaluate the Model
* Deliverable 3: Optimize the Model
* Deliverable 4: A Written Report on the Neural Network Model (README.md)

## Results

### Deliverable 1: Data Preprocessing
#### What variable(s) are considered the target(s) for your model?
The target variable or dependent variable is the IS_SUCCESSFUL column. Our dataset contains past data of the companies AlphabetSoup have funded and this column shows weather or not the company was successful in the past. Thus we must seperate this column from the dataframe and assign it to our dependent variable, 'y'.

#### What variable(s) are considered to be the features for your model?
The feature variables or independent variables are our input values. They will influence our target value in the machine learning model. Our feature variables will be every other column of data in our new dataframe besides the IS_SUCCESSFUL column.

#### What variable(s) are neither targets nor features, and should be removed from the input data?
The columns EIN and NAME are neither targets or features. EIN is the identification number for each organization, and NAME is the name of each organization. These variables are unique to their index and will have no effect on the analysis.

### Deliverable 2: Compiling, Training, and Evaluating the Model
#### How many neurons, layers, and activation functions did you select for your neural network model, and why?
The neural network's input variable is set to equal the number of variables (#) in our dataframe. We have incoorperated two hidden layers due to the size of our data. The additional hidden layer will allow the model to evaluate interactions and identify complex relationships between weighted variables. The first hidden layer has 80 neurons and the second hidden layer has 30 neurons. The activation functions for each hidden layer will be the Rectified Linear Unit (RELU) function beacause it will simplify data in a range from 0 to 1, as we are looking for a binary outcome.

#### Were you able to achieve the target model performance?
No, we were not able to achive the target model performance of 75%. The accuracy of our model is about 72% at most, with a loss of 56%.

### Deliverable 3: Optimize the Model
#### What steps did you take to try and increase model performance?
In an attempt to improve the model performance, I removed the 'STATUS' column to remove extra noise from the dataset, and added a third hidden layer to to improve our model so that it accounts for more information. Within the hidden layers, I changed the activation functions for each layer - the first two layers using relu and the last layer using sigmoid. Lastly, I increased the number of epochs from 100 to 200 to allow the neural network model more rounds to analyze the data. This can allow for increased optimization of training data as the model has more rounds to analyze the data. Unfortunetally these methods fails to improve the model with the loss at 56% and the accuarcy at 73%.

## Summary
The results of the model performance suggest our current model is not fit to predict whether or not organizations will be successful in once receiving funds from Alphabet Soup. The loss of the model is 56% which is extremely high. The accuarcy of the model did not reach the target model performance of 75%. The issue may lay in the size of our dataset; maybe adding more data would allow our model to perform better.

If we were to veer away from a deep learning model, I'd recommend using a Support Vector Machine (SVM) as the model. The SVM model is more fitting to use when analyzing binary classifiaction because it will focus on the overall scope while avoid overfitting the data. SVM uses data points from two separate groups to build models that will predict outcomes for linear and nonlinear data. In binary classification problems, SVMs can be more reliable than deep learning models.
