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

## PROGRAM & OUTPUT:
```
DEVELOPED BY: HYCINTH D
REGISTER NO:212223240055
```
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Load the image
image = cv2.imread('d.jpg')  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
# Original Image
plt.figure(figsize=(7,3))
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
![Screenshot 2024-10-05 084725](https://github.com/user-attachments/assets/d17ca973-d858-41f8-9d47-1e74f26dd53b)

### SOBEL EDGE DETECTOR
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
plt.figure(figsize=(7,3))
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
![Screenshot 2024-10-05 084738](https://github.com/user-attachments/assets/37cda12c-f0c0-4b25-b873-37e3d17065b8)

### LAPLACIAN EDGE DETECTOR
```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.figure(figsize=(7,3))
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
![Screenshot 2024-10-05 084952](https://github.com/user-attachments/assets/b73d583c-1d31-49a8-b1aa-b0584c7ae5ae)

### CANNY EDGE DETECTOR
```
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.figure(figsize=(7,3))
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')
```
![Screenshot 2024-10-05 085000](https://github.com/user-attachments/assets/f2bce8d3-76b5-49b4-ad1c-2eea4600c358)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
