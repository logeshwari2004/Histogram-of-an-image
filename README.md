# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the libraries.

### Step2:
Use cv2.calcHist to find the histogram of the image.

### Step3:
Plot the image and its stem plots using the functions.

### Step4:
Equalize the grayscale image using the in-built function cv2.equalizeHist().

### Step5:
Display the original and equalized image.

## Program:
```python
# Developed By:LOGESHWARI.P
# Register Number:212221230055

# Write your code to find the histogram of gray scale image and color image channels.
import cv2
import matplotlib.pyplot as plt
Gray_image = cv2.imread("image.jpg")
Color_image = cv2.imread("horse.jpg",-1)
cv2.imshow("Gray Image",Gray_image)
cv2.imshow("Colour Image",Color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()

# Display the histogram of gray scale image and any one channel histogram from color image
import numpy as np
import matplotlib.pyplot as plt
gray_hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([Color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(Gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
cv2.destroyAllWindows()

# Write the code to perform histogram equalization of the image. 
import cv2
gray_image = cv2.imread("image.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows 

```
## Output:
### Input Grayscale Image and Color Image
![DIP4A](https://user-images.githubusercontent.com/94211349/230021918-fbee49ba-0815-44bb-92ff-9b04741e84ef.png)

### Histogram of Grayscale Image and any channel of Color Image
![DIP4B](https://user-images.githubusercontent.com/94211349/230021981-19cf3346-a60f-4a01-b6b7-13577c542ac5.png)

![DIP4C](https://user-images.githubusercontent.com/94211349/230022029-61e388a1-0d15-4280-94e9-ffee29cd8ecf.png)


### Histogram Equalization of Grayscale Image
![DIP4D](https://user-images.githubusercontent.com/94211349/230022076-f4bf8f27-9952-450b-8ab8-74ac948c7a9c.png)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
