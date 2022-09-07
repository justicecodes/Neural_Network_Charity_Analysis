# Neural_Network_Charity_Analysis

## Overview: 
The purpose of this project is to utilize machine learning and deep-learning neural networks with the Python TensorFlow library to create a binary classifier capable of predicting whether applicants from charitable organizations will be successful if funded by Alphabet Soup. 
The following steps are used to analyze the data:
  * Preprocessing the data 
  * Compile, train and evaluate the model
  * Optimize the model

## Results: 
#### Data Preprocessing
* The columns EIN and NAME are categorical information and were removed from the input data
* The target is the column IS_SUCCESSFUL, which refers to whether the charity donation was used effectively
* The features are columns APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT which have been counted, had bins created (other), and standardized


#### Compiling, Training, and Evaluating the Model
* The first model (AlphabetSoupCharity.ipynb) used 80 and 40 neurons, 2 layers, and used the ReLU activation function
<img width="624" alt="first_model" src="https://user-images.githubusercontent.com/103595718/189001575-f3e016c1-a784-421e-a9a0-331f183feff0.png">
The loss was high, 1.58, and accuracy was low, .657

How many neurons, layers, and activation functions did you select for your neural network model, and why?
* Were you able to achieve the target model performance?
* What steps did you take to try and increase model performance?


#### Summary: 
Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and explain your recommendation.
* The deep learning neural network model did not reach the target of 75% accuracy. Considering that this target level is pretty average we could say that the model is not outperforming.
* Since we are in a binary classification situation, we could use a supervised machine learning model such as the Random Forest Classifier to combine a multitude of decision trees to generate a classified output and evaluate its performance against our deep learning model.
