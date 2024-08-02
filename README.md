# CV_scene_recognition
This project focuses on scene recognition using various image feature extraction techniques and classification methods. The goal is to classify images into predefined categories using computer vision and machine learning approaches.

#Features

The project implements three different image feature extraction methods:

1. Tiny Image Features: Inspired by the "80 Million Tiny Images" dataset. Each image is resized to a very small resolution (e.g., 16x16), converted to grayscale, flattened into a 1D array, and normalized.

2. Bag of Words: Utilizes HOG (Histogram of Oriented Gradients) features. The project builds a vocabulary of visual words using K-means clustering on HOG descriptors sampled from the training images. The images are then represented as histograms of these visual words.

Classifiers
Three different classification methods are implemented:

1. Nearest Neighbor Classifier: Finds the k-nearest neighbors of a test image in the feature space and assigns the most common category among them as the predicted label.

2. Support Vector Machine (SVM) Classifier: Uses linear SVM to classify images based on their feature representations. It trains multiple one-vs-all SVM classifiers and uses them to predict the categories of test images.


#Steps
Step 1: Represent Each Image with Appropriate Features

## Tiny Image Features:

*  Resizes the original image to a small resolution (16x16).
* Converts to grayscale.
* Flattens into a 1D array and normalizes.

## Bag of Words:

* Computes HOG descriptors for each image.
* Builds a vocabulary using K-means clustering on the HOG features.
* Represents each image as a histogram of visual words from the vocabulary.
## Step 2: Classify Each Test Image
* Nearest Neighbor: Classifies by finding the closest training images in the feature space.
* Support Vector Machine: Classifies using trained SVM models.

## Step 3: Evaluate the Recognition System
* Builds a confusion matrix to evaluate performance.
* Outputs results on a webpage to visualize and interpret classifier performance.

Usage
Run the project using the command line:
```
python main.py [-f | --feature <representation to use>] [-c | --classifier <classifier method>]

```

Example Command
```
python main.py -f tiny_image -c nearest_neighbor
```

Screenshots

<img width="1082" alt="Screenshot 2024-08-02 at 1 08 31 PM" src="https://github.com/user-attachments/assets/17e712b6-53a5-4caa-b390-896c57ee917b">

