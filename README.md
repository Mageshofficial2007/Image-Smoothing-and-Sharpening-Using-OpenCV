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

```python

```








### Result:
Thus, smoothing filters and sharpening filters are successfully implemented using OpenCV.
The smoothing filters reduce noise and improve image quality, while sharpening filters enhance edges and details for better feature extraction.
