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
``` Python
Developed by : SUROTHAAMAN R
Register Number : 212222103003
```
# Import the necessary packages
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
```
# Create the Text using cv2.putText
```python
img = np.zeros((100,400),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img ,'Django',(80,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')
```
# Create the structuring element
```python
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)
```
# Erode the image
```python
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')
```
# Dilate the image
```python
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')
```
## Output:

### Display the input Image
![image](https://github.com/surothaaman/erosion--dilation/assets/133313653/7c0beacc-00d0-4363-8f4c-72b83c864bad)



### Display the Eroded Image
![image](https://github.com/surothaaman/erosion--dilation/assets/133313653/53af27d6-b289-422e-969d-a6db48e3b5e5)




### Display the Dilated Image
![image](https://github.com/surothaaman/erosion--dilation/assets/133313653/02d31f58-d219-43fc-b3a4-f08b1486a94c)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
