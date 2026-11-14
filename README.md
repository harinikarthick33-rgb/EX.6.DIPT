# EXP-6: Edge-detection-opencv
# NAME: Harini V K
# REGISTER NO: 212225220036
# Aim
To perform edge detection using Sobel, Roberts, Prewitt, Laplacian, and Canny edge detectors.

# Software Required
Anaconda – Python 3.7
Jupyter Notebook / VS Code
OpenCV (cv2)
NumPy
Matplotlib

# Algorithm
# Step 1:
Import all the necessary modules for the program.

# Step 2:
Load an image using cv2.imread().

# Step 3:
Convert the image to grayscale.

# Step 4:
Apply Sobel operator using OpenCV to detect edges.

# Step 5:
Apply Prewitt operator using custom kernels.

# Step 6:
Apply Roberts operator using custom kernels.

# Step 7:
Apply Laplacian operator using OpenCV.

# Step 8:
Apply Canny edge detector using OpenCV.

# Step 9:
Display all edge-detected images for comparison.

# Program
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('Harini.new.jpeg')  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
# Original Image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')
```
# Output
<img width="636" height="455" alt="image" src="https://github.com/user-attachments/assets/892e93ed-7f0d-4fab-a7ee-47249c8d15f4" />

<img width="647" height="433" alt="image" src="https://github.com/user-attachments/assets/c0628102-4599-4099-bd5b-1345b7d31745" />

<img width="657" height="452" alt="image" src="https://github.com/user-attachments/assets/9d2517ef-dd5e-4f17-93af-f37403b3c531" />

<img width="627" height="447" alt="image" src="https://github.com/user-attachments/assets/14d95d77-2043-4aac-b6ae-1b9e60cda79b" />




