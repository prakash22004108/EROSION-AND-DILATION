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
Developed by:PRAKASH R
Register Number:212222240074
```
### Import the necessary packages
``` Python
import cv2
import numpy as np
```
### Create the Text using cv2.putText
```python

img1 = np.zeros((100, 400), dtype="uint8")
font = cv2.FONT_HERSHEY_PLAIN
cv2.putText(img1, "PRAKASH R", (5, 70), font, 2, 255, 5, cv2.LINE_AA)
cv2.imshow("Prakash output", img1)
cv2.waitKey(0)

```
### Create the structuring element
```python
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```


### Erode the image
```python
cv2.erode(img1, kernel)
image_erode = cv2.erode(img1,kernel1)
cv2.imshow("Erode image",image_erode)
cv2.waitKey(0)
```
### Dilate the image
```python
image_dilatel=cv2.dilate(img1,kernel1)
cv2.imshow("Dilate image",image_dilatel)
cv2.waitKey(0)
```
## Output:

### Display the input Image

![01](https://github.com/prakash22004108/EROSION-AND-DILATION/assets/113497032/74c88d10-7b37-49e5-8da8-912c88893e1c)


### Display the Eroded Image

![02](https://github.com/prakash22004108/EROSION-AND-DILATION/assets/113497032/040c7652-1f05-4a73-9bfc-955ecefe00bf)


### Display the Dilated Image

![03](https://github.com/prakash22004108/EROSION-AND-DILATION/assets/113497032/0a5b76a4-25ba-432e-9b76-9cbf7d5062de)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
