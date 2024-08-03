# Image-Processing

## Introduction:

This project provides a set of tools for image processing, focusing on edge detection and seam carving techniques. The goal is to offer efficient methods for detecting edges in images and resizing images by removing low-energy seams. This project utilizes data preprocessing, custom filtering techniques, and advanced algorithms to achieve these tasks.

## Functions:

- MyCanny: The MyCanny function performs edge detection using the Canny edge detection algorithm. It includes steps for Gaussian blur, Sobel filtering, non-maximum suppression, and thresholding.
Parameters:
input_img: Input image as a NumPy array.
st_deviation: Standard deviation for Gaussian blur.
gm_threshold: Gradient magnitude threshold for edge detection.
Returns:
nms_img: Image after non-maximum suppression.
output_img: Binary image after thresholding.

- MyCannyFull: The MyCannyFull function extends the MyCanny function by incorporating hysteresis thresholding for edge linking.
Parameters:
input_img: Input image as a NumPy array.
st_deviation: Standard deviation for Gaussian blur.
gm_threshold: Gradient magnitude threshold for edge detection.
low_gm_threshold: Lower gradient magnitude threshold for hysteresis.
high_gm_threshold: Higher gradient magnitude threshold for hysteresis.
Returns:
output_img: Binary image after full edge detection and hysteresis.

- MySeamCarving: The MySeamCarving function resizes an image by removing seams with the least energy. This is useful for content-aware image resizing.
Parameters:
input_img: Input image as a NumPy array.
width: Desired width of the output image.
height: Desired height of the output image.
Returns:
output_img: Resized image after seam carving.

## Example Usage:

- Edge Detection:
The MyCanny_script.ipynb and MyCannyFull_script.ipynb notebooks demonstrate the edge detection functionalities.

MyCanny Script:
Loads and processes images for edge detection using the MyCanny function.
Applies the Canny edge detection algorithm and displays the results.
MyCannyFull Script:

Extends the edge detection process using the MyCannyFull function.
Incorporates hysteresis thresholding and displays the enhanced edge detection results.

- Seam Carving:
The MySeamCarving_script.ipynb notebook demonstrates the seam carving functionality.

MySeamCarving Script:
Loads an image and resizes it by removing low-energy seams using the MySeamCarving function.
Displays the original and resized images.

- Image Processing:
The combined script demonstrates both edge detection and enhanced edge detection with hysteresis thresholding.

image_processing Script:
Loads and processes images for edge detection using both MyCanny and MyCannyFull functions.
Applies edge detection and hysteresis thresholding and displays the results for comparison.

## Acknowledgements:

Thanks to the contributors and the open-source community for their support and resources. Special thanks to the developers of PyTorch and Kornia for providing the tools necessary for this project.
