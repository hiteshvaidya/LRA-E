# LRA-E
AAAI 2019 LRA-E Model

# We have provided scripts for training LRA-E on mnist and fmnist.

# How to run
* python mnist/mnist.py runs 4 layer MLP on mnist
* python fmnist/fmnist.py runs 4 layer MLP on fashion-mnist.

# Structure of code
We have structured code keeping following things in mind
* easy to modify
* our codebase maps with psuedo-code provided in our paper
* easy to convert for researchers familiar with other deep learning libraries(Pytorch/Theano).
* Using basic ops to understand the update rule for LRA-E 

Class MLP creates all the necesssary function
* Declare all the Weight and biases variables for the model.[How deeper you wish to go]
* forward :- Function does the forward pass for the model on cpu or gpu.
* compute_output:- gives you set of post and preactivations for the model.
* backward :- will help you calculating backpropagation (backprop) gradients and one step of SGD [Note: Can be replaced with any TF optimizer].
* compute_lra_update :- Will compute LRA_updates (instead of backprop)


We will be updating this repo to add more examples and also optimal training rules for LRA.

