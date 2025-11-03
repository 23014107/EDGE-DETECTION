# EDGE-DETECTION

NAME : RAMYA.P

REG NO : 212223240137

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
NAME : RAMYA.P
REG NO : 212223240137
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('/content/ramya photo.jpg')
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
A<img width="268" height="338" alt="image" src="https://github.com/user-attachments/assets/b589ee1b-a208-49f9-b09b-2c681e78f82d" />



### SOBEL EDGE DETECTOR
<img width="257" height="335" alt="image" src="https://github.com/user-attachments/assets/fe4ae4fe-25f9-4067-ade8-33b735d246cf" />



### LAPLACIAN EDGE DETECTOR
<img width="268" height="331" alt="image" src="https://github.com/user-attachments/assets/1c46d4c1-5dea-46cd-a0e8-f6d1fbebae3c" />



### CANNY EDGE DETECTOR
<img width="256" height="335" alt="image" src="https://github.com/user-attachments/assets/2a2ea694-6a23-443a-bb5d-f6b0ab8220bc" />



## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
