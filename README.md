# JHub Coding Module 4C

This repository contains guidance and dataset resources for the JHub Coding Module, Challenge 4C.

## General Guidance and Information

The notebook provided is a template for completing Challenge 4C, and provides generic instructions for the challenge and what you need to achieve. It has been produced to improve the consistency of submissions, and to act as a basic starting point for the challenge. Despite this, the challenge still aims to give students a good amount of flexibility in applying a range of techniques and chosen processes to solve the challenge. This challenge is designed to be a considerable step-up compared to Challenge 4B, and as such should test the ability of students more thoroughly for applying various principles of data science and machine learning.

**Important:** Please do not change or modify the code within Sections 1-3 of the notebook, with exception to Section 2.2 for your chosen dependencies. The prepopulated code has been provided to save difficulties with downloading and extracting the dataset for this challenge. When you make a submission, your notebook will be tested in Google Colab, so it is essential that your code has been tested and works without any issues on the Google Colab platform. You need to populate the required functions for data preprocessing / preparation to solve this problem. All dependencies must be documented in Section 2.2.

**You can:** add further cells or text blocks to extend or further explain your solution add further functions

**Dont:** rename the helper functions and classes within the notebook, since this ensures consistency during testing of submissions.

---

## Challenge Overview and Description

### **1.1 Summary of Requirements:**

In summary, this challenge consists of the following tasks:

1. Loading and processing of a large image dataset, which is stored in a realistic directory structure.

2. Preprocessing and preparation of image data and labels into a suitable form for a DNN.

3. Model production, tuning and evaluation of performance on the image classification task using the training and test sets provided.

4. Final model predictions on a seperately held-out test set (supplied with no labels), and saving the prediction labels as .csv. A helper function is provided at the bottom of this template for loading this final data (labels are not provided).

---

### **1.2 Introducing the dataset and model requirements:**

For this challenge you must produce a functioning Deep Neural Network model that classifies a 32x32 RGB images into one of three possible classes: Aircraft, Ships or Automobiles. 

The dataset provided consists of two splits of data - the training and test splits. Each of these have been split using stratified sampling techniques, with an equal proportion of data available for each class, and so imbalanced data is not an issue in this challenge. 

Within each split, there are a large number of .png images for each class. These are organised into a directory structure, like so:

    - Train
        - aircraft 
            [1000 PNG formatted 32x32 RBG images]
        - automobile
            [1000 PNG formatted 32x32 RBG images]
        - ship
            [1000 PNG formatted 32x32 RBG images]
        
    - Test
        - aircraft
            [333 PNG formatted 32x32 RBG images]
        - automobile
            [333 PNG formatted 32x32 RBG images]
        - ship
            [333 PNG formatted 32x32 RBG images]
            

To complete the task, you must first load and preprocess the images into suitable training and test datasets, followed by the training, tuning and evaluation of a Deep Neural Network model. The aim is to produce a tuned model that generalises as highly to the test set as possible. 

As a rule of thumb, if you are achieving an accuracy of 75% or higher on the test set (having only trained on training data), your model is performing well.

You are not limited to a particular type of Deep Learning Model, and may apply any architecture type you like. However, for the purpose of this challenge you should use the TensorFlow and the Keras frameworks for model production.

---
### **1.3 Final predictions on held-out dataset:**

Once your model is finalised and you have evaluated the performance on the test dataset, you must make final predictions on a held-out private test set. This private test set can be loaded using the function provided at the bottom of this notebook. Please note - no labels are provided for this data, and it is up to you to provide labels for this data by making predictions with your model. The final prediction labels for these must be provided as a .csv with a label per row for each image. **Hint:** It's highly recommended to format your predictions as a Pandas series, followed by simply saving this as a .csv using .to_csv().

---