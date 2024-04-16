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

## Program :
### Developed By : MANOGARAN S
### Reg No : 212223240081
```
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("duck.jpeg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
## Sobel X axis
```
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
## Sobel Y axis
```
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
## Sobel XY axis
```
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
## Laplacian Edge Detector
```
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
## Canny Edge Detector
```
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
## Sobel X axis
![Screenshot 2024-04-16 232411](https://github.com/manogarans/EDGE-DETECTION/assets/139331782/40aa66f0-aff1-4f6f-939b-9366d6fb066f)

## Sobel Y axis
 ![Screenshot 2024-04-16 232416](https://github.com/manogarans/EDGE-DETECTION/assets/139331782/11306113-dbe9-45a8-b978-b5f4d0c15a0f)

## Sobel XY axis
![Screenshot 2024-04-16 232423](https://github.com/manogarans/EDGE-DETECTION/assets/139331782/b72c2ccc-702a-4073-adfc-4cb672ceb092)


### LAPLACIAN EDGE DETECTOR
![Screenshot 2024-04-16 232428](https://github.com/manogarans/EDGE-DETECTION/assets/139331782/a7a6087b-9336-432d-af6c-6b8dec455e90)


### CANNY EDGE DETECTOR
![Screenshot 2024-04-16 232433](https://github.com/manogarans/EDGE-DETECTION/assets/139331782/8f744102-7534-4bcd-b265-26d22dc5a4ef)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
