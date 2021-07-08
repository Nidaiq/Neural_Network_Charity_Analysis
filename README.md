# Neural_Network_Charity_Analysis

# Background

Beck is a data scientist and programmer for Alphabet Soup which is a charitable organization dedicated to support initiatives related to the environment, people's health and unified world.  Alphabet Soup has raised and donated over 10 billion dollars in the past 10 years.  Beck is in charge of the data to determine if the foundation's money is being utilized effectively by the organizations that the donations have been made to. Unfortunately, not every donation made is impactful even so that in some cases the organizations will take the money and disappear.

## Purpose

The purpose of this analysis is to predict which organizations are worth donating to and which are too high risk by using a mathematical data driven solution and utilizing a deep learning neural network. This model will evaluate the input data and produce a clear decision-making result using the tensor flow library. This would help Alphabet Soup to determine which organizations should receive their donations.

# Results

## Data Preprocessing

[unique_value](https://github.com/Nidaiq/Neural_Network_Charity_Analysis/blob/4a60a5746ce475d630a74148348d6303d2d15816/Resources/unique_value.png) shows the different variables in the list after EIN and Name were dropped.

- The *IS_SUCCESSFUL* variable are considered the targets for the model as it shows which organizations have used the money effectively.

- The following variable(s) are considered to be the feature for the model:
*APPLICATION_TYPE*
*AFFILIATION*
*CLASSIFICATION*
*USE_CASE*
*ORGANIZATION*
*STATUS*
*INCOME_AMT*
*SPECIAL_CONSIDERATION*
*ASK_AMT*

- The *EIN* and *NAME* were considered to be neither the feature nor the target for the model and were therefore deleted.

## Compiling, Training, and Evaluating the Model

- Two layers were chosen and along with the output layer were chosen for the original model.  There were 80 neurons in the first layer and 30 in the second.  The activation for layer 1 and layer 2 were relu and for the output layer was sigmoid.  [Original_model](https://github.com/Nidaiq/Neural_Network_Charity_Analysis/blob/c1b5c101c192b0ec253b21c35da0b7359ad32d28/Resources/Original_Model.png) shows that the accuracy rate for the original model was 73.42%.

- The result of 75% accuracy was not achieved after the 3 attempts

- The following steps were taken to attempt to increase the model performance:

 		[Attempt#1](https://github.com/Nidaiq/Neural_Network_Charity_Analysis/blob/c1b5c101c192b0ec253b21c35da0b7359ad32d28/Resources/Attempt%231.png) increased number of neurons in a layer and an accuracy of 73.44% was achieved.

 		[Attempt#2](https://github.com/Nidaiq/Neural_Network_Charity_Analysis/blob/c1b5c101c192b0ec253b21c35da0b7359ad32d28/Resources/Attempt%232.png) increased the neural layers and an accuracy of 73.34% was achieved

 		[Attempt#3](https://github.com/Nidaiq/Neural_Network_Charity_Analysis/blob/c1b5c101c192b0ec253b21c35da0b7359ad32d28/Resources/Attempt%233.png) change number of neurons in layers and change the type of activation and an accuracy of 73.41% was achieved.

# Recommendations

After making multiple attempts the model could not be optimized and the requirement of 75% accuracy could not be achieved.  It is suggested the Random Forest Classifier be used as it may be a faster model and could avoid the overfitting which might be occurring in the neural network model.

According to towardsdatascience.com, "Random Forest is less computationally expensive and does not require a GPU to finish training. A random forest can give you a different interpretation of a decision tree but with better performance. Neural Networks will require much more data than an everyday person might have on hand to actually be effective. The neural network will simply decimate the interpretability of your features to the point where it becomes meaningless for the sake of performance."  This explination could be used for the recommendation for this analysis as well.


# Reference

3 Reasons to Use Random Forest Over a Neural Network–Comparing Machine Learning versus Deep Learning.  https://towardsdatascience.com/3-reasons-to-use-random-forest-over-a-neural-network-comparing-machine-learning-versus-deep-f9d65a154d89.  Accessed on July 7th, 2021.