# **Finding Lane Lines on the Road** 
[![Udacity - Self-Driving Car NanoDegree](https://s3.amazonaws.com/udacity-sdc/github/shield-carnd.svg)](http://www.udacity.com/drive)

<img src="examples/laneLines_thirdPass.jpg" width="480" alt="Combined Image" />


# Reflection

1. Describe the pipeline.

We use multiple approaches, first one using the pipeline in which we perform transforms over multiple transformations as described in the outlined pipeline:
    Raw Image -- > Convert to Grayscale --> Apply Gaussian Blur --> Find Canny Edges -->
    Detect Region of Interest --> Detect Lines using Hough Transforms --> Add lines on original image.
    
    ![Raw Image](./Raw.png)

2. Identify any shortcomings

3. Suggest possible improvements





