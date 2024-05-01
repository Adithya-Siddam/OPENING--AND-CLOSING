# EX 10 OPENING AND CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
- Step1: Import the necessary packages
- Step2: Give the input text using cv2.putText()
- Step3: Perform opening operation and display the result
- Step4: Similarly, perform closing operation and display the result
## Program:
```
NAME: S Adithya Chowdary
REG.No: 212221230100
``` 
# Import the necessary packages
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
```
# Create the Text using cv2.putText
```python
img1=np.zeros((100,400), dtype='uint8')
font=cv2.FONT_HERSHEY_TRIPLEX
cv2.putText(img1,'PROMPT ENGINEER',(4,70), font,1,(255),5,cv2.LINE_AA)

```
# Create the structuring element
```python
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```
# Use Opening operation
```python
image1=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel)
plt.imshow(image1)
plt.axis("off")
```
# Use Closing Operation
```python
image2=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel)
plt.imshow(image2)
plt.axis("off")
```
## Output:
### Display the input Image
![image](https://github.com/Adithya-Siddam/OPENING--AND-CLOSING/assets/93427248/2a723be2-a63c-4243-b50a-94ca106ecef3)
### Display the result of Opening
![image](https://github.com/Adithya-Siddam/OPENING--AND-CLOSING/assets/93427248/94d05263-2015-4d2e-b2f0-57de028ea925)
### Display the result of Closing
![image](https://github.com/Adithya-Siddam/OPENING--AND-CLOSING/assets/93427248/b0867344-e9fa-46fa-b17c-6b090687155b)
## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
