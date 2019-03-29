# 06-02

## Challenge 02 - Eye Tracking

![](https://images.unsplash.com/photo-1531704118376-ec637130bfa0?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1050&q=80)

Photo by [Eduardo Mallmann](https://unsplash.com/photos/3LPGWASiSbM)

## Guidelines

### Introduction

Today will be a mini project based on Eye Tracking. A bit of context first. You have two folders:
* `close`
* `open/train`
* `open/test`

In those folders, are present images of eyes, either opened or closed. You will have two main tasks:
* Classification: make a classifier that predicts whether the eye is opened or closed
* Regression: make a regression that predicts the center of the pupil

Before doing so, you have to handle properly the images.

### Data Exploration
First, look at the data, open an image, display it, convert it to an array.
Feel free to use keras methods `load_img` and `img_to_array`.

### Classification

Your first task will be to make a classifier that detects either an eye is closed or not based on a picture.
To do so, use the data from `close` and `open/train`. You have to load all the data into an array `X` and labels into `y`. Then perform data preparation, and finally model building and training.

### Regression

Your second task will be to predict the center of an eye using regression, using the target values into the file `open/train/dataPupilCenter.csv`

In this file, for each eye, the center is labeled. Then test your model performance on the data into `open/test`.

The main idea is not really to find the perfect center, but to allow then to have a region of interest around the eye for further processing, like in the following image:

![](../../00-Lectures/images/eye_box.png)
