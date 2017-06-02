# **Finding Lane Lines on the Road** 

## Writeup Template

### You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report



[//]: # (Image References)

[image1]: ./test_images_out/gray_solidWhiteCurve.jpg "Grayscale"

[image2]: ./test_images_out/edges_solidWhiteCurve.jpg "Grayscale"

[image3]: ./test_images_out/med_solidWhiteCurve.jpg "Grayscale"

[image4]: ./ftest_images_out/line_solidWhiteCurve.jpg "Grayscale"

[image5]: ./ftest_images_out/lfinal_solidWhiteCurve.jpg "Grayscale"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 6 steps. 
1. I converted the images to grayscale, 

![alt text][image1]

2. I blurred the image.
3. I applied canny edge with low thresh:70 high thresh:100

![alt text][image2]

4. define a polygon for point of interest

![alt text][image3]

5. make a Hough transform with threshold : 10, min_line_length = 100, max_line_gap = 200
6. apply line images from step 5 to original image

![alt text][image5]


In order to draw a single line on the left and right lanes, I modified the draw_lines() function by ...

If you'd like to include images to show how the pipeline works, here is how to include an image: 

![alt text][image1]


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when ... 

Another shortcoming could be ...


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...
