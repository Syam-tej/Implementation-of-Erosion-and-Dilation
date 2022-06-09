# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
## Step1:
Import the necessary packages to do Erosion and Dilution.

## Step2:
Create the text image of our name using putText from cv2 package.

## Step3:
Create the required structural element.

## Step4:
Apply Erode and Dilution for our NameImage.

## Step5:
Display the output images.

## step6:
End the programm
 
## Program:
Developed by:SYAM TEJ

Register number:212221240056
``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
image= np.zeros((100,400),dtype='uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image,' challa sandeep',(5,70), font,2,(255),5,cv2.LINE_AA)
cv2.imshow("Name",image)

# Create the structuring element
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))

# Erode the image
erodeImage = cv2.erode(image,kernel1)
cv2.imshow("Erode Image",erodeImage)

# Dilate the image
dilationImage = cv2.dilate(image,kernel1)
cv2.imshow("Dilated Image",dilationImage)



cv2.waitKey(0)
cv2.DestroyAllWindows

```
## Output:

### Display the input Image
![10 1](https://user-images.githubusercontent.com/93427224/172760847-9d5f63a7-7be3-41e4-8d05-5c8f9879399a.png)


### Display the Eroded Image
![10 2](https://user-images.githubusercontent.com/93427224/172760855-7aca2af8-fdfd-4fb8-aa3b-380780ebfe5f.png)


### Display the Dilated Image
![10 3](https://user-images.githubusercontent.com/93427224/172760870-c18ce9d4-4ebe-47a2-b93a-ab56d62e9004.png)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
