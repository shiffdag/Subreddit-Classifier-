# Drowsiness Detector and Eye Tracking 
------------------------------------------------------------------------------------------------------------------

## Executive Summary 
------------------------------------------------------------------------------------------------------------------

The underying goal of this project is to serve two purpuses: 1) detect drowsy related signs and indicators that someone is exhibiting when they are operating a car 2) Detect lack of attention of a person operating a car by mechansim of tracking the direction of their eye gaze. The app will raise an alarm in several number of instances. An alarm will be raised if the driver is either: shutting their eyes, blinking too frequently, yawning, not looking at the road, or starting at one direction for a prolonged amount of time. The purpose of the alarm is to mitigate careless driving or the drowsiness of a driver that may lead to a collision or accident. 


## Problem Statement
----------------------------------------------------------------------------------------------------------------------
Drowsy Driving is a detriment and has been the root cause for many mortalities. A poll conducted by the AAA Foundation found that one in three admitted to driving drowsy in the past month. And shockingly, 37% of people confessed that they had actually dozed off at the wheel in the U.S. In European countries, drowsy driving accounts for 10 to 30% of all crashes.  An estimated 1 in the past 25 adult drivers report having fallen asleep. An estimated 1 in the past 25 adult drivers report having fallen asleep while driving in the previous 30 days.  The national highway traffic administration estimates that drowsy driving was responsible for 72,000 crashes, 44,000 injuries, and 800 deaths in 2018.  



## Table of Contents 
[Sample Data ](https://git.generalassemb.ly/shiffraw/Capstone-Project/tree/master/data)

[Method 1 ](https://git.generalassemb.ly/shiffraw/Capstone-Project/blob/master/method1modeling.ipynb)

[Method 2 ](https://git.generalassemb.ly/shiffraw/Capstone-Project/blob/master/method2modeling.ipynb)

[Power Point Slides ](https://git.generalassemb.ly/shiffraw/Capstone-Project/blob/master/powerpoint%207.pptx)










## Methodology 

Two underlying approaches were implemented in regards to drowsiness detection.  

### Method 1 
The first approach consisted of using the MRL dataset which contains 84,000 images of grayscale images. Each image is of a person with closed eyes or open yes.  A classification model was utilized to classify an image as either belonging to the  closed or open eyes category. The model that was used for classification is a neural network known as MobileNet.  MobileNets are small, low-latency, low-power models parameterized to meet the resource constraints of a variety of use cases. They can be built upon for classification, detection, embeddings and segmentation similar to how other popular large scale models, such as Inception, are used. MobileNet uses Depthwise Separable Convulution. Depthwise separable convolution is a depthwise convolution followed by a pointwise convolution. My model's accuracy was 0.95. For object detection Haar Cascades was utilized. Haar Cascade is a machine learning object detection algorithm used to identify objects in an image or video and based on the concept of features proposed by Paul Viola and Michael Jones in their paper "Rapid Object Detection using a Boosted Cascade of Simple Features" in 2001. In addition, OpenCV was utilized in this project. 

### Method 2 
The second method consists of contructing a facial landmark detector that will assign keypoints to various regions of the face. The facial landmark detector attempts to localize and label the regions such as: mouth, right eyebrow, left eyebrow, left eye, right eye, nose, and jaw. The facial landmark detector that was used is an implementation of the paper “ One Millisecond Face Alignment with an Ensemble of Regression Trees”  by Kazemi and Sullivan (2014). The method starts by using: 1) a training set of labeled facial landmarks on an image. These images are manually labelled, specifying particular (x,y) coordinates of regions surrounding each facial structure 2) Priors, of more specifically, the probability on distance between pairs of input pixels. Given this training data, an ensemble of regression trees are trained to estimate the facial landmark positions directly from the pixel intensities themselves. The end result is a facial landmark detector that can be used to detect facial landmarks in real-time. The distance between the keypoints that sit along the top and buttom are utilized to determine if someone is closing their eyes or not.  Additionally, eye tracking will be implemented by gauging where a vast majority of the sclera of the eye is located.  When someone is looking to their right, the sclera, sits on the left part of the eye and when someoene looks to their left the sclera sits on the right part of the eye. Given the pixel gradient or difference betwewen the sclera and the iris, or pupil, distinguishing between the sclera and non-sclera regions are able to be determined.  A GUI, using Tkinter, was used to implement this method. An alarm is raised when someone is closing their eyes, blinking excesivel and if someone is staring too much in one direction (left, right, center.  





## Conclusion 

In order to increase the quality and efficacy of this app, yawning and nodding detection will be added. 
The alarm as of now goes off when the drowsiness detectors automatically goes off. In order to improve the model
intervals over time frame will be used to stimulate the alarm insteam of an instantaneous alarm. The amalgamation of various indicators of drowsiness were utilized in determing what to look out for when to raise the alarms in the app.  










