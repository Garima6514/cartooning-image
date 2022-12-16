# cartooning-image
the main aim of this project is to detect objects or convert real life images into cartoon or cartoons into real images. 


Nowadays many different apps are available for the cartoonification of an image. The main aim of this article is not to simply build another tool for users to turn their favorite images into cartoon drawings but to draw their attention towards the coding side of it and how easily one can make their own program after learning the basics.
Here, we make use of OpenCV to convert an image into it’s cartoon form.

OpenCV -
OpenCV (Open Source Computer Vision Library) is an open-source computer vision and machine learning software library. OpenCV was built to provide a common infrastructure for computer vision applications and to accelerate the use of machine perception in commercial products. It is used to perform different operations on images that transform them using different techniques.
Step 1 — Installing OpenCV
To install OpenCV:

Step 2 — Importing necessary libraries
Import the following libraries in your notebook -

OpenCV
easygui
numpy
matplotlib.pyplot
imageio
Step 3 — Reading an image
Now for input, we need to select an image. Image can be selected from either your system or can be uploaded directly from the internet. Here, I’ve uploaded one from my system. For this, I’ve made use of easygui library.


The image is stored in img. In case no file is selected or the uploaded file format is not selected then a message as “Can not find any image. Choose appropriate file” will be displayed.

The image is by default read in BGR color palette. We need to convert it in RGB format.


Changing color palette
Next, we have to convert the image to grayscale -


Converting the image to grayscale
Step 4 — Median Blurring
3 types of blurring are available namely,

Gaussian Blur
Median Blur
Bilateral Blur
Here, we perform median blurring on the image. The central element of the image is replaced by the median of all the pixels in the kernel area. This operation processes the edges while removing the noise.


Median Blurring
Step 5 — Edge Mask
The next step is to create the edge mask of the image. To do so, we make use of the adaptive threshold function.

Adaptive thresholding is the method where the threshold value is calculated for smaller regions and therefore, there will be different threshold values for different regions.


Creating edge mask
Step 6 — Removing Noise
We need to get rid of the unwanted details of the image or the “noise”. In imaging, noise emerges as an artifact in the image that appears as a grainy structure covering the image.

To do so, we perform bilateral blurring.


Removing Noise
Step 7 — Eroding and Dilating
Erosion —

Erodes away the boundaries of the foreground object
Used to diminish the features of an image.
Dilation —

Increases the object area
Used to accentuate features

Eroding and Dilating an image
Step 8 — Stylization of an image
Now, we perform stylization on the image.


The stylization of the image
