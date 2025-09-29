# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().



### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:
```python
# Developed By: SreeHari K
# Register Number: 212223230212

import cv2
import matplotlib.pyplot as plt 
Gray_image=cv2.imread("gray.jpg")
plt.imshow(Gray_image)
plt.show()
Color_image=cv2.imread("color.jpg")
plt.imshow(Color_image)
plt.show()

# Write your code to find the histogram of gray scale image and color image channels.
hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('gray_scale value')
plt.ylabel('pixel count')
plt.stem(hist)
plt.show()

# Display the histogram of gray scale image and any one channel histogram from color image

hist1 = cv2.calcHist([Color_image],[0],None,[256],[0,256]) 
plt.figure()
plt.title("Histogram")
plt.xlabel('color_scale value') 
plt.ylabel('pixel count')
plt.stem(hist1)
plt.show()

# Write the code to perform histogram equalization of the image.

equ1=cv2.equalizeHist(cv2.imread('color.jpg',0)) 
equ=cv2.cvtColor(equ1,cv2.COLOR_BGR2RGB) 
plt.title("Equalised Image")
plt.axis("off")
plt.imshow(equ) 
plt.show()


```
## Output:
### Input Grayscale Image and Color Image
![Screenshot 2025-04-23 195207](https://github.com/user-attachments/assets/89c5d321-7264-4021-8f7b-765bd7086a6b)



### Histogram of Grayscale Image and any channel of Color Image
![Screenshot 2025-04-23 195621](https://github.com/user-attachments/assets/2978708c-ac46-4492-8685-6cac8259e229)



### Histogram Equalization of Grayscale Image.
![Screenshot 2025-04-23 195900](https://github.com/user-attachments/assets/eccbe877-ed64-499e-8234-2663bf0ccf3f)




## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV
