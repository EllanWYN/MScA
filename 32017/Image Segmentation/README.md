# MScA 32017 Advanced Machine Learning - Image Segmentaion Project

This project involves training a UNet Neural Network on a series of satellite
images to classify pixels in the images into one of five classes: trees, crops,
roads, buidlings, or water.

The four IPython notebooks were provided by the instructor. They show:  
  1. [The basics of image segmentation](MScA_32017_ImageSegmentation1_Basics.ipynb)
  2. [What the training images look like and how to manipulate them](MScA_32017_ImageSegmentation2_DataExploration.ipynb)
  3. [How to build and train a UNet](MScA_32017_ImageSegmentation3_UNetSimple.ipynb)
  4. [Project insructions](MScA_32017_ImageSegmentation4_ProjectInstructions.ipynb)

The basis of the project is to take the base code, add improvements, and 
submit the test output to a server that will calculate the weighted logloss 
against a known mask. The target logloss is under 0.2

## Record of Attempts

### Attempt 1

I first ran the batch code unaltered on the dataset to make sure that everything
worked correctly and the output matched on upload.

I got a logloss of 0.36 for a score of 76%

## Attempt 2

My first change will be by editing the `get_rand_patch()` function. As suggested
by the project instructions, I've edited this function to randomly rotate the 
selected patch and mask after selection but before sending it to training.

I got a logloss of 0.35 for a score of 78%

Not much of an improvement.

## Attempt 3

Adding batch normalization and dropout layers to each level both down and up
the UNet.

Weighted logloss 0.347886 score of 79%

## Improved Prections

At this point it made sense to write the prediction algorithm to predict on 23 
images and test on the 24th before training on the entire set and then looking
at the test file.

## Attempt 4




