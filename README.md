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

## Program:
### NAME: SAKTHIVEL R
### REG.NO:212222100044

## Convert image to grayscale and remove noise
```python
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("dog.jpeg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)

```
## Sobel edge detection:
### Sobel x axis:
```python
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
### Sobel y axis:
```python
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
### Sobel xy axis:
```python
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
## LAPLACIAN EDGE DETECTOR:

```python
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

## CANNY EDGE DETECTOR:

```python
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
# Output:
## Sobel edge detection:
### Sobel x axis:
![image](https://github.com/Gokul0117/EDGE-DETECTION/assets/121165938/92fcd997-995d-4494-ba92-c4a6bff9a035)


### Sobel y axis:
![Screenshot 2024-04-02 114640](https://github.com/Gokul0117/EDGE-DETECTION/assets/121165938/87ea9bfd-da26-4fd0-a01e-d05e373fe59d)


### Sobel xy axis:

![Screenshot 2024-04-02 114650](https://github.com/Gokul0117/EDGE-DETECTION/assets/121165938/86b28369-af22-4f89-93d9-0bfcaff6437e)


## Lapacian Detector:

![Screenshot 2024-04-02 114658](https://github.com/Gokul0117/EDGE-DETECTION/assets/121165938/a2dd2b3f-f06a-4164-8c9b-188f0264fb24)

## Cany edge detector:
![Screenshot 2024-04-02 114709](https://github.com/Gokul0117/EDGE-DETECTION/assets/121165938/a6eb85fb-c53b-4565-b56c-5d94a882a3a5)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
