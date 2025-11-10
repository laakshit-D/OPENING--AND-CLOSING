# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages

### Step2
Create the Text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Use Opening operation

### Step5:
Use Closing Operation

## Program:
```
Developed by: LAAKSHIT D
Register Number: 212222230071
```
```py
# Import the necessary packages
import cv2
import numpy as np
from matplotlib import pyplot as plt

# Create a black image
img = np.zeros((200, 400), dtype=np.uint8)

# Create the text using cv2.putText
cv2.putText(img, 'OPENCV', (50, 120), cv2.FONT_HERSHEY_SIMPLEX, 2, (255), 5, cv2.LINE_AA)

# Create the structuring element
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (7, 7))

# Use the Opening Operation
opening = cv2.morphologyEx(img, cv2.MORPH_OPEN, kernel)

# Use the Closing Operation 
closing = cv2.morphologyEx(img, cv2.MORPH_CLOSE, kernel)

# Display the images
titles = ['Original Image', 'Opening', 'Closing']
images = [img, opening, closing]

for i in range(3):
    plt.subplot(1, 3, i+1)
    plt.imshow(images[i], cmap='gray')
    plt.title(titles[i])
    plt.axis('off')

plt.show()

```
## Output:

### Display the input Image

<img width="184" height="125" alt="image" src="https://github.com/user-attachments/assets/fae2d30f-798a-4dac-8cca-1b317de801e0" />


### Display the result of Opening

<img width="183" height="121" alt="image" src="https://github.com/user-attachments/assets/bea5ef95-3d88-48e2-abf6-4c52e5092dc9" />

### Display the result of Closing

<img width="187" height="130" alt="image" src="https://github.com/user-attachments/assets/e3057241-f528-44cd-bce1-e5bbd7f64a5b" />

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
