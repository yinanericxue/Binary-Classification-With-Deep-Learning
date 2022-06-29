# Binary Classification With Deep Learning

## After learning the softmax regression algorithm, I was confident that I could design any classification models, no matter how many labels and features are present. However, after learning about the following dataset, I was speechless.

<img width="545" alt="Screen Shot 2022-06-28 at 8 03 59 PM" src="https://user-images.githubusercontent.com/102645083/176343140-fda8190b-d58a-4eb8-8b93-be2edaa1f610.png">

## While we could easily recognize the windmill-like patterns right away, it's impossible for a model to classify it using the classic ML algorithms. I initally thought that using KNN may do the trick, but the predictions near the outliers and center would be an absolute disaster. 

## This led me to the topic of Aritifical Neural Networks, which is a series of deep learning algorithms that simulates how the human brain process information, and it's especially useful for modeling non-linear statistical data, like what we have above. Every network starts with the input layer, where the initial data enters the workflow as artifical input neurons. They are inputted directly into the first of possibly many fully-connected hidden layers, where neurons go through a nonlinear transformation by taking in a set of weights and bias, and are outputted right away or through an activation function. This process applies to every hidden layer, and the outputs from the final hidden layer is called the Output Layer, where the conclusion can be made, and it can vary from percentages for regression problems to labels for classification problems. This entire workflow called Forward-Propagation, which is the process of calculation and storage of intermediate variables for a neural network, and every layer's input is the previous layer's output. The weights and bias are updated through every iteration, and it's important that we include a loss function after Forward-Progagation to compare the predictions to the actual values. 

<img width="626" alt="3-intro-deep-neural-networks" src="https://user-images.githubusercontent.com/102645083/176347293-f65a8a75-75bd-4521-9371-04941e70a4ee.png">

## The next part of this algorithm is called Back-Propagation, and I struggled a lot with understanding it. In classic ML algorithms, we have really have to deal with an enormous amount of variables, or the weights and bias that we are trying to find, and performing partial derivatives and optimization using gradient descent were quite straightforward. However, we can't do that for neural networks. If we think of an entire network as a function, every neuron / variable directly affects the final outcome. Complex network models can have millions of them, which means by just performing partial derivative on just one neuron, we need to take in account for the chain rule caused by every single other neuron. Doing such is virtually impossible, which is why Back-Propagation is so important. By using what we've already calculated using Forward-Propagation, we can find the error rate (dz/dc) for each neuron of every layer, which makes it very simple to find the partial derivatives in term of the weights and bias. In simpler words, the two propagations work simultaneously to fine-tune the weights and bias of the entire network through each iteration.

<img width="879" alt="Screen Shot 2022-06-28 at 9 27 44 PM" src="https://user-images.githubusercontent.com/102645083/176351694-baac47c0-4d72-4dd8-b895-21257f77aec4.png">

