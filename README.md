# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import necessary packages

### Step2:
Create an empty window and add text to it

### Step3:
create a structuring element

### Step4:
Do the operation

### Step5:
Print the output images

 
## Program:


#### Import the necessary packages
``` Python
import numpy as np
import cv2
import matplotlib.pyplot as plt
```

#### Create the Text using cv2.putText
```py
img = np.zeros((100,400),dtype = 'uint8')
img = cv2.imread("west.jpg")
plt.imshow(img)
plt.axis('off')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img ,' ',(5,60),font,2,(255),5,cv2.LINE_AA)
```


#### Create the structuring element
```py
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
cv2.erode(img,kernel)
```


#### Erode the image
```py

img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')
```


#### Dilate the image
```py
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')




```
## Output:

#### Display the input Image
<br>
<br>
<br>

![f6499fae-af08-40e0-843f-ba9edf1331ee](https://github.com/swedha333/erosion-dilation/assets/121490575/da6c0d82-2e76-444f-a626-8bf40eacf7e3)

<br>
<br>
<br>

#### Display the Eroded Image
<br>
<br>
<br>

![93538a17-0e56-45c8-9048-fb8b9d7675c6](https://github.com/swedha333/erosion-dilation/assets/121490575/0dbf85a6-3958-4952-9474-9e4ccad45fd2)

<br>
<br>
<br>

#### Display the Dilated Image
<br>
<br>
<br>

![image](https://github.com/swedha333/erosion-dilation/assets/121490575/a2475492-5736-4c4f-ba35-2ca41394d152)


<br>
<br>
<br>

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
