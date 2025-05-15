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
### Name: HAREVASU S
### Register Number: 212223230069
``` Python
import numpy as np
import cv2
import matplotlib.pyplot as plt

def load_img():
    blank_img = np.zeros((300,700), dtype=np.uint8)
    front = cv2.FONT_HERSHEY_SIMPLEX
    cv2.putText(blank_img, text='HAREVASU', org=(50,200), fontFace=front, 
                fontScale=5, color=(255, 255, 255), thickness=25, lineType=cv2.LINE_AA)
    return blank_img

def display_img(img,title="Original Image"):
    fig=plt.figure(figsize=(10,8))
    ax=fig.add_subplot(111)
    ax.imshow(img,cmap='gray')
    ax.set_title(title, fontsize=16)
    plt.show()

img = load_img()
display_img(img)

kernal = np.ones((5,5),dtype=np.uint8)

img1 = cv2.erode(img,kernal,iterations = 2)
display_img(img1,"Eroded Image")

dilate = cv2.dilate(img,kernal,iterations = 3)
display_img(dilate,"Dilated Image")
```
## Output:
### Display the input Image
![image](https://github.com/user-attachments/assets/cf0d2a21-b959-4c9b-b2f2-8e3de2e70945)


### Display the Eroded Image
![image](https://github.com/user-attachments/assets/7d644075-1624-4d68-a065-f1eba22f46a2)

### Display the Dilated Image
![image](https://github.com/user-attachments/assets/60b26637-fc81-44d0-a6fe-7a4a0eb76993)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
