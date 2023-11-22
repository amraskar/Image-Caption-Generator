# Image Caption Generator: Project Overview 
* In this project, i implemented the caption generator using CNN (Convolutional Neural Networks) and LSTM (Long short term memory).
* The image features will be extracted from Xception which is a CNN model trained on the imagenet dataset.
* And then i feed the features into the LSTM model which will be responsible for generating the image captions.

# Code and Resources Used 
**Python Version:** 3.11  
**Packages:** string, os, PIL, pickle, numpy, matplotlib, tensorflow, keras

# Dataset Used 
**Flicker8k_Dataset:** https://github.com/jbrownlee/Datasets/releases/download/Flickr8k/Flickr8k_Dataset.zip
**Flickr_8k_text:** https://github.com/jbrownlee/Datasets/releases/download/Flickr8k/Flickr8k_text.zip

# Data Cleaning
I needed to clean it up so that it was usable for our model. I made the following changes:

*	Removed Remove dash (-) from captions.
*	Converted captions to lowercase.
*	Removed punctuation.
*	Removed hanging 's and a.
*	Removed words with numbers in them.
*	Made columns for the number of actors in each movie.

# Xception Pretrained Model:
The image features will be extracted from Xception - pre-trained model that have been already trained on large datasets-.
I needed to preprocess the input image first so that it was usable for our model. I made the following changes:

*	Resized every image to (299, 299) -Xception's default input size-.
*	Added an extra dimension to the array to represent the batch size, because Xception is designed to process images in batches.
*	Made the range of pixel values [-1, 1].

# 
* Appended the =start= and =end= identifier for each caption.
* So that LSTM model can identify the starting and ending of the caption.

# Tokenizing the vocabulary
* To represent words with numbers.
* Map each word of the vocabulary with a unique index value.

# Create Data generator
* To make this task into a supervised learning task.
* I have to provide input and output to the model for training
* The input to the model is [x1, x2] and the output will be y where:
  
** x1 is the 2048 feature vector of that image
** x2 is the input text sequence
** y is the output text sequence -the next word in the sequence- that the model has to predict.
