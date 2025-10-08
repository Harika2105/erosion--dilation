# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import required libraries (OpenCV, NumPy) and load the image in grayscale


### Step2:
Define a structuring element (kernel) for morphological operations.

### Step3:
Apply erosion using cv2.erode() on the image with the defined kernel.

### Step4:
Apply dilation using cv2.dilate() on the image with the same kernel.

### Step5:
Display and compare the original, eroded, and dilated images.

 
## Program:
## Developed by: S.Harika
## Reg NO: 212224240155

```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
```
image = np.zeros((500, 500, 3), dtype=np.uint8)
```
```
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'HARIKA', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
```
```
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')
```
```
kernel = np.ones((3, 3), np.uint8)
eroded_image = cv2.erode(image, kernel, iterations=1)
```
```
plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))
plt.title("Eroded Image")
plt.axis('off')
```
```
dilated_image = cv2.dilate(image, kernel, iterations=1)
```
```
plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB)) 
plt.title("Dilated Image")
plt.axis('off')
```
## Output:

### Display the input Image
<img width="463" height="474" alt="Screenshot 2025-10-08 225124" src="https://github.com/user-attachments/assets/5c546646-e714-43a6-bb49-7c3cbf07d6bb" />

### Display the Eroded Image
<img width="461" height="474" alt="Screenshot 2025-10-08 225205" src="https://github.com/user-attachments/assets/da175237-b36c-48a7-b193-ce4bf8634041" />

### Display the Dilated Image
<img width="445" height="463" alt="Screenshot 2025-10-08 225241" src="https://github.com/user-attachments/assets/5446b42c-f3d5-40f4-a6f1-b7c9df4b32ce" />


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
