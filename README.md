# Neural Network Charity Analysis

## CWRU Module 19 Challenge

## Overview of the Project
The purpose of this project is to use deep-learning neural networks with the TensorFlow platform in Python, to analyze and classify the success of charitable donations.

### Summary

The effort involved using Tensorflow and Sklearn to build neural network models.  The data was preprocessed, split into trainging and evaluation segments and NN models were run to train and then assess the NN models efficacy with several rounds using different parameters to attempt to get to 75% accuracy.   This was not possible and, therefore, the models do not predict the outcome of the charity donations effectively. 


### Deliverable 1: Preprocessing Data for a Neural Network Model

* The columns EIN and NAME were removed
* The column IS_SUCCESSFUL is binary refering to charity donation being effective and is the target 
* The columns APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT are the features for the model and are categorical variables which were encoded, grouped and split into training testing datasets and then standardized using standardScaler


**Drop EIN and Name columns** 

![img](https://github.com/fhsal/Neural_Network_Charity_Analysis/blob/main/images/drop_EIN_Name.png)


**Application count distribution** 

![img](https://github.com/fhsal/Neural_Network_Charity_Analysis/blob/main/images/application_counts_profile.png)

**grouping**

![img](https://github.com/fhsal/Neural_Network_Charity_Analysis/blob/main/images/application_other.png)

**Classification count distribution** 

![img](https://github.com/fhsal/Neural_Network_Charity_Analysis/blob/main/images/classification_counts_profile.png)

**grouping**

![img](https://github.com/fhsal/Neural_Network_Charity_Analysis/blob/main/images/classification_other.png)


### Deliverable 2: Compile, Train, and Evaluate the Model
involved adding major earthquake data as a layer to the map, as for tectonic plates.  As these overlay with the existing earthquake data it was necessary to modify the rendering so that the major earthquakes could be easily visible on the map

**Complile model**

![img](https://github.com/fhsal/Neural_Network_Charity_Analysis/blob/main/images/compile_model.png)

**Train model**

![img](https://github.com/fhsal/Neural_Network_Charity_Analysis/blob/main/images/train_model.png)


**First round with model, 100 Epochs** 

![img](https://github.com/fhsal/Neural_Network_Charity_Analysis/blob/main/images/round_one.png)

### Deliverable 3: Optimize the Model
The NN model has two hidden layers with 80 and 30 neurons respectively.  The output layer is binary classification using Sigmoid.   The activation function is Relu and optimization is adam with loss function of binary_crossentropy.  Model accuracy is slightly under 73%. 

Increasing the number of layers (e.g., 200, 500) and using different activation functions (e.g., Tanh) does not improve model performance 

**Second round with model, 500 Epochs** 

![img](https://github.com/fhsal/Neural_Network_Charity_Analysis/blob/main/images/round_two.png)

**Using Tanh** 

![img](https://github.com/fhsal/Neural_Network_Charity_Analysis/blob/main/images/tanh_one.png)

**Second round with model** 

![img](https://github.com/fhsal/Neural_Network_Charity_Analysis/blob/main/images/round_two.png)

**Adding a third layer** 

![img](https://github.com/fhsal/Neural_Network_Charity_Analysis/blob/main/images/3_layers_1.png)
![img](https://github.com/fhsal/Neural_Network_Charity_Analysis/blob/main/images/3_layers_2.png)
![img](https://github.com/fhsal/Neural_Network_Charity_Analysis/blob/main/images/3_layers_3.png)

## Summary
The NN model did not reach the target of 75% accuracy.  As this is a binary classification, a supervised machine learning model such as the Random Forest Classifier or other ensembleor vector models might produce better results.