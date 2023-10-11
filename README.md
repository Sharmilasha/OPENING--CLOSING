# OPENING--CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.


### Step2:
Create the Text using cv2.putText.

### Step3:
Create the structuring element.

### Step4:
Use Opening operation.

### Step5:
Use Closing Operation.

 
## Program:
```

# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt 

# Create the Text using cv2.putText
image = np.zeros((100,250),dtype = 'uint8')
img=cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(img,"SHARMILA",(5,70),font,2,(204,0,102),5,cv2.LINE_AA)
plt.title("Original Image")
plt.imshow(img,'magma')
plt.axis('off')

# Create the structuring element
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))

# Use Opening operation
opening_image = cv2.morphologyEx(img,cv2.MORPH_OPEN,kernel)
plt.title("Opening")
plt.imshow(opening_image,'magma')
plt.axis('off')

# Use Closing Operation
closing_image = cv2.morphologyEx(img,cv2.MORPH_CLOSE,kernel)
plt.title("Closing")
plt.imshow(closing_image,'magma')
plt.axis('off')
```
## Output:

### Display the input Image

![J1](https://github.com/Sharmilasha/OPENING--CLOSING/assets/94506182/3e9e79d2-912a-44d5-bf59-822dc26cd24c)


### Display the result of Opening
![J2](https://github.com/Sharmilasha/OPENING--CLOSING/assets/94506182/73a5ec00-4b74-4c7a-8355-b43df2d44e26)

### Display the result of Closing

![J4](https://github.com/Sharmilasha/OPENING--CLOSING/assets/94506182/d28cef8d-17c2-4cf7-9159-214df92e4de8)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
