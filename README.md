# Project 3
### Cluster Analysis through unsupervised learning on Fashion MNIST image dataset using K-means algorithm, Auto-Encoder based K-means clustering model and Auto-Encoder based Gaussian Mixture Model

CSE 474/574: Introduction to Machine Learning 
(Fall 2019) 

Sargur N. Srihari 
University at Bufalo,

The State University of New York 
Bufalo, New York 14260

September 9, 2019

## 1 Task
The task of this project is to perform cluster analysis on fashion MNIST dataset using unsupervised
learning. Cluster analysis is one of the unsupervised machine learning technique which doesn't require
labeled data.
Your task will be that of clustering images and identify it as one of many clusters. You are required
to train your unsupervised model using Fashion-MNIST clothing images. Following are the three tasks
to be performed:

1. Use KMeans algorithm to cluster original data space of Fashion-MNIST dataset using Sklearns
library.
2. Build an Auto-Encoder based K-Means clustering model to cluster the condensed representation
of the unlabeled fashion MNIST dataset using Keras and Sklearns library.
3. Build an Auto-Encoder based Gaussian Mixture Model clustering model to cluster the condensed
representation of the unlabeled fashion MNIST dataset using Keras and Sklearns library.
Report the clustering accuracy for each of the task.

## 2 Dataset
For training and testing of our clustering models, we will use the Fashion-MNIST dataset. The
Fashion-MNIST is a dataset of Zalando's article images, consisting of a training set of 60,000 examples
and a test set of 10,000 examples. Each example is a 28x28 grayscale image.
Each image is 28 pixels in height and 28 pixels in width, for a total of 784 pixels in total. Each
pixel has a single pixel-value associated with it, indicating the lightness or darkness of that pixel, with
higher numbers meaning darker. This pixel-value is an integer between 0 and 255. The training and
test data sets have 784 columns. You can import the Fashion MNIST dataset using keras library.

## 3 Plan of Work
1. Extract feature values: Fashion MNIST dataset is downloaded and processed into a Numpy
array that contains the feature vectors and a Numpy array that contains the labels.

2. K-Means Clustering: Use Sklearns library to cluster Fashion MNIST dataset into 10 clusters.
Report the clustering accuracy.

3. Train using Auto-Encoder Network: Use Keras library to build a Auto-Encoder Network.

4. Create K-Means clustering layer: By training the auto-encoder, we have the encoder learned
to compress each image into latent 
oating point values. We are going to use K-Means to generate
the cluster centroids, which is the 10 cluster centers in the latent feature space. We then cluster
compressed latent codes produced by AutoEncoder using K-Means.

5. Create GMM clustering layer: Similar to Step 4, we are going to use Gaussian Mixture
Model to generate the cluster centroids, which are the 10 cluster centers in the latent feature
space (Latent space provided by pre-trained encoder network)

6. Test your machine learning scheme: Create a confusion matrix and report the clustering
accuracy by matching the clustering assignment for step 2, 4 and 5.
