# EX.NO : 05
# DATE :

# <p align="center">Image Transformation</p>
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import the necessary libraries and read the original image and save it as a image variable.
<br>

### Step2:
Translate the image using M=np.float32([[1,0,20],[0,1,50],[0,0,1]])<br>
translated_img=cv2.warpPerspective(input_img,M,(cols,rows))
<br>

### Step3:
Scale the image using M=np.float32([[1.5,0,0],[0,2,0],[0,0,1]]) <br>
scaled_img=cv2.warpPerspective(input_img,M,(cols,rows))
<br>

### Step4:
Shear the image using M_x=np.float32([[1,0.2,0],[0,1,0],[0,0,1]]) <br>
sheared_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))
<br>

### Step5:
Reflection of image can be achieved through the code M_x=np.float32([[1,0,0],[0,-1,rows],[0,0,1]])<br> reflected_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))
<br>
### Step 6:
Rotate the image using angle=np.radians(45) M=np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]]) <br>rotated_img=cv2.warpPerspective(input_img,M,(cols,rows))

### Step 7:
Crop the image using cropped_img=input_img[20:150,60:230]

### Step 8:
Display all the Transformed images.

## Program:

### Developed By: Harshini M
### Register Number:212220230022

### i)Image Translation
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image=cv2.imread("new.jpg")
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
rows,cols,dim = input_image.shape
M = np.float32([[1,0,100],
               [0,1,100],
               [0,0,1]])
translated_image = cv2.warpPerspective(input_image,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()
```

### ii) Image Scaling
```python
M=np.float32([[3,0,0],
             [0,4.5,0],
             [0,0,1]])
scaled_img=cv2.warpPerspective(input_image,M,(cols,rows))
plt.axis('off')
plt.imshow(scaled_img)
plt.show()
```

### iii)Image shearing
```python
rows,cols,dim=input_image1.shape
M_x=np.float32([[1.5,0,0],
             [0,1,0],
             [0,0,1]])
M_y=np.float32([[1,0,0],
               [0.5,1,0],
               [0,0,1]])
sheared_img_xaxis=cv2.warpPerspective(input_image1,M_x,(int(cols*1.5),int(rows*1.5)))
sheared_img_yaxis=cv2.warpPerspective(input_image1,M_y,(int(cols*1.5),int(rows*1.5)))
plt.axis('off')
plt.imshow(sheared_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(sheared_img_yaxis)
plt.show()
```

### iv)Image Reflection
```python
M_x=np.float32([[1,0,0],
               [0,-1,rows],
               [0,0,1]])
M_y=np.float32([[-1,0,cols],
               [0,1,0],
               [0,0,1]])
reflected_img_xaxis=cv2.warpPerspective(input_image1,M_x,(cols,rows))
reflected_img_yaxis=cv2.warpPerspective(input_image1,M_y,(cols,rows))
plt.axis('off')
plt.imshow(reflected_img_xaxis)
plt.show()
plt.axis('off')
plt.imshow(reflected_img_yaxis)
plt.show()
```

### v)Image Rotation
```python
angle=np.radians(45)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
               [np.sin(angle),np.cos(angle),0],
               [0,0,1]])
rotated_img=cv2.warpPerspective(input_image1,M,(cols,rows))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()
```

### vi)Image Cropping
```python
cropped_img=input_image1[300:450,300:430]
plt.axis('off')
plt.imshow(cropped_img)
plt.show()
```
## Output:
### i)Image Translation
<br>
<img width="282" alt="image" src="https://user-images.githubusercontent.com/75235554/166098906-ffd7728f-62d0-4a19-8a19-c0537624d8af.png">
<br>

### ii) Image Scaling
<br>
<img width="327" alt="image" src="https://user-images.githubusercontent.com/75235554/166098917-a103c3ce-ff6b-4996-82a1-ab2998071712.png">
<br>


### iii)Image shearing
<br>
<img width="252" alt="image" src="https://user-images.githubusercontent.com/75235554/166098936-a2c7b1a3-5dce-4d59-b467-06ad077f0518.png">
<br>


### iv)Image Reflection
<br>
<img width="256" alt="image" src="https://user-images.githubusercontent.com/75235554/166098949-5d88e38f-438d-4aab-89f1-884fcd6171ec.png">
<br>



### v)Image Rotation
<br>
<img width="287" alt="image" src="https://user-images.githubusercontent.com/75235554/166098960-cbeab0c6-d4c9-4612-8fb4-bce3d4b0e6f0.png">
<br>



### vi)Image Cropping
<br>
<img width="215" alt="image" src="https://user-images.githubusercontent.com/75235554/166098970-c9d2a008-5f05-4d70-a5a1-7aa74c8933a8.png">
<br>




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
