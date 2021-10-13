<img src="https://github.com/NikolaZizic/2-layered-Data-Science-Project-Object-Detection-with-OpenCV-and-Tensorflow/blob/main/images/background%201.jpg" width="988" height="250" />

# A 2-layered Data Science Project : Object Detection with OpenCV and Tensorflow

## Table of Content
  
  * [Overview](#overview)
  * [Technical Aspect](#technical-aspect)
  * [Installation](#installation)
  * [Part 1: Face detection with OpenCV](#face-detection)
  * [Part 2: Hand gesture detection with Tensorflow](#hand-gesture)
  * [Technologies Used](#technologies-used)
  * [Team](#team)
 






## Overview
Our idea was to do two separate object detection applications, one that would detect different hand gestures and the other that would detect the face of the user and thus serve as a type of password to the main app. Plus we would use the different hand gestures that we have fed to the learning model to influence certain tasks on our computer like for example: if the app detects a thumbs up gesture it would increase the volume or maybe open Google Chrome etc. For this project, we will be using Tensorflow and OpenCV.
 

## Technical Aspect 

```bash
import PIL
from colorthief import ColorThief
import io
```
## Installation

The code is written in Python 3.8.5 . If you don't have Python installed you can find it [here](https://www.python.org/downloads/). If you are using a lower version of Python you can upgrade using the pip package, ensuring you have the latest version of pip.

<div id='face-detection'/>

## Part 1: Face detection with OpenCV

For the first part of our project we used OpenCV in order to, at first time, train and then build a model capable to recognize the user, once the user is recognized Part 2 of project will began. 

### Modules used

```bash
import numpy as np
import cv2
import pickle
import statistics as stat
```

The main module for us was OpenCV, and its prebuilt algorithms called cascades. So before you begin make sure that you have modules needed, and pay attention to where you install OpenCV because you will need that file path in order to access cascades. Even if you forget the file location, don’t panic you can always use *[this command](#command).

<div id='command'/>
```bash
import cv2
print(cv2.__file__)
```


<div id='hand-gesture'/>

## Part 2: Hand gesture detection with Tensorflow



> STEP 1



#### Windows User

The whole project is built on a Windows OS.  





> STEP 2


#### Collecting images

The first thing is to collect the images. Usually, for a good detection model, at least 20+ images for each label would be required. Since we are using a Tensorflow prebuilt model, the more images we feed our model the more it will be precise but it will also increase the training time. 

#### Labelling Images

We will be using Labelimg that is a graphical image annotation tool. The idea is to clone the repo into a new directory on our PC. In order to run the program there is a few packages that will be needed; The code can be found in the jupyter notebook.

<img src="https://github.com/NikolaZizic/2-layered-Data-Science-Project-Object-Detection-with-OpenCV-and-Tensorflow/blob/main/images/labelimg.jpg">





> STEP 3 


#### Choosing and training the model 

We will be using the Tensorflow zoo that can be found  [here](https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/tf2_detection_zoo.md). When it comes to choosing a pre trained model to implement there is a few things to keep in mind. Usually a model that does faster detections does it with a smaller accuracy and a slow detection model can perform with a higher accuracy. Therefore, there is a tradeoff between speed and accuracy. Choosing a model will depend on the problem that you are trying to solve.  Since we want a model with an optimal balance between accuracy and speed, and a box shaped output for our detections, we decided to take the SSD MobileNet V2 FPNLite 320x320. It is also possible to use your GPU using cuda to train your model. Since we are using our laptops (that are relatively weak), we will be doing it using only our CPU. 

If you are using a weaker PC/ laptop this can take quite a long time to train even for only 2000 steps. It can cause high temperatures inside your hardware so try to lower the temperature as much as you can. An external fan helped us a lot. 

<img src="https://github.com/NikolaZizic/2-layered-Data-Science-Project-Object-Detection-with-OpenCV-and-Tensorflow/blob/main/images/heat%20cmd.JPG">

When the model finishes training, you can see the training metrics with Tensorboard using your localhost:6006.

<img src="https://github.com/NikolaZizic/2-layered-Data-Science-Project-Object-Detection-with-OpenCV-and-Tensorflow/blob/main/images/Tensorboard%20train%20merics.JPG">



## Technologies Used

<img src="https://github.com/NikolaZizic/2-layered-Data-Science-Project-Object-Detection-with-OpenCV-and-Tensorflow/blob/main/images/python%20logo.png" width="232" height="75" />
<img src="https://github.com/NikolaZizic/2-layered-Data-Science-Project-Object-Detection-with-OpenCV-and-Tensorflow/blob/main/images/opencv-logo.png" width="232" height="75" />
<img src="https://github.com/NikolaZizic/2-layered-Data-Science-Project-Object-Detection-with-OpenCV-and-Tensorflow/blob/main/images/tensorflow.png" width="232" height="75" />






## Team

Nikola Zizic

Andrija Lucic
