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

# ORIGINAL:
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread("boy.jpg")
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')

```
# SOBEL EDGE DETECTOR:
```python
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5) 
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```

# LAPLACIAN EDGE DETECTOR:
```python
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```

# CANNY EDGE DETECTOR:
```python
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')  
```
## Output:
### SOBEL EDGE DETECTOR:

![image](https://github.com/user-attachments/assets/04b0c405-8709-4620-99f3-47d0c062d87c)


### LAPLACIAN EDGE DETECTOR:

![image](https://github.com/user-attachments/assets/d973d9e1-5fb6-4dc8-b12c-40907372dd76)



### CANNY EDGE DETECTOR:

![image](https://github.com/user-attachments/assets/6a841c9b-89ff-455e-9ff6-7c5deabaa564)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
