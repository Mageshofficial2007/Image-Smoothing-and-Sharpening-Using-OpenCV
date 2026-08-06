# Image-Smoothing-and-Sharpening-Using-OpenCV
## Aim
To write a Python program using OpenCV to apply different smoothing filters (Averaging, Weighted Averaging, Gaussian, Median) and sharpening filters (Laplacian Kernel and Laplacian Operator) for image enhancement, and display each result separately along with the original image for comparison.

## The program performs the following operations:
1.	Read and display an input image
2.	Apply Averaging filter
3.	Apply Weighted Averaging filter
4.	Apply Gaussian filter
5.	Apply Median filter
6.	Apply Laplacian sharpening using kernel
7.	Apply Laplacian operator
8.	Display all outputs for comparison

## Software Used
1.	Anaconda – Python 3.7
2.	Jupyter Notebook / VS Code
3.	OpenCV (cv2)
4.	NumPy
5.	Matplotlib
6.	Algorithm

## developed by : MAGESH BOOPATHI.M
## register no : 212224230145

### Step 1:
Import the required libraries: OpenCV, NumPy, and Matplotlib.

### Step 2:
Read the input image (e.g., image.jpg).

### Step 3:
Convert the image from BGR to RGB format for display.

### Step 4:
Apply Averaging Filter using cv2.blur().

### Step 5:
Apply Weighted Averaging Filter using a custom kernel with cv2.filter2D().

### Step 6:
Apply Gaussian Filter using cv2.GaussianBlur().

### Step 7:
Apply Median Filter using cv2.medianBlur().

### Step 8:
Apply Laplacian Sharpening using Kernel with cv2.filter2D().

### Step 9:
Convert image to grayscale and apply Laplacian Operator using cv2.Laplacian().

### Step 10:
Display all filtered images using a grid layout for comparison.

## programm:
#### 1. Smoothing Filters i) Using Averaging Filter
```python

import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("girl.jpg")
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
### output
<img width="1193" height="513" alt="Screenshot 2026-08-06 091447" src="https://github.com/user-attachments/assets/8896369c-2727-4d96-8019-40ab277865f9" />

#### ii) Using Weighted Averaging Filter
```python
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()
```
### output
<img width="622" height="588" alt="Screenshot 2026-08-06 091658" src="https://github.com/user-attachments/assets/6ef9b2ab-734f-4072-8249-2ccf17d9dede" />

#### iii) Using Gaussian Filter
```python
gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()
```
### output
<img width="601" height="583" alt="Screenshot 2026-08-06 091716" src="https://github.com/user-attachments/assets/bb3f258e-9dfa-4d55-9cf2-fd6d9a979af0" />

#### iv) Using Median Filter
```python
import cv2
import matplotlib.pyplot as plt

# Read the original image
image2 = cv2.imread("girl.jpg")

# Check if the image is loaded
if image2 is None:
    print("Error: girl.jpg not found!")
else:
    # Apply Median Blur
    median = cv2.medianBlur(image2, 13)

    # Display Original and Median Blur
    plt.figure(figsize=(10,5))

    plt.subplot(1,2,1)
    plt.imshow(cv2.cvtColor(image2, cv2.COLOR_BGR2RGB))
    plt.title("Original Image")
    plt.axis("off")

    plt.subplot(1,2,2)
    plt.imshow(cv2.cvtColor(median, cv2.COLOR_BGR2RGB))
    plt.title("Median Blur")
    plt.axis("off")

    plt.show()
```
### output
<img width="1146" height="556" alt="Screenshot 2026-08-06 091733" src="https://github.com/user-attachments/assets/23544343-065b-42ce-b84d-7026857e192a" />

#### 2. Sharpening Filters i) Using Laplacian Linear Kernal
```python
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()
```
### output
<img width="615" height="587" alt="Screenshot 2026-08-06 091942" src="https://github.com/user-attachments/assets/324af783-45b1-4e16-b92a-9241fe61363a" />

#### ii) Using Laplacian Operator
```python
laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()
```
### output
<img width="1484" height="601" alt="Screenshot 2026-08-06 093259" src="https://github.com/user-attachments/assets/fa8ac58b-0b03-4046-810a-8ce9bf828b88" />


### Result:
Thus, smoothing filters and sharpening filters are successfully implemented using OpenCV.
The smoothing filters reduce noise and improve image quality, while sharpening filters enhance edges and details for better feature extraction.
