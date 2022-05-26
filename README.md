# **Region Based Convolutional Neural Network**


![p](https://github.com/MarwanMohamed95/Region-Based-Convolutional-Neural-Network-R-CNN/blob/main/test.png?raw=true)

- In this project we will implement R-CNN on raccoon dataset toclassify the image as raccoon or not raccoon.


![photo](https://miro.medium.com/max/1400/0*Esmqth8McxPM2YtB.png)
- The R-CNN works as follow:
  - First Input the image.
  - Extract Regions that might have object using selective search on the input image.
  - Compute IOU between the region and the true bounding box to label the regions according to their classes.
  - Training the CNN Model on the regions with softmax in the last layer to classify them which region region belongs to which class.


## Steps of the Project:
    - 1. Importing Libraries
    - 2. Loading images and annotations
    - 3. Defining different pathes and variables
    - 4. Defining a method to compute IOU
    - 5. Preparing the data for training the model
    - 6. Defining the model (MobileNetV2)
    - 7. Evaluating the model
    - 8. Testing the model on input image

### - Intersection Over Union:

  - In order to define whether the region proposal is positive or negative we compute the iou between the proposed region and the grouund truth bounding box so if iou is greater than 0.7 the region will be labeled as +ve class (contains the raccoon) but if iou is less than 0.05 it will be classified as -ve class (not contatins the raccoon).
  - The IoU method computes the ratio of the area of overlap to the area of the union between the predicted bounding box and the ground-truth bounding box:

![photo](https://929687.smushcdn.com/2633864/wp-content/uploads/2016/09/iou_equation.png?raw=true&lossy=1&strip=1&webp=1)


### Model Evaluation 

![p](https://github.com/MarwanMohamed95/Region-Based-Convolutional-Neural-Network-R-CNN/blob/main/evaluation.png?raw=true)