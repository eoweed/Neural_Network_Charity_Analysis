# Neural_Network_Charity_Analysis

### Overview:
The purpose of this project is to build a neural network model that will predict whether applicants will be successful if they receive investment funds from the AlphabetSoup foundation. 
Data from past applicants, who were funded by AlphabetSoup, is used with the keras sequential model to help predict whether future applicants will be successful or not. The initial model is also tweaked for optimization to try and improve the accuracy of the predictions. 

### Results:
#### Data Preprocessing:
The data was preprocessed for the model by dropping irrelevant columns, binning categorical data into fewer categories, using OneHotEncoder to encode the categorical data, and splitting the resulting dataset into training and testing data. 
- Target Variable: 
    - IS_SUCCESSFUL
- Feature Variables: 
    - APPLICATION_TYPE
    - AFFILIATION
    - CLASSIFICATION
    - USE_CASE
    - ORGANIZATION
    - STATUS
    - INCOME_AMT
    - SPECIAL_CONSIDERATIONS
    - ASK_AMT
- Irrelevant Variables:
    - EIN
    - NAME
#### Compiling, Training, and Evaluating the Model:
***Original Model*** Accuracy: 0.7235

***Optimization Attempt 1:*** Accuracy: 0.6949

I removed additional columns from the dataset (EIN, NAME, APPLICATION_TYPE, and CLASSIFICATION) to determine if those features were confusing the model, however the resulting accuracy is less than the accuracy from the original model.

***Optimization Attempt 2:*** Accuracy: 0.7242

I increased the number of neuron units in the model to 150 units for Layer 1 and 100 units for Layer 2 so that the model might better understand the complex relationships within the dataset. The resulting accuracy was slightly higher than the accuracy in the original model.

***Optimization Attempt 3:*** Accuracy: 0.7236

I increased the number of epochs while training the model to 70 epochs so that the model could have more attempts at learning from the data. This only increased the accuracy by .0001 from the original model.

***Optimization Attempt 4:*** Accuracy: 0.7238

I changed the activation function in the hidden layers of the model to the Tanh activation function to determine if it might be better at transforming the data and defining the output of the model. The resulting accuracy only had a slight increase compared to the original model.

***Optimization Attempt 5:*** Accuracy: 0.7224

I added 4 hidden layers and increased the number of epochs to 70 epochs, so that the model might be able to better understand the complexity of the data by having more neuron layers to pass through, and increased attempts at learning from the data. However, this resulted in a decrease in accuracy compared to the original model. 

Unfortunately, I was not able to increase the accuracy to the target rate of 0.75 in any of these optimization attempts.


### Summary:

### Software:
