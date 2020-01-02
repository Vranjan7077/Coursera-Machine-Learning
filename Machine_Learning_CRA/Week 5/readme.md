## Random Initialization ##
Initializing all theta weights to zero does not work with neural networks. When we backpropagate, all nodes will update to the same value repeatedly. Instead we can randomly initialize our weights for our Θ matrices using the following method:

![Image](https://github.com/Vranjan7077/Coursera-Machine-Learning-/blob/master/Machine_Learning_CRA/Week%205/random%20initialize.png?raw=true)

Hence, we initialize each Θ(l)ij to a random value between[−ϵ,ϵ]. Using the above formula guarantees that we get the desired bound. The same procedure applies to all the Θ's. Below is some working code you could use to experiment.


## Putting it Together ## 
First, pick a network architecture; choose the layout of your neural network, including how many hidden units in each layer and how many layers in total you want to have.

1)  Number of input units = dimension of features x^{(i)}x(i) <br/>
2)  Number of output units = number of classes <br/>
3)  Number of hidden units per layer = usually more the better (must balance with cost of computation as it increases with more hidden units) <br/>
4)  Defaults: 1 hidden layer. If you have more than 1 hidden layer, then it is recommended that you have the same number of units in every hidden layer.

### Training a Neural Network ###

1)  Randomly initialize the weights <br/>
2)  Implement forward propagation to get hΘ(x(i)) for any x^{(i)}x(i) <br/>
3)  Implement the cost function <br/>
4)  Implement backpropagation to compute partial derivatives <br/>
5)  Use gradient checking to confirm that your backpropagation works. Then disable gradient checking. <br/>
6)  Use gradient descent or a built-in optimization function to minimize the cost function with the weights in theta.

The following image gives us an intuition of what is happening as we are implementing our neural network:<br/>
![Image](https://github.com/Vranjan7077/Coursera-Machine-Learning-/blob/master/Machine_Learning_CRA/Week%205/put%202gether.png?raw=true)

