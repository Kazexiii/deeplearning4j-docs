---
title: Deeplearning4j's Features
layout: default
---

# Features

Here's a non-exhaustive list of Deeplearning4j's features. **This is an outdated list.**

### Integrations

* Spark
* Hadoop/YARN
* Model Import from Keras

### APIs

* Scala
* Java 


### Libraries

* [ND4J: N-dimensional arrays for the JVM](http://nd4j.org)
* [libND4J: Native CPU/GPU operations for ND4J](https://github.com/deeplearning4j/deeplearning4j/tree/master/libnd4j)
* [DataVec: Data preparation for DL4J](https://github.com/deeplearning4j/deeplearning4j/tree/master/datavec)
* [Deeplearning4j](https://github.com/deeplearning4j/deeplearning4j/tree/master/deeplearning4j)

### Nets

* [Restricted Boltzmann machines](./restrictedboltzmannmachine.html)
* [Convolutional nets](./convolutionalnets.html)
* [Recurrent nets: Long Short-Term Memory (LSTM)](https://github.com/deeplearning4j/deeplearning4j/blob/master/deeplearning4j/deeplearning4j-core/src/test/java/org/deeplearning4j/models/classifiers/lstm/LSTMTest.java) (including bi-directional LSTMs)
* [Denoising and Stacked Denoising autoencoders](./denoisingautoencoder.html)
* [Deep autoencoders](./deepautoencoder.html)

Since Deeplearning4j is a composable framework, users can arrange shallow nets to create various types of deeper nets. Combining convolutional nets with recurrent nets, for example, is how Google accurately generated captions from images in late 2014.

### Tools

DL4J contains the following built-in vectorization algorithms:

* [DataVec: Machine Learning Data Pipelines for Vectorization/Tensorization](https://github.com/deeplearning4j/DataVec)
* Moving-window for images
* Moving-window for text 
* Viterbi for sequential classification
* [Word2Vec](./word2vec.html)
* [Bag-of-Words encoding for word count and TF-IDF](./bagofwords-tf-idf.html)
* [Doc2Vec for Paragraph Vectors](https://deeplearning4j.org/doc2vec)
* Constituency parsing
* [DeepWalk](http://arxiv.org/abs/1403.6652)

DL4J supports the following type of optimization algorithms:

* Stochastic gradient descent
* Stochastic gradient descent with line search
* Conjugate gradient line search (c.f. [Hinton 2006](http://www.cs.toronto.edu/~hinton/science.pdf))
* L-BFGS

Each of these optimization algorithms may be paired with training features (known as 'updaters' in DL4J) such as:

* SGD (learning rate only)
* Nesterovs momentum
* Adagrad
* RMSProp
* Adam
* AdaDelta

### Hyperparameters

* Dropout (random ommission of feature detectors to prevent overfitting)
* Sparsity (force activations of sparse/rare inputs)
* Adagrad (feature-specific learning-rate optimization)
* L1 and L2 regularization (weight decay)
* Weight transforms (useful for deep autoencoders)
* Probability distribution manipulation for initial weight generation
* Gradient normalization and clipping

### Loss/objective functions

* MSE: Mean Squared Error: Linear Regression
* EXPLL: Exponential log likelihood: Poisson Regression
* XENT: Cross Entropy: Binary Classification
* MCXENT: Multiclass Cross Entropy
* RMSE_XENT: RMSE Cross Entropy
* SQUARED_LOSS: Squared Loss
* NEGATIVELOGLIKELIHOOD: Negative Log Likelihood

### Activation functions 

Activations functions are defined in ND4J [here](https://github.com/deeplearning4j/deeplearning4j/tree/master/nd4j/nd4j-backends/nd4j-api-parent/nd4j-api/src/main/java/org/nd4j/linalg/api/ops/impl/transforms)

* ReLU
* Leaky ReLU
* Tanh
* Sigmoid
* Hard Tanh
* Softmax
* Identity
* [ELU](http://arxiv.org/abs/1511.07289): Exponential Linear Units
* Softsign
* Softplus
