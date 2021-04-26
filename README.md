# CS585-Styler-Transfer

## What is Neural Style Transfer 
Neural style transfer is a optimization technique used to take two images, one is the content image, another is the style image. And the output image looks like the content image, but the style will look like the style reference image. Neural style transfer implemented by optimizing the output image to match the content statistics of the content image and the style statistics of the style reference image. These statistics are extracted from the images using a convolutional network.

## Project Overview
For this project, we mainly use TensorFlow_hub to realize style transfer. And our key points are not about to train an style transfer model. What we mind is what kind of styles are hard to learn or what kind of content pictures(especially face images) will fail to transfer. We try many groups of content images and style images to find problems in style transfer .

## Problems in Style Transfer
This session is about the problems we find during experiment.
### 1. falsely learn the color distribution of style images
When there is an obvious boundary between the upper and lower colors in the style image, the original image will retain such features after conversion, even if there is no obvious boundary between the upper and lower colors in the original image.
<p align="center">
  <img src="./pictures/problem1_1.png" height="300"/>
</p>
