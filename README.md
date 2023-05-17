# <p align="center">Opening-and-Closing...</p>

## Aim:

To implement Opening and Closing using Python and OpenCV.

## Software Required:

  1. Anaconda - Python 3.7 ,
  
  2. OpenCV.
  
## Algorithm:

### Step 1:

Load the necessary packages requiured for the implemtation of opening and closing.

### Step 2:

Create the text image for the implemtation of opening and closing using cv2.putText function.

### Step 3:

Create the structuring image for the implemtation of opening and closing on the text image.

### Step 4:

Apply the erosion and dilation to the text image using cv2.MORPH_OPEN and cv2.MORPH_CLOSE.

### Step 5:

Display the images of the erosion and dilation applied using the plt.imshow.

### Step 6:

End the program.

## Program:

```python

Developed by : Akash A
Register Number: 212221230003
Program to implement Opening and Closing using Python and OpenCV.

```

```python

# Import the necessary packages...

import cv2
import numpy as np
import matplotlib.pyplot as plt

```

```python

# Create the Text using cv2.putText...

text_image = np.zeros((100,300),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SCRIPT_COMPLEX = 3
cv2.putText(text_image,"Akash",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("Original Text Image")
plt.imshow(text_image,'magma')
plt.axis('off')

```

```python

# Create the structuring element...

kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(9,9))

```

```python

# Use Opening operation...

image1=cv2.morphologyEx(text_image,cv2.MORPH_OPEN,kernel)
plt.title("Implementing Opening")
plt.imshow(image1,'magma')
plt.axis('off')

```

```python

# Use Closing Operation...

image2=cv2.morphologyEx(text_image,cv2.MORPH_CLOSE,kernel)
plt.title("Implementing Closing")
plt.imshow(image2,'magma')
plt.axis('off')

```


## Output:

### Display the input Image:

![a1](https://github.com/Akash020803/Opening-and-Closing/assets/94177474/a5aa8320-0e94-43f6-a528-5c668124fec2)


### Display the result of Opening:

![a2](https://github.com/Akash020803/Opening-and-Closing/assets/94177474/65c8621a-336d-4686-98cb-92f63ee22584)


### Display the result of Closing:

![a3](https://github.com/Akash020803/Opening-and-Closing/assets/94177474/ccf1bfde-d992-4fb3-9783-2f29a42bdb8d)


## Result:

Thus the Opening and Closing operation is used in the image using python and OpenCV.

