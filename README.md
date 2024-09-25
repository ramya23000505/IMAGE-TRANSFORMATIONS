# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
<br>

### Step2:
<br>

### Step3:
<br>

### Step4:
<br>

### Step5:
<br>

## Program:
#### Developed By: Ramya R
#### Register Number: 212223230169

## i)Original Image:
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_img = cv2.imread("rapunzel.jpg")
# cv2.imshow("image webp",input_img)
input_img = cv2.cvtColor(input_img, cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_img)
plt.show()
```
## ii)Image Translation
```
rows,cols,dim=input_img.shape
M=np.float32([[1,0,50],  [0,1,100],  [0,0,1]])
translated_image=cv2.warpPerspective(input_img,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()
```
## iii) Image Scaling
```
scale_factor = 1.5
M_scale = np.float32([[scale_factor, 0, 0],
                      [0, scale_factor, 0],
                      [0, 0, 1]])

scaled_img = cv2.warpAffine(input_img, M[:2], (int(cols*scale_factor), int(rows*scale_factor)))
plt.axis('off')
plt.imshow(scaled_img)
plt.show()
```
## iv)Image shearing
```
M_x = np.float32([[1, 0.2, 0],
                  [0, 1, 0],
                  [0, 0, 1]])

sheared_img_xaxis = cv2.warpAffine(input_img, M_x[:2], (cols, rows))
plt.axis('off')
plt.imshow(sheared_img_xaxis)
plt.show()
M_y = np.float32([[1, 0, 0],
                  [0.2, 1, 0],
                  [0, 0, 1]])

sheared_img_yaxis = cv2.warpAffine(input_img, M_y[:2], (cols, rows))
plt.axis('off')
plt.imshow(sheared_img_yaxis)
plt.show()
```
## v)Image Reflection
```
M_x = np.float32([[-1, 0, cols],
                  [0, 1, 0],
                  [0, 0, 1]])

reflected_img_xaxis = cv2.warpAffine(input_img, M_x[:2], (cols, rows))

plt.axis("off")
plt.imshow(reflected_img_xaxis)
plt.show()

M_y = np.float32([[1, 0, 0],
                  [0, -1, rows],
                  [0, 0, 1]])

reflected_img_yaxis = cv2.warpAffine(input_img, M_y[:2], (cols, rows))

plt.axis("off")
plt.imshow(reflected_img_yaxis)
plt.show()
```
## vi)Image Rotation
```
angle = np.radians(-60)
M = np.float32([[np.cos(angle), -np.sin(angle), 0],
                [np.sin(angle), np.cos(angle), 0]])
center = (cols // 2, rows // 2)
M = cv2.getRotationMatrix2D(center, -60, 1.0)
rotated_img = cv2.warpAffine(input_img, M, (cols, rows))

plt.axis('off')
plt.imshow(rotated_img)
plt.show()
```
## vii)Image Cropping
```
cropped_img = input_img[50:200, 200:400]
plt.axis('off')
plt.imshow(cropped_img)
plt.show()
```
## Output:
### i)Original image:
![Screenshot 2024-09-25 201707](https://github.com/user-attachments/assets/48508087-3404-4d81-828e-4a8c55deec48)

### ii)Image Translation
![Screenshot 2024-09-25 201715](https://github.com/user-attachments/assets/71ec157b-4db6-4d85-ae5c-63b61b0de081)

### iii) Image Scaling
![Screenshot 2024-09-25 201721](https://github.com/user-attachments/assets/389ecab1-5319-4a4f-8f9b-6fad60808ae0)

### iv)Image shearing
![Screenshot 2024-09-25 202002](https://github.com/user-attachments/assets/2530527e-9bdf-46f5-bbf9-9bca3159e8bd) ![Screenshot 2024-09-25 202008](https://github.com/user-attachments/assets/602de6b1-430b-4810-ba9d-f672f2bacf09)




### v)Image Reflection
<br>
<br>
<br>
<br>



### vi)Image Rotation
<br>
<br>
<br>
<br>



### vii)Image Cropping
<br>
<br>
<br>
<br>




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
