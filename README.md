# Implementation-of-Filters
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary modules.

### Step2:
For performing smoothing operation on a image.
* Average filter
```python
kernel=np.ones((11,11),np.float32)/121
image3=cv2.filter2D(image2,-1,kernel)
```
* Weighted average filter
```python
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
```
* Gaussian Blur
```python
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
```
* Median filter
```python
median=cv2.medianBlur(image2,13)
```

### Step3
For performing sharpening on a image.
* Laplacian Kernel
```python
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
```
* Laplacian Operator
```python
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
```

### Step4
Display all the images with their respective filters.


## Program:
```python
# Developed By   : Aditya JV
# Register Number: 212220230002
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("pos.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
```

### 1. Smoothing Filters

i) Using Averaging Filter
```Python
kernel=np.ones((11,11),np.float32)/121
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(8,8))
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
```Python
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.figure(figsize=(8,8))
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
```Python
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.figure(figsize=(8,8))
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
```Python
median=cv2.medianBlur(image2,13)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Median Blur")
plt.axis("off")
plt.show()


```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```Python
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.figure(figsize=(8,8))
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
```Python
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.figure(figsize=(8,8))
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
</br>
![Using Averaging Filter](https://user-images.githubusercontent.com/75235386/168429219-f60ef620-79b3-4b57-b143-597afe63469a.png)
</br>

ii) Using Weighted Averaging Filter
</br>
![Using Weighted Averaging Filter](https://user-images.githubusercontent.com/75235386/168429228-981607a7-68f1-476f-b0e4-02f51e0ad87d.png)
</br>

iii) Using Gaussian Filter
</br>
![Using Gaussian Filter](https://user-images.githubusercontent.com/75235386/168429233-ae856eae-de15-417d-9b7d-33b6564dcba8.png)
</br>

iv) Using Median Filter
</br>
![Using Median Filter](https://user-images.githubusercontent.com/75235386/168429240-3baabd25-934b-4016-907d-b93f60090e07.png)
</br>

### 2. Sharpening Filters

i) Using Laplacian Kernal
</br>
![Using Laplacian Kernal](https://user-images.githubusercontent.com/75235386/168429251-bb626757-79ad-421f-9269-242b51fa9d5c.png)
</br>

ii) Using Laplacian Operator
</br>
![Using Laplacian Operator](https://user-images.githubusercontent.com/75235386/168429257-c127a71e-256e-4def-80cb-b78f60028edd.png)
</br>

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
