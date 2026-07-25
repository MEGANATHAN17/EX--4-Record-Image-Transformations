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
# OUTPUT :


# PROGRAM :
# OUTPUT :


# PROGRAM :
# OUTPUT :


# PROGRAM :
# OUTPUT :


# PROGRAM :
# OUTPUT :


# PROGRAM :
# OUTPUT :


