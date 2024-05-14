# EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

## PROGRAM :
### DEVELOPED BY : Karnan K
### REGISTER NO : 212222230062
### Convert image to grayscale and remove noise
```P
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("cat.jpeg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
### SOBEL EDGE DETECTOR
**SOBEL X AXIS :**
```p
sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelx)
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
**SOBEL Y AXIS :**
```p
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobely)
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
**SOBEL XY AXIS :**
```p
sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelxy)
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```
### LAPLACIAN EDGE DETECTOR
```p
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(lap)
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```
### CANNY EDGE DETECTOR
```p
canny=cv2.Canny(gray,120,150)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(canny)
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```

## Output:
### SOBEL EDGE DETECTOR


### SOBEL X AXIS :
![1](https://github.com/IamShakthi/EDGE-DETECTION/assets/117913445/caff429f-d2c7-435c-a9bc-2aa684506114)





### SOBEL Y AXIS :

![2](https://github.com/IamShakthi/EDGE-DETECTION/assets/117913445/cbfcfc0b-b68e-470b-8ec1-ff0e39eabfa8)



### SOBEL XY AXIS :

![3](https://github.com/IamShakthi/EDGE-DETECTION/assets/117913445/c1919680-18ed-47f7-9ea8-6e1c614d59f5)



### LAPLACIAN EDGE DETECTOR :

![4](https://github.com/IamShakthi/EDGE-DETECTION/assets/117913445/38f15bf9-0de6-4624-84d0-ab9934908883)



### CANNY EDGE DETECTOR :

![5](https://github.com/IamShakthi/EDGE-DETECTION/assets/117913445/ce080b28-13ea-47af-8f2f-42fdc9c4bbdf)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
