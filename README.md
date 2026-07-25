# EX-_3-Record-Histogram-processing

# Aim

To write a Python program using OpenCV to perform histogram equalization on both grayscale and color images to enhance image contrast and brightness.

The program performs the following operations:

Read and display a grayscale image
Plot histogram of the grayscale image
Apply histogram equalization on grayscale image
Read and display a color image
Plot histogram of B, G, R channels
Convert image to HSV color space
Apply histogram equalization on the Value (V) channel
Convert the enhanced image back to BGR format
Display original and enhanced images with histograms
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
Read the image parrot.jpg in grayscale format.

Step 3:
Display the grayscale image and plot its histogram.

Step 4:
Apply histogram equalization using cv2.equalizeHist() to enhance contrast.

Step 5:
Display original grayscale image, its histogram, enhanced image, and its histogram using a 2 × 2 grid.

Step 6:
Read the same image in color format.

Step 7:
Split the image into B, G, R channels and plot their histograms.

Step 8:
Convert the image from BGR to HSV color space.

Step 9:
Apply histogram equalization on the V (Value) channel.

Step 10:
Merge the channels and convert the image back to BGR format.

Step 11:
Display original color image, histogram, enhanced image, and enhanced histogram using a 2 × 2 grid

Developed By:
Name: MEGANATHAN R
Register No: 212224230156



# PROGRAM :
```
import cv2
import matplotlib.pyplot as plt 
Gray_image=cv2.imread("1.jpg")
plt.imshow(Gray_image)
plt.show()
Color_image=cv2.imread("ex2.jpg")
plt.imshow(Color_image)
plt.show()
```
# OUTPUT :
<img width="772" height="387" alt="image" src="https://github.com/user-attachments/assets/7bef3ac4-b739-4162-8302-a79557fb0c23" />


# OUTPUT :
<img width="797" height="511" alt="image" src="https://github.com/user-attachments/assets/e222d87e-d572-4ec4-9bba-d3c807782ba0" />


# PROGRAM :
```
hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('gray_scale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()
```
# OUTPUT :
<img width="775" height="555" alt="image" src="https://github.com/user-attachments/assets/c465f404-eb54-494c-ba48-646896991f52" />


# PROGRAM :
```

hist1 = cv2.calcHist([Color_image],[0],None,[256],[0,256]) 
plt.figure()
plt.title("Histogram")
plt.xlabel('color_scale value') 
plt.ylabel('pixel count')
plt.stem(hist1)
plt.show()
```
# OUTPUT :
<img width="816" height="562" alt="image" src="https://github.com/user-attachments/assets/ba2bebfa-3c9a-4f09-85ce-14a72f81a915" />


# PROGRAM :
```
equ1=cv2.equalizeHist(cv2.imread('1.jpg',0)) 
equ=cv2.cvtColor(equ1,cv2.COLOR_BGR2RGB) 
plt.title("Equalised Image")
plt.axis("off")
plt.imshow(equ) 
plt.show()
```
# OUTPUT :

<img width="720" height="387" alt="image" src="https://github.com/user-attachments/assets/c4c4e522-d77e-4551-8cce-40940840500b" />


# Result:
Thus, histogram equalization is successfully performed on both grayscale and color images using OpenCV. The contrast and brightness of the images are significantly improved, enhancing visual quality and feature visibility.



