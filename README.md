# IMAGETRANSFORMATION

## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read the original image and save it as a image variable.

### Step2:
Translate the image.

### Step3:
Scale the image.

### Step4:
Shear the image in both the the axes.

### Step5:
Find the reflection of the image.

### Step6:
Rotate the image.

### Step7:
Crop the image.

### Step8:
Display all the transformed images.


## Program:
```python
Developed By: Dharini PV
Register Number: 212222240024
```
## Image Translation
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("lamborghini.jpeg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M = np.float32([[1.5,0,0],[0,1.7,0],[0,0,1]])
translated_image = cv2.warpPerspective(org_image,M,(cols,rows))
plt.imshow(translated_image)
plt.show()
```
## Image Scaling
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("lamborghini.jpeg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M = np.float32([[1.5,0,0],[0,1.7,0],[0,0,1]])
scaled_img = cv2.warpPerspective(org_image,M,(cols*2,rows*2))
plt.imshow(org_image)
plt.show()
```
## Image Shearing
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("lamborghini.jpeg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M_X = np.float32([[1,0.5,0],[0,1,0],[0,0,1]])
M_Y = np.float32([[1,0,0],[0.5,1,0],[0,0,1]])
sheared_img_xaxis = cv2.warpPerspective(org_image,M_X,(int(cols*1.5),int(rows*1.5)))
sheared_img_yaxis = cv2.warpPerspective(org_image,M_Y,(int(cols*1.5),int(rows*1.5)))
plt.imshow(sheared_img_xaxis)
plt.show()
plt.imshow(sheared_img_yaxis)
plt.show()
```
## Image Reflection
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("lamborghini.jpeg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
M_X = np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M_Y = np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
reflected_img_xaxis = cv2.warpPerspective(org_image,M_X,(int(cols),int(rows)))
reflected_img_yaxis = cv2.warpPerspective(org_image,M_Y,(int(cols),int(rows)))
plt.imshow(reflected_img_xaxis)
plt.show()
plt.imshow(reflected_img_yaxis)
plt.show()
```
## Image Rotation
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("lamborghini.jpeg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
angle = np.radians(25)
M = np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
rotated_img = cv2.warpPerspective(org_image,M,(int(cols),int(rows)))
plt.imshow(rotated_img)
plt.show()
```
## Image Cropping
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
org_image = cv2.imread("lamborghini.jpeg")
org_image = cv2.cvtColor(org_image,cv2.COLOR_BGR2RGB)
plt.imshow(org_image)
plt.show()
rows,cols,dim = org_image.shape
cropped_img=org_image[80:900,80:500]
plt.imshow(cropped_img)
plt.show()
```
## Output:
### i)Image Translation
![Screenshot from 2023-09-07 21-50-58](https://github.com/DHARINIPV/IMAGETRANSFORMATION/assets/119400845/df573749-460b-4abc-9560-b4f01b900d5c)


### ii) Image Scaling
![Screenshot from 2023-09-07 21-53-22](https://github.com/DHARINIPV/IMAGETRANSFORMATION/assets/119400845/21898650-f366-49f7-8450-354d51b052f8)


### iii)Image shearing
![Screenshot from 2023-09-07 21-54-56](https://github.com/DHARINIPV/IMAGETRANSFORMATION/assets/119400845/fc0f643a-5443-4248-a673-8b00d12ecc0a)


### iv)Image Reflection
![Screenshot from 2023-09-07 21-56-01](https://github.com/DHARINIPV/IMAGETRANSFORMATION/assets/119400845/d762d162-82fb-4d4c-97fd-e395eade7606)


### v)Image Rotation
![Screenshot from 2023-09-07 21-59-11](https://github.com/DHARINIPV/IMAGETRANSFORMATION/assets/119400845/9562bc90-08b6-4018-90bb-198dd732ad39)


### vi)Image Cropping
![Screenshot from 2023-09-07 22-00-52](https://github.com/DHARINIPV/IMAGETRANSFORMATION/assets/119400845/5e386cda-6491-4070-9b5e-c18e2a30dd08)

## Result: 
Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
