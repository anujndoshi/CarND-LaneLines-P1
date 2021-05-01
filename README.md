
# **Finding Lane Lines on the Road** 
[![Udacity - Self-Driving Car NanoDegree](https://s3.amazonaws.com/udacity-sdc/github/shield-carnd.svg)](http://www.udacity.com/drive)

<img src="examples/laneLines_thirdPass.jpg" width="480" alt="Combined Image" />


# Reflection

1. Describe the pipeline.

We use multiple approaches, first one using the pipeline in which we perform transforms over multiple transformations as described in the outlined pipeline:
    Raw Image -- > Convert to Grayscale --> Apply Gaussian Blur --> Find Canny Edges -->
    Detect Region of Interest --> Detect Lines using Hough Transforms --> Add lines on original image.
    
    
   Raw Image ==
    <img width="293" alt="Raw" src="https://user-images.githubusercontent.com/37958757/116795654-910f7580-aaa4-11eb-9818-6a20909923c4.png">
    
   Convert to Grayscale == <img width="294" alt="Gray" src="https://user-images.githubusercontent.com/37958757/116795708-f4010c80-aaa4-11eb-86a5-47dc88834464.png">

   Blur Image == <img width="294" alt="Blur" src="https://user-images.githubusercontent.com/37958757/116795715-fc594780-aaa4-11eb-8536-67b1f38ff4ee.png">
    
   Edges == <img width="290" alt="Edges" src="https://user-images.githubusercontent.com/37958757/116795720-03805580-aaa5-11eb-9f34-adb842084724.png">
    
   Final Image == <img width="315" alt="Final" src="https://user-images.githubusercontent.com/37958757/116795725-0a0ecd00-aaa5-11eb-8764-2fe1c2e25fca.png">

2. Identify any shortcomings

   There are a few short comings in the following pipeline:
   
   Robustness:
   The following pipline tracks lines only in the specified ROI at the centre of the image and this can disallow it from being more roboust towards lines on the edges.
   Also the paramters are static and not adaptive. In case of varying line thickness or worn out lines such as on dusty roads this wont work very well. 
   
   

3. Suggest possible improvements

    - A posible parameter could be a dynamic way of updating the parameters.
    - I have also implemented a solution in the optional section using another color space and thresholding in order to detect stronger white edges in the HSV color space to filter out other noise. We can try something similar in order to preprocess information to retain only important details to make the pipeline faster.



