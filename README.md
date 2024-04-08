# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
</br>
Import the required libraries.
</br> 

### Step2
</br>
Convert the image from BGR to RGB.
</br> 

### Step3
</br>
Apply the required filters for the image separately.
</br> 

### Step4
</br>
Plot the original and filtered image by using matplotlib.pyplot.
</br> 

### Step5
</br>
End the program.
</br> 

## Program:
### Developed By   : KANCHARLA NARMADHA
### Register Number:212222110016
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("moon.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/169
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Average Filter Image")
plt.axis("off")
plt.show()
```
ii) Using Weighted Averaging Filter
```
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()
```
iii) Using Gaussian Filter
```
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()
```

iv) Using Median Filter
```
median=cv2.medianBlur(image2,13)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Median Blur")
plt.axis("off")
plt.show()
```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()
```
ii) Using Laplacian Operator
```
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()
```

## OUTPUT:
### 1. Smoothing Filters

i) Using Averaging Filter

![image](https://github.com/kancharlaNarmadha/Implementation-of-filter/assets/119559316/49b55e39-a52a-4735-b4e9-eea424b6cd3e)



ii) Using Weighted Averaging Filter

![image](https://github.com/kancharlaNarmadha/Implementation-of-filter/assets/119559316/b03e51a7-6664-4a07-a5e0-37fae026fb4f)



iii) Using Gaussian Filter

![image](https://github.com/kancharlaNarmadha/Implementation-of-filter/assets/119559316/8fe8db59-236b-4e0f-b764-fd49aaff7ea0)



iv) Using Median Filter
![image](https://github.com/kancharlaNarmadha/Implementation-of-filter/assets/119559316/a5601b2f-2840-4763-aa78-4014737515bf)



### 2. Sharpening Filters

i) Using Laplacian Kernal

![image](https://github.com/kancharlaNarmadha/Implementation-of-filter/assets/119559316/9d4a1e94-f76d-4662-b033-b411acc0780d)



ii) Using Laplacian Operator

![image](https://github.com/kancharlaNarmadha/Implementation-of-filter/assets/119559316/82a1b005-d456-48f4-ab59-e471df23db84)




## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
