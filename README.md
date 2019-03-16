# KerasHyperOpt

A simple Keras example with automatic hyperparameter search using hyperopt

Hyperopt is used to search the best values for the decay rate, number of neurons, dropout rate, the momentum and the number of epochs to categorize MNIST.

The results will will look like the following: 

![Result of the search](pictures/decay.png?raw=true "Result of the search")


Since this was done with Tensorflow 1.12 which had a memory bug I had to implement some debug code.

The actual work around for the memory issue was done by the following line.

```tf.keras.backend.clear_session() #There is a memory leak in some tensorflow sessions```
