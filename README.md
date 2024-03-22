# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()
### Step2:
Print the image using imshow().
### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.
### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.
### Step5:
The Histogram of gray scale image and color image is shown.

## Program:
```python
# Developed By: Evangelin.S
# Register Number:212221230025

import cv2
import matplotlib.pyplot as plt

# Write your code to find the histogram of gray scale image and color image channels.
gray_image = cv2.imread("image.jpg")
color_image = cv2.imread("image1.jpg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows() 

# Display the histogram of gray scale image and any one channel histogram from color image
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("images.jfif")
color_image = cv2.imread("image1.jpg")
gray_hist = cv2.calcHist([gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
plt.imshow(color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()

# Write the code to perform histogram equalization of the image. 
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("images.jfif",0)
cv2.imshow("Gray Image",gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows
```
## Output:
### Input Grayscale Image and Color Image
![image](https://github.com/Evangelin-Ruth/Histogram-of-an-images/assets/94219798/64940f64-15ec-4c84-9b3a-178eb96ad828)

### Histogram of Grayscale Image and any channel of Color Image
![image](https://github.com/Evangelin-Ruth/Histogram-of-an-images/assets/94219798/3142375d-d0c0-4604-8c39-c8b1c9be80dc)
![image](https://github.com/Evangelin-Ruth/Histogram-of-an-images/assets/94219798/0c9ff9fb-c098-48d4-96b2-a4e8dab78620)
![image](https://github.com/Evangelin-Ruth/Histogram-of-an-images/assets/94219798/6e5df2ba-f187-49ca-b5f5-83b4261c289d)
![image](https://github.com/Evangelin-Ruth/Histogram-of-an-images/assets/94219798/fc9aa41b-7035-429f-86f2-9b74fa7653d1)

### Histogram Equalization of Grayscale Image.
![image](https://github.com/Evangelin-Ruth/Histogram-of-an-images/assets/94219798/8d7fe19b-f170-4240-aba2-a92d5a719fae)

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
