# Neural Network Activation Functions

Activation functions are one of the most important features of artificial neural networks. These mathematical functions mainly decide whether 
the succeeding neuron should get activated or not based on the input from the preceding neuron. This activation functions does the non-linear 
transformation and makes the network capable to learn and perform complex tasks. 

The most used activation functions are discussed below along with their advantages and disadvantages:

## Step Activation Function  

Step Function: is a threshold based activation function where the neuron gets activated if the input value satisfies the threshold factor. 
The signal sent to the succeeding layer is identical to the preceding layer.  

<p align="center">
<img src="https://github.com/arghadeep25/Neural-Network-Activation-Functions/blob/master/plots/step.png" width="600"> 
</p>

**Advantages**:  
- Ideal for binary classifiers.  

**Disadvantages**:  
- As gradient of this function is zero, this function cannot be used during backpropagation. This function will not lead to any improvement of error  


## Linear Activation Function  

Linear Function: is a linear activation function which results a product of the weight A and the input from each neuron. The output from this activation 
function is proportional to the input value. This activation function allows multiple output rather than 0 and 1.  

<p align="center">
<img src="https://github.com/arghadeep25/Neural-Network-Activation-Functions/blob/master/plots/linear.png" width="600"> 
</p>

**Advantages**:  
- Ideal for simple tasks where interpretability is desired.  

**Disadvantages**:  
- Derivative of linear function is constant.  
- It is independent of the input i.e while backpropagating as the gradient is constant there is no improvement in error.  

## Sigmoid Activation Function  

Sigmoid: is a non-linear 'S' shaped activation function. To overcome the limitations of binary step function and linear function, sigmoid function came forward. 
The results produced by sigmoid function is non-linear which mainly helps during backpropagation. The value of the output is limited to 0 and 1 i.e. the function 
is asymmetric around the origin. On top of that, derivative of sigmoid function is smooth and differentiable everywhere on the curve.  

<p align="center">
<img src="https://github.com/arghadeep25/Neural-Network-Activation-Functions/blob/master/plots/sigmoid.png" width="600"> 
</p>

**Advantages**:  
- Non-linear activation function which helps during backpropragation.  
- Results smooth gradient which helps to eliminate oscillation in output value.  
- The output values are bound to 0 and 1.   

**Disadvantages**:  
- For very low and high value of \textit{x}, there will be almost no changes to prediction. Thus causing vanishing gradient problem i.e. 
the network refuse to learn hence saturate the network.  
- Outputs are not zero centered.  
- Sigmoid function is computationally expensive.  

## TanH Activation Function  

Tanh: is a non-linear activation function which is quite similar to sigmoid function. In case of sigmoid function the output bounds are limited to
0 and 1 but in this case the outputs are limited to -1 and 1. As this function is non-linear, it helps during backpropagation. 
As the function is quite similar to sigmoid, it holds almost same properties like continuous and differentiable at all points.  

<p align="center">
<img src="https://github.com/arghadeep25/Neural-Network-Activation-Functions/blob/master/plots/tanh.png" width="600"> 
</p>

**Advantages**:  
- Non-linear activation function which helps during backpropagation.  
- As the function is zero centered, it gives the flexibility to chose models with strong negative and positive values.  

**Disadvantages**: 
- Likewise sigmoid function, tanh also encounter the vanishing gradient problem. Hence get saturated during training. 

## Rectified Linear Unit Activation Function  

ReLU: also known as Rectified Linear Unit is one of the most widely used activation functions. Though it is named as linear, in reality ReLU 
is a non-linear activation function. This helps during backpropagating errors and activating multiple layers of neurons. 
The main advantage of ReLU is it does not activate all the neurons at a same time. From fig. it is quite evident that when it receive negative inputs 
it convert the inputs to zero and the succeeding neurons doesn't get activated. It gives a flexibility while training a deep neural network as it makes 
the network sparse. Hence the network becomes computationally inexpensive and efficient.  

<p align="center">
<img src="https://github.com/arghadeep25/Neural-Network-Activation-Functions/blob/master/plots/relu.png" width="600"> 
</p>

**Advantages**: 
- As it doesn't activate all the neurons at the same time hence it makes computationally efficient i.e. allows the network to converge rapidly.  
- Non-linear activation function which allows backpropagation.  


**Disadvantages**:  
- Dying ReLU problem - arises when no weight is updated during training and the network results identical output over iterations.  
- This is caused when a large gradient flows through ReLU neuron during weight update.  

## Leaky Rectified Linear Unit  

Leaky ReLU: To overcome the dead neuron problem of ReLU, leaky ReLU came forward. ReLU doesn't consider the negative values hence it start from 0 and goes 
accordingly. In case of leaky ReLU, a small linear component of x is defined as shown in fig. This linear component removed the zero gradient problem in case 
of ReLU as shown in fig. Hence, this eradicate the dead neuron problem. 

<p align="center">
<img src="https://github.com/arghadeep25/Neural-Network-Activation-Functions/blob/master/plots/leaky.png" width="600"> 
</p>

**Advantages**: 
- Eradicate the dead neuron problem of ReLU.  
- Non-linear activation function which allows backpropagation.  
- Likewise ReLU, leaky ReLU also do not activate all the neurons at a same time.  


**Disadvantages**:  
- Results are not consistent for negative input values.

