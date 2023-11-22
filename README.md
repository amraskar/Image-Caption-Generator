# Image Caption Generator: Project Overview 
* In this project, i implemented the caption generator using CNN (Convolutional Neural Networks) and LSTM (Long short term memory).
* The image features will be extracted from Xception which is a CNN model trained on the imagenet dataset.
* And then i feed the features into the LSTM model which will be responsible for generating the image captions.

## Code and Resources Used 
**Python Version:** 3.11  
**Packages:** string, os, PIL, pickle, numpy, matplotlib, tensorflow, keras

## Dataset Used 
**Flicker8k_Dataset:** https://github.com/jbrownlee/Datasets/releases/download/Flickr8k/Flickr8k_Dataset.zip
**Flickr_8k_text:** https://github.com/jbrownlee/Datasets/releases/download/Flickr8k/Flickr8k_text.zip

## Data Cleaning
I needed to clean it up so that it was usable for our model. I made the following changes:

*	Removed Remove dash (-) from captions.
*	Converted captions to lowercase.
*	Removed punctuation.
*	Removed hanging 's and a.
*	Removed words with numbers in them.
*	Made columns for the number of actors in each movie.

