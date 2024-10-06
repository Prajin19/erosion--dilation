# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step-1
Initialize an Empty Image:Create a black image of size 100x600 pixels.
### Step-2
Add Text to the Image:Use a specified font to write the word "Lifestyle" on the image at a defined position.
### Step-3
Display the Original Image:Show the image containing the text without axis labels.
### Step-4
Create Structuring Elements:Define a structuring element for morphological operations (e.g., a cross-shaped kernel).
### Step-5
Erode the Image:Apply erosion to the image using the defined structuring element to reduce the size of white regions.
### Step-6
Dilate the Image:Apply dilation to the original image using the same structuring element to increase the size of white regions.
## Program:
```
Developed by : Prajin S
Register Number : 212223230151
```


### Import the necessary packages
``` Python
import cv2
import numpy as np
import matplotlib.pyplot as plt
```

### Create the Text using cv2.putText
``` Python
image = np.zeros((300, 600, 3), dtype="uint8")
text = "Prajin S"
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, text, (50, 150), font, 2, (255, 255, 255), 3)
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
plt.subplot(1, 1, 1)
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis("off")
```


### Create the structuring element
``` Python
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))
```


### Erode the image
``` Python
eroded_image = cv2.erode(image, kernel, iterations=1)
eroded_image_rgb = cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB)
plt.subplot(1, 1,1)
plt.imshow(eroded_image_rgb)
plt.title("Eroded Image")
plt.axis("off")
```



### Dilate the image
``` Python
dilated_image = cv2.dilate(image, kernel, iterations=1)
dilated_image_rgb = cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB)
plt.subplot(1, 1,1)
plt.imshow(dilated_image_rgb)
plt.title("Dilated Image")
plt.axis("off")
```




## Output:

### Display the input Image
![image](https://github.com/user-attachments/assets/b8bc65d8-665c-41ab-b556-54c6504fad20)


### Display the Eroded Image
![image](https://github.com/user-attachments/assets/798f06b2-bd72-410b-8fdb-707c6b4ee1b1)


### Display the Dilated Image
![image](https://github.com/user-attachments/assets/781e77af-9ff1-42f3-a2e1-596fbdbdcd37)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
