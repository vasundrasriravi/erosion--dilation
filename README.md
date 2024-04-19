# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary pacakages

### Step2:
Create the text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Erode the image

### Step5:
Dilate the Image

## Program:
```
NAME: VASUNDRA SRI R
REG.NO: 212222230168
```
# Import the necessary packages
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
```
# Create the Text using cv2.putText
```
img = np.zeros((100,400),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img ,'VASUNDRA',(5,60),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')
```
# Create the structuring element
```
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
cv2.erode(img,kernel)
```
# Erode the image
```
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')
```
# Dilate the image
```
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')

```
## Output:

### Display the input Image
![Screenshot 2024-04-19 115846](https://github.com/vasundrasriravi/erosion--dilation/assets/119393983/fe847b60-4657-4b2e-95e9-1105e632f8a3)

### Display the Eroded Image
![Screenshot 2024-04-19 115823](https://github.com/vasundrasriravi/erosion--dilation/assets/119393983/0cd1d943-ccf3-49b0-8d53-a99a57ba920a)

### Display the Dilated Image
![Screenshot 2024-04-19 115835](https://github.com/vasundrasriravi/erosion--dilation/assets/119393983/b7299de5-c982-4301-b6b5-ad52dd37d7b2)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
