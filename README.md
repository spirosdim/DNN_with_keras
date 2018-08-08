# DNN_with_keras
Finding the right hyperparameteres for a Deep Neural Network with keras. Classification task with 7 classes. 
Use cartographic variables to classify forest categories.

# Deep Neural Network Architecture
- 2 hidden layers
- 54 -> 1024 -> 256 -> 7

### weight initialization 
- he_normal 
It draws samples from a truncated normal distribution centered on 0 with stddev = sqrt(2 / fan_in) 
where fan_in is the number of input units in the weight tensor.

### Activation functions
- RELU(Z) = max(0, Z)
- SOFTMAX(Z) = 1/(1+e^Z)

### Optimizer
Adam
- learning rate : lr=0.01 
- beta_1=0.9, beta_2=0.999  (paper's default)
- epsilon= 1e-08 (paper's default)
- learning rate decay: decay=0.1  
- batch size: 128
- epochs=200
- loss function: loss=categorical_crossentropy 

### Also used:
- Batch normalization to normalize the input layer by adjusting and scaling the activations
- Weight Regularization L2 to prevent overfitting

### In the end we check the loss and the accuracy over four different learning rates which is is one of the most important hyperparameters.
