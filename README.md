# EDGEDETECTION

## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the required packages for further process.

### Step2:
Read the image and convert the rgb image to gray scale image.

### Step3:
Use filters for smoothing the image to reduce the noise.

### Step4:
Apply the respective filters - Sobel, Laplacian edge detector and Canny edge detector.

### Step5:
Display the filtered image using plot and imshow.
 
## Program:

```
Developed by: RASIKA.M
register number:212222230117
```

# Import the packages
```
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("starbucks.jpeg")
gray_image = cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
new_image = cv2.GaussianBlur(gray_image,(3,3),0)
```

# SOBEL EDGE DETECTOR:

### SOBEL X:
```
sobelx = cv2.Sobel(new_image,cv2.CV_64F,1,0,ksize = 5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'RdPu')
plt.title('RdPu')
plt.subplot(1,2,2)
plt.imshow(sobelx,cmap = 'RdPu')
plt.title("Sobel X")
plt.xticks([])
plt.yticks([])
plt.show()
```
### SOBEL Y:
```
sobely = cv2.Sobel(new_image,cv2.CV_64F,0,1,ksize = 5)
plt.figure(figsize = (8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'OrRd')
plt.title('OrRd')
plt.subplot(1,2,2)
plt.imshow(sobely,cmap = 'OrRd')
plt.title("Sobel Y")
plt.xticks([])
plt.yticks([])
plt.show()
```
### SOBEL XY:
```
sobelxy = cv2.Sobel(new_image,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize = (8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'BuPu')
plt.title('BuPu')
plt.subplot(1,2,2)
plt.imshow(sobelxy,cmap = 'BuPu')
plt.title('Sobel XY')
plt.xticks([])
plt.yticks([])
plt.show()
```

# LAPLACIAN EDGE DETECTOR
```
laplacian = cv2.Laplacian(new_image,cv2.CV_64F)
plt.figure(figsize = (8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'bone')
plt.title('bone')
plt.subplot(1,2,2)
plt.imshow(laplacian,cmap = 'bone')
plt.title('Laplacian')
plt.xticks([])
plt.yticks([])
plt.show()
```


# CANNY EDGE DETECTOR
```canny_edge = cv2.Canny(new_image,120,150)
plt.figure(figsize = (8,8))
plt.subplot(1,2,1)
plt.imshow(new_image,cmap = 'gist_gray')
plt.title('gist_gray')
plt.subplot(1,2,2)
plt.imshow(canny_edge,cmap = 'gist_gray')
plt.title('Canny Edges')
plt.xticks([])
plt.yticks([])
plt.show()
```
## Output:
### SOBEL EDGE DETECTOR
## SOBEL X:
![Screenshot from 2023-10-23 16-38-17](https://github.com/rasika1206/EDGEDETECTION/assets/124434806/01bce1be-26fb-4282-948f-fcaaaf443472)


## SOBEL Y:
![Screenshot from 2023-10-23 16-38-22](https://github.com/rasika1206/EDGEDETECTION/assets/124434806/6e61a793-1be8-4f55-8c97-628fcac538b3)

## SOBEL XY:
![Screenshot from 2023-10-23 16-38-28](https://github.com/rasika1206/EDGEDETECTION/assets/124434806/4b8556a5-8ede-4b99-b8e6-4e7ddb9bd492)



### LAPLACIAN EDGE DETECTOR
![Screenshot from 2023-10-23 16-38-35](https://github.com/rasika1206/EDGEDETECTION/assets/124434806/d3786746-cfee-47bc-b78d-cadfbc192e6d)



<br>
<br>
<br>
<br>
<br>
<br>


### CANNY EDGE DETECTOR


![Screenshot from 2023-10-23 16-38-41](https://github.com/rasika1206/EDGEDETECTION/assets/124434806/ef096193-b9d3-413a-a52b-8a23e40a94be)

<br>
<br>
<br>
<br>
<br>

<br>

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
