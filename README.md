# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:

### Step1:
<br> import the neccesary packages


### Step2:
<br> creat the text using cv2.put Text

### Step3:
<br> create the structuting element

### Step4:
<br>  Erodde the image

### Step5:
<br> Dilate the image

 
## Program:

``` Python
import cv2
import numpy as np
from matplotlib import pyplot as plt
imput_image='actor.jpg'
color_image=cv2.imread(imput_image)
gray_image=cv2.cvtColor(color_image,cv2.COLOR_BGR2GRAY)
edges=cv2.Canny(gray_image,100,200)
kernel_size=5
kernel=np.ones((kernel_size,kernel_size),np.uint8)
erosion=cv2.erode(edges,kernel,iterations=1)
dilation=cv2.dilate(edges,kernel,iterations=1)
plt.figure(figsize=(15,10))
plt.subplot(2,3,1)
plt.imshow(cv2.cvtColor(color_image,cv2.COLOR_BGR2RGB))
plt.title('Original Color Image')
plt.axis('on')
plt.subplot(2,3,2)
plt.imshow(gray_image,cmap='gray')
plt.title('black and white image')
plt.axis('on')
plt.subplot(2,3,3)
plt.imshow(edges,cmap='gray')
plt.title('edge segmentation')
plt.axis('on')
plt.subplot(2,3,4)
plt.imshow(edges,cmap='gray')
plt.title('erosion')
plt.axis('on')
plt.subplot(2,3,5)
plt.imshow(edges,cmap='gray')
plt.title('dilation')
plt.axis('on')




```
## Output:

![WhatsApp Image 2024-10-16 at 15 12 58_4a4170de](https://github.com/user-attachments/assets/405ff4d2-2ad2-45d6-b0c0-bea1b5a65a9c)
![WhatsApp Image 2024-10-16 at 15 12 59_e05ce6f9](https://github.com/user-attachments/assets/f3738921-834f-484e-b3bc-116d0bed23d8)

![WhatsApp Image 2024-10-16 at 15 12 59_04715077](https://github.com/user-attachments/assets/fd3f3679-437e-439a-8c56-9acd7cbfbb7f)







## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
