# Neural_Network_Charity_Analysis

## Overview of the Analysis
The purpose of this analysis was to take a provided dataset to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup. This analysis required analyzing more than 34,000 organizations that have received funding from Alphabet Soup.

## Analysis

### Data Preprocessing
- The target for the model is the IS_SUCCESSFUL column
- The features for this model are: NAME, APPLICATION, TYPE, AFFILIATION, CLASSIFICATION, USE-CASE, ORGANIZATION, INCOME_AMT, and ASK-AMT
- Variables removed from the input data included EIN and NAME in the initial analysis, and SPECIAL_CONSIDERATIONS and STATUS when optimizing

### Compiling, Training, and Evaluating the Model
- The initial version of this model used 2 hidden layers (with 80 neurons and then 30 neurons) with a Sigmoid activation function in the output layer as can be seen below:
-
![Initial Model](https://github.com/baileyvo/Neural_Network_Charity_Analysis/blob/main/Initial_Model.PNG)

- The attempt at optimization used 3 hidden layers (with 80 neurons, 40 neurons, then 20 neurons), with a Linear activation function in the ouput layer as can be seen below:

![Optimized Model](https://github.com/baileyvo/Neural_Network_Charity_Analysis/blob/main/Optimized_Model.PNG)

- The initial model achieved an accuracy of 0.7278134226799011, which did not meet the target of 75%. 
- To try and increase model performance, a number of steps were taken: two more variables were dropped (SPECIAL_CONSIDERATIONS and STATUS), an additional hidden layer was added and the numbers of neurons in hidden layers were tweaked, and the number of epochs were increased from 50 to 100. Unfortunately these updates did not increase the accuracy, reaching only a small increase to 0.7282798886299133.

## Summary
Overall, the target accuracy could not be reached. One possible way to improve accuracy would be to use the Tanh activation function, to take into account negative values in the scaled dataset. 
