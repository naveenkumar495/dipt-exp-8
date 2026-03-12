# EXP NO : 08-THRESHOLDING
# Name : Naveenkumar M
# Reg NO : 212224230183
## Aim
To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm

### Step1:
Load the necessary packages

### Step2:
Read the Image and convert to grayscale
### Step3:
Use Global thresholding to segment the image.

### Step4:
Use Adaptive thresholding to segment the image.

### Step5:
Use Otsu's method to segment the image and display the results.>

## Program

~~~python
# Load the necessary packages
~~~python
import cv2
import numpy as np
import matplotlib.pyplot as plt
~~~


# Read the Image and convert to grayscale

~~~python
image = cv2.imread('naveen.tif')  # Replace with your image file path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
~~~


# Use Global thresholding to segment the image
~~~python
_, global_thresholded = cv2.threshold(gray_image, 127, 255, cv2.THRESH_BINARY)

~~~

# Use Adaptive thresholding to segment the image
~~~python
adaptive_thresholded = cv2.adaptiveThreshold(gray_image, 255, cv2.ADAPTIVE_THRESH_GAUSSIAN_C, cv2.THRESH_BINARY, 11, 2)
~~~


# Use Otsu's method to segment the image 
~~~python
_, otsu_thresholded = cv2.threshold(gray_image, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)

~~~
# Display the results
~~~python
plt.subplot(2, 2, 2)
plt.imshow(global_thresholded, cmap='gray')
plt.title("Global Thresholding")
plt.axis('off')

# Adaptive Thresholding
plt.subplot(2, 2, 3)
plt.imshow(adaptive_thresholded, cmap='gray')
plt.title("Adaptive Thresholding")
plt.axis('off')

# Otsu's Method
plt.subplot(2, 2, 4)
plt.imshow(otsu_thresholded, cmap='gray')
plt.title("Otsu's Method")
plt.axis('off')

# Show the plot
plt.tight_layout()
plt.show()
~~~



## Output

### Original Image
<img width="713" height="281" alt="image" src="https://github.com/user-attachments/assets/fa3ba62b-3e26-4907-a633-bb8fc8c25a03" />


### Global Thresholding
<img width="323" height="283" alt="image" src="https://github.com/user-attachments/assets/82ddeef3-06f5-4cdb-b874-4e07ab6cfb81" />


### Adaptive Thresholding
<img width="330" height="301" alt="image" src="https://github.com/user-attachments/assets/258aef3d-4a5f-4b4e-a173-59071af9e0af" />


### Optimum Global Thesholding using Otsu's Method
<img width="276" height="297" alt="image" src="https://github.com/user-attachments/assets/931a8ffe-7e95-439b-82c8-ee8ff2497bf8" />



## Result
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.
