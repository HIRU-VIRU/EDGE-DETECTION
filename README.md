# EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

## Program:
### ORIGINAL IMAGE
```
NAME : DHANUSH P
REG NO : 212223230042



import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('Shanks.jpeg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
### SOBEL EDGE DETECTOR
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5) 
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
### LAPLACIAN EDGE DETECTOR
```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
### CANNY EDGE DETECTOR
```
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')  
```
## Output:
### ORIGINAL IMAGE
<img width="413" height="531" alt="image" src="https://github.com/user-attachments/assets/ee59408d-c6f1-411a-abf3-0e89988a89d6" />


### SOBEL EDGE DETECTOR
<img width="413" height="531" alt="image" src="https://github.com/user-attachments/assets/0a9e4a23-09b5-436e-82fe-603211a0c72d" />


### LAPLACIAN EDGE DETECTOR
<img width="413" height="531" alt="image" src="https://github.com/user-attachments/assets/10637892-c520-4c03-ba2d-c9ee95a18ad1" />


### CANNY EDGE DETECTOR
<img width="413" height="531" alt="image" src="https://github.com/user-attachments/assets/26b6bd2d-edcb-4994-af49-f153d130ab40" />


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
