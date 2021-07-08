# Neural_Network_Charity_Analysis

# Background
Beck is a data scientist and programer for Alphabet Soup which is a charitable organization dedicated to support initiatives related to the environment, people's health and unified world.  Alphabet Soup has raised and donated over 10 billion dollars in the past 10 years.  Beck is incharge of the data to determine if the foundation's money is being utalized effectively by the organizations that the donations have been made to. Unfortunately, not every donation made is impactful even so that in some cases the organizations will take the money and disappear.

## Purpose
The purpose of this analysis is to predict which organizations are worth making a donation to and which are too high risk by using a mathematical data driven solution and utalizing a deep learning neural network. This model will evaluate the input data and produce a clear decision making result using the tensor flow library. This would help Alphabet Soup to determine which organizations should recieve their donations.

# Results

## Data Preprocessing

[unique_value]() shows the different variables in the list after EIN and Name were dropped

- The IS_SUCCESSFUL variable are considered the targets for the model as it shows which organizations have used the money effectively


- The following variable(s) are considered to be the feature for the model:
APPLICATION_TYPE
AFFILIATION
CLASSIFICATION
USE_CASE
ORGANIZATION
STATUS
INCOME_AMT
SPECIAL_CONSIDERATION
ASK_AMT


The EIN and NAME were considered to be neither the feature nor the target for the model and were therefore deleted.

## Compiling, Training, and Evaluating the Model

- Two layers were chosen and along with the output layer were chosen for the original model.  There were 80 neurons in the first layer and 30 in the second.  The activation for layer 1 and layer 2 were relu and for the output layer was sigmoid.  [Original_model](https://github.com/Nidaiq/Neural_Network_Charity_Analysis/blob/c1b5c101c192b0ec253b21c35da0b7359ad32d28/Resources/Original_Model.png) shows that the accuracy rate for the original model was 73.42%

- The result of 75% accuracy was not acheived after the 3 attempts

-The following steps were taken to attempt to increase the model performance
[Attempt#1](https://github.com/Nidaiq/Neural_Network_Charity_Analysis/blob/c1b5c101c192b0ec253b21c35da0b7359ad32d28/Resources/Attempt%231.png) increased number of neurons in a layer and an accuracy of 73.44% was acheived

[Attempt#2](https://github.com/Nidaiq/Neural_Network_Charity_Analysis/blob/c1b5c101c192b0ec253b21c35da0b7359ad32d28/Resources/Attempt%232.png) increase the neural layers and an accuracy of 73.34% was acheived

[Attempt#3](https://github.com/Nidaiq/Neural_Network_Charity_Analysis/blob/c1b5c101c192b0ec253b21c35da0b7359ad32d28/Resources/Attempt%233.png) change number of neurons in layers and change the type of activation and an accuracy of 73.41% was acheived

# Recommendations

After making multiple attempts the model could not be optimized and the requirement of 75% accuracy could not be acheived.  It is suggested the Random Forest Classifier be used as it may be a faster model and could avoid the overfitting which might be occuring in the neural_network model.
