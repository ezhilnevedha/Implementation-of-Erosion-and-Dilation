# Implementation-of-Erosion-and-Dilation
### Name: Ezhil Nevedha K
### Reg no: 212223230055
### Date: 21/05/2026
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary pacakages

### Step2:
Create the text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Erode the image

### Step5:
Dilate the Image

 
## Program:

``` Python
# developed by :Ezhil Nevedha K
# Reg no : 212223230055

import cv2
import numpy as np
import matplotlib.pyplot as plt
# Create a blank image
image = np.zeros((500, 500, 3), dtype=np.uint8)
# Add text on the image using cv2.putText
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'Ezhil Nevedha K', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
# Display the input image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')
# Create a simple square kernel (3x3)
kernel = np.ones((3, 3), np.uint8)
# Apply erosion (shrinking effect)
eroded_image = cv2.erode(image, kernel, iterations=1)
# Display the eroded image
plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Eroded Image")
plt.axis('off')
# Apply dilation (expanding effect)
dilated_image = cv2.dilate(image, kernel, iterations=1)
# Display the dilated image
plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Dilated Image")
plt.axis('off')

```
## Output:

### Display the input Image
<img width="490" height="411" alt="image" src="https://github.com/user-attachments/assets/37a79f50-0e41-4d3e-9036-f9c2b88b4640" />


### Display the Eroded Image
<img width="408" height="414" alt="image" src="https://github.com/user-attachments/assets/05aca7f2-62c4-41a7-8982-2620d8baf796" />


### Display the Dilated Image
<img width="410" height="413" alt="image" src="https://github.com/user-attachments/assets/cdb5d08a-fad0-469d-86e2-bcf48dc4404d" />


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
