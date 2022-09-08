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
* The target of training the model in each iteration is an accuracy rate of 75%
1. The first model (AlphabetSoupCharity.ipynb) used 80 and 40 neurons, 2 layers, and used the ReLU activation function
<img width="624" alt="first_model" src="https://user-images.githubusercontent.com/103595718/189001575-f3e016c1-a784-421e-a9a0-331f183feff0.png">

  * Total params = 6,721; the loss was high, 1.58, and accuracy was low, .657


##### Optimization attempts: 
* To increase the performance of the model, bucketing was applied to the features INCOME_AMT and CLASSIFICATION, adding an "Other" category to group values with small occurences
* Additional models were tested to improve accuracy:
2. Neurons were added to the hidden layer, increasing each layer to 100 and 50 respectively
    * Params increased to 9,301; loss: 0.5638 - accuracy: 0.7300
3. Hidden layers were added, increasing the number of layers from 2 to 4
    * Params increased to 10,796; loss: 0.5659 - accuracy: 0.7298 
4. Changed the activation function from Sigmoid to ReLu and decreased Epochs from 100 to 80
    * Params still 9,301; loss: 0.6102 - accuracy: 0.7238 


#### Summary: 
* The deep learning neural network model did not reach the target of 75% accuracy despite different trials
* The most effective model occured when the neurons were increased (test 2) as the loss was lowest and accuracy highest compared to other tests
* Alternatively, we could use a supervised machine learning model such as the Random Forest Classifier to combine a multitude of decision trees to generate a classified output and evaluate its performance against our deep learning model.
