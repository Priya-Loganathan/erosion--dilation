# Implementation-of-Erosion-and-Dilation

## Aim:
To implement Erosion and Dilation using Python and OpenCV.

## Software Required:
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm:
### Step1:
Import the necessary pacakages.

### Step2:
Create the text using cv2.putText.

### Step3:
Create the structuring element.

### Step4:
Erode the image.

### Step5:
Dilate the Image.

## Program:
### Import the necessary packages
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
```

### Create the Text using cv2.putText
```
img = np.zeros((100,400),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img ,'CUTE',(60,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')
```

### Create the structuring element
```
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)
```

### Erode the image
```
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')

```

### Dilate the image
```
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')
```

## Output:
### Display the input Image
<img width="347" alt="326269651-83804a6e-7d26-4ea6-97e3-fa30e15eb268" src="https://github.com/Priya-Loganathan/erosion--dilation/assets/121166075/c837b553-8352-4bfb-aeb4-e60f675885f0">

### Display the Eroded Image
<img width="344" alt="326269695-71e54801-29bb-4894-ad68-7d34ee364a9c" src="https://github.com/Priya-Loganathan/erosion--dilation/assets/121166075/e91cf755-7651-4dad-b3d5-03d2ceb91792">

### Display the Dilated Image
<img width="347" alt="326269730-3579027b-a658-44f8-9c60-5a423c0ce6f9" src="https://github.com/Priya-Loganathan/erosion--dilation/assets/121166075/f837c1f8-f1cd-47a7-ac62-95ef647e94cf">

## Result:
Thus the generated text image is eroded and dilated using python and OpenCV.
