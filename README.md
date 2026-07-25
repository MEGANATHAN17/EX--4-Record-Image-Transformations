# EX--4-Record-Image-Transformations

# Aim

To write a Python program using OpenCV to perform various geometric transformations on an image.

The program performs the following operations:

Image Translation
Image Scaling (Resizing)
Image Shearing
Image Reflection (Flipping)
Image Rotation
Software Used
Anaconda – Python 3.7
Jupyter Notebook / VS Code
OpenCV (cv2)
NumPy
Matplotlib
# Algorithm

Step 1:
Import the required libraries: OpenCV, NumPy, and Matplotlib.

Step 2:
Read the input image in color mode.

Step 3: Image Translation
Create a translation matrix to shift the image
Move the image 50 pixels to the right and 80 pixels down
Apply transformation using cv2.warpAffine()
Display original and translated images
Step 4: Image Scaling
Resize the image to 0.5× (downscale)
Resize the image to 2× (upscale)
Use cv2.resize()
Display original, downscaled, and upscaled images
Step 5: Image Shearing
Create transformation matrices for:
Horizontal shearing
Vertical shearing
Apply transformations using cv2.warpAffine()
Display original and sheared images
Step 6: Image Reflection
Perform flipping using cv2.flip():
Horizontal reflection
Vertical reflection
Both axes
Display all reflected images
Step 7: Image Rotation
Create rotation matrices for:
45° rotation
90° rotation
Use cv2.getRotationMatrix2D() and cv2.warpAffine()
Display original and rotated images
# Program :

Developed By:
Name: MEGANATHAN R
Register No: 212224230156

# PROGRAM :
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread('ex2.jpg') 
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title("Original Image")  
plt.axis('off') 
```
# OUTPUT :

<img width="686" height="463" alt="image" src="https://github.com/user-attachments/assets/57c0f3a7-43c1-4275-ac26-079551cb16d4" />


# PROGRAM :
```
tx, ty = 100, 50  
M_translation = np.float32([[1, 0, tx], [0, 1, ty]])  
translated_image = cv2.warpAffine(image, M_translation, (image.shape[1], image.shape[0]))  
plt.imshow(cv2.cvtColor(translated_image, cv2.COLOR_BGR2RGB)) 
plt.title("Translated Image")  
plt.axis('off')
```
# OUTPUT :

<img width="658" height="452" alt="image" src="https://github.com/user-attachments/assets/e8032665-df3c-4d11-ac45-08dd36cb9cb8" />



# PROGRAM :
```
fx, fy = 5.0, 2.0 
scaled_image = cv2.resize(image, None, fx=fx, fy=fy, interpolation=cv2.INTER_LINEAR)
plt.imshow(cv2.cvtColor(scaled_image, cv2.COLOR_BGR2RGB)) 
plt.title("Scaled Image") 
plt.axis('off')
```
# OUTPUT :

<img width="722" height="221" alt="image" src="https://github.com/user-attachments/assets/c2d5b538-b2c8-4ae9-9ce4-4def2c17d43b" />


# PROGRAM :
```
shear_matrix = np.float32([[1, 0.5, 0], [0.5, 1, 0]])  
sheared_image = cv2.warpAffine(image, shear_matrix, (image.shape[1], image.shape[0]))
plt.imshow(cv2.cvtColor(sheared_image, cv2.COLOR_BGR2RGB))  
plt.title("Sheared Image")
plt.axis('off')
```
# OUTPUT :

<img width="670" height="470" alt="image" src="https://github.com/user-attachments/assets/4ad57ec0-73b7-4af9-8870-07565a0bfa27" />


# PROGRAM :
```

reflected_image = cv2.flip(image, 2) 
plt.imshow(cv2.cvtColor(reflected_image, cv2.COLOR_BGR2RGB)) 
plt.title("Reflected Image")  
plt.axis('off')
```
# OUTPUT :

<img width="592" height="452" alt="image" src="https://github.com/user-attachments/assets/eab9cd48-1a26-4dd7-9902-f6cb08f0e66f" />


# PROGRAM :
```
(height, width) = image.shape[:2]  
angle = 45  
center = (width // 2, height // 2)  
M_rotation = cv2.getRotationMatrix2D(center, angle, 1) 
rotated_image = cv2.warpAffine(image, M_rotation, (width, height)) 
plt.imshow(cv2.cvtColor(rotated_image, cv2.COLOR_BGR2RGB)) 
plt.title("Rotated Image")  
plt.axis('off')
```
# OUTPUT :

<img width="651" height="453" alt="image" src="https://github.com/user-attachments/assets/b8fc6e01-7b65-41e5-85bd-93351ac00999" />

# PROGRAM :
```
x, y, w, h = 100, 100, 200, 150 
cropped_image = image[y:y+h, x:x+w]
plt.imshow(cv2.cvtColor(cropped_image, cv2.COLOR_BGR2RGB))
plt.title("Cropped Image") 
plt.axis('off')
```
# OUTPUT :

<img width="693" height="480" alt="image" src="https://github.com/user-attachments/assets/dbe5b6a7-3ab6-44f1-ae9c-5d0ddf92205b" />

# Result :

Thus, various geometric transformations such as translation, scaling, shearing, reflection, and rotation are successfully performed using OpenCV. These transformations demonstrate how images can be spatially manipulated for different computer vision applications.
