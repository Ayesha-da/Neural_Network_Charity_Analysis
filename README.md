# Neural_Network_Charity_Analysis
## Overview of the loan prediction risk analysis:
To create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.
To design a neural network and create a binary classification model that can predict if an Alphabet Soup–funded organization will be successful based on the features in the dataset,determining the number of neurons and layers in model and finally compiling, training, and evaluating the model to determine model’s loss and accuracy.

![alphabet-soup](https://user-images.githubusercontent.com/84524153/137585675-124daf7b-4ba0-496a-bdac-13087b52f493.png)

## Results:


### Data Preprocessing
- What variable(s) are considered the target(s) for your model?

   "Is_successful" feature is considered the target of the model.
  
![feature2](https://user-images.githubusercontent.com/84524153/137585474-59dd988d-2c10-497d-af98-ca589125c29a.png)

- What variable(s) are considered to be the features for your model?

  Application_type, Affiliation, Classification, Use_case, Organization, Status, Income_amt, Special_considerations, Ask_amt are considered features of the model.

- What variable(s) are neither targets nor features, and should be removed from the input data?

  EIN and NAME are removed from the features.

![feature1](https://user-images.githubusercontent.com/84524153/137603247-5f048e8f-3114-410f-bfd2-0f82ad231261.png)

### Compiling, Training, and Evaluating the Model

- How many neurons, layers, and activation functions did you select for your neural network model, and why?
##### Neurons and Layers
Two layers were selected, first one with 80 neurons, second one with 30 neurons.

Neurons are added so there is a distributed effort to find optimal weights and each neuron can focus on different features to identify nonlinear effects and so is less likely to fixate on complex variables

These additional layers are added so they can observe and weight interactions between clusters of neurons across the entire dataset, which means they can identify and account for more information than any number of neurons in a single hidden layer.

##### Activation function

Hidden layers are activated using "relu" function and the output layer with "sigmoid" function.

Relu function is used since it is simple, fast, and empirically it seems to work well.

Sigmoid function is used since this function is differentiable and output values are bound between 0 and 1, normalizing the output of each neuron.

![layer](https://user-images.githubusercontent.com/84524153/137595873-4cb75f3b-480d-4dc9-b0b9-6ceb2cf6a2ed.png)
![layer_output](https://user-images.githubusercontent.com/84524153/137595879-1227379b-f962-46c9-9425-0d8af1ed3c2c.png)

- Were you able to achieve the target model performance?

  The model failed to reach the target performance of 75%
  
- What step did you take to try and increase model performance?
 
   ###### The hidden layers were increased and the nodes for each layer is adjusted.
   ###### Different activation function combinations were used on the model.
   ###### Ran the kerastuner search for best hyperparameters to evaluate best model against full test data.
   ###### Optimized the features for different combinations such as  type of organization, special considerations,use cases and ask amount.
 
 ###### kerastuner search
![kerasturner](https://user-images.githubusercontent.com/84524153/137595855-70bc51e4-354f-4d34-9e33-b95db51efe09.png)

![kerasturner_output](https://user-images.githubusercontent.com/84524153/137595861-403b99c4-5dba-4f16-8391-3b05998dbfc5.png)


## Summary:
