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
NAME: DEVADARSHAN A S
REG.No: 212222110007
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
font=cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,'PERFORMANCE ENGINEER',(4,70), font,1,(255),5,cv2.LINE_AA)
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
![Screenshot 2024-04-23 104823](https://github.com/DEVADARSHAN2/OPENING--AND-CLOSING/assets/119432150/f856984f-880e-4f89-8b73-db3a4c416705)
### Display the result of Opening
![Screenshot 2024-04-23 104829](https://github.com/DEVADARSHAN2/OPENING--AND-CLOSING/assets/119432150/da14911b-22e9-4292-8885-319c3eb86060)
### Display the result of Closing
![Screenshot 2024-04-23 104837](https://github.com/DEVADARSHAN2/OPENING--AND-CLOSING/assets/119432150/6dc080da-1fb1-4b55-b870-d45326209c4b)
## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
