# EROSION-AND-DILATION

## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary libraries (OpenCV and NumPy).
<br>


### Step2:
Use cv2.putText to add the text to the img1 image at specific coordinates.
<br>

### Step3:
Define two kernels (kernel and kernel1) for morphological operations.
<br>

### Step4:
Display the eroded image using cv2.imshow.
<br>

### Step5:
Use cv2.waitKey(0) to wait for a key press indefinitely.
<br>

 
## Program:
```
DEVELOPED BY:GURUMOORTHI R
REG NO:212222230042
```
``` 
# Import the necessary packages


import cv2
import numpy as np



# Create the Text using cv2.putText

img1=np.zeros((100,400),dtype="uint8")
font=cv2.FONT_HERSHEY_PLAIN
cv2.putText(img1,"GURUMOORTHI R",(5,70),font,2,(255),5,cv2.LINE_AA)
cv2.imshow("image",img1)
cv2.waitKey(0)

# Create the structuring element

kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))


# Erode the image

cv2.erode(img1, kernel)
image_erode = cv2.erode(img1,kernel1)
cv2.imshow("GURUMOORTHI R-212222230042",image_erode)
cv2.waitKey(0)



# Dilate the image

image_dilatel=cv2.dilate(img1,kernel1)
cv2.imshow("GURUMOORTHI R-212222230042",image_dilatel)
cv2.waitKey(0)



```
## Output:

### Display the input Image

![1](https://github.com/gururamu08/EROSION-AND-DILATION/assets/118707009/38cdcc12-af16-4a27-b90a-f91ca55b691a)



<br>

### Display the Eroded Image

![2](https://github.com/gururamu08/EROSION-AND-DILATION/assets/118707009/e1b9daae-7d3e-461a-8e9a-3c7c4ff2070c)



<br>

### Display the Dilated Image

![3](https://github.com/gururamu08/EROSION-AND-DILATION/assets/118707009/cbdfb956-4412-4032-9d5f-12d2c6b3b2db)



<br>

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
