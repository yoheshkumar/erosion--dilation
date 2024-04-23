## EX 09 Implementation-of-Erosion-and-Dilation
### Aim
To implement Erosion and Dilation using Python and OpenCV.
### Software Required
1. Anaconda - Python 3.7
2. OpenCV
### Algorithm:
#### Step1:<br>
Import the necessary pacakages

#### Step2:<br>
Create the text using cv2.putText

#### Step3:<br>
Create the structuring element

#### Step4:<br>
Erode the image


#### Step5: <br>
Dilate the Image

 
### Program:
```
NAME: R.M YOHESH KUMAR 
REG.NO: 212222240118
```

##### Import the necessary packages
``` Python
import numpy as np
import cv2
import matplotlib.pyplot as plt
```
##### Create the Text using cv2.putText
``` Python
img = np.zeros((100,400),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img ,'GS BOLT',(60,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img)
plt.axis('off')
```
##### Create the structuring element
``` Python
kernel = np.ones((5,5),np.uint8)
kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(5,5))
cv2.erode(img,kernel)
```
##### Erode the image
``` Python
img_erode = cv2.erode(img,kernel1)
plt.imshow(img_erode)
plt.axis('off')

```
##### Dilate the image
``` Python
img_dilate = cv2.dilate(img,kernel1)
plt.imshow(img_dilate)
plt.axis('off')



```
### Output:
#### Display the input Image
![Screenshot 2024-04-23 095251](https://github.com/yoheshkumar/erosion--dilation/assets/119393568/e29695ad-d112-4cfd-a288-134f572c4c5a)

#### Display the Eroded Image
![Screenshot 2024-04-23 095258](https://github.com/yoheshkumar/erosion--dilation/assets/119393568/d2e36fbe-d149-4a52-872d-d2e140956e06)

#### Display the Dilated Image
![Screenshot 2024-04-23 095303](https://github.com/yoheshkumar/erosion--dilation/assets/119393568/87de0bf4-107f-47d9-9f9b-5bc8f518706d)

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
