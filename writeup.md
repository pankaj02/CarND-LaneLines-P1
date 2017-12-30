# **Finding Lane Lines on the Road** 

## Writeup

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: test_images_output/solidWhiteCurve.jpg
[image2]: test_images_output/solidYellowCurve2.jpg

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps. 
* First, I converted the images to grayscale 
* removed noise by using GaussianBlur
* Find out edges using Canny 
* Define region of interest to remove unwanted lines
* Find out line using hough line

In order to draw a single line on the left and right lanes, I modified the draw_lines() function as ...
* taken slope of line between threshold 20 degree and 60 degree 
* taken average of positive and negative slope separately
* calculate average of x and y coordinates
* calculate average intercept b = y - mx
* draw line using y_min and y_max with x coordinate calculate as (y - b )/m


Images : 

![alt text][image1]
![alt text][image2]


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when other lanes are closer to predicted lane 
then predicted lane slopes are distorted resulting in wrong annotation of labe



### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...
