# Color Conversion
## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
<br>Import cv2 and save and image as filename.jpg

### Step2:
<br>Use imread(filename, flags) to read the file.

### Step3:
<br>Use cv2.cvtColor(src, code, dst, dstCn) to convert an image from one color space toanother.

### Step4:
<br>Split and merge the image using cv2.split and cv2.merge commands

### Step5:
<br>End the program and close the output image windows.

## Program:
```python
# Developed By: ASHWIN A O
# Register Number: 212220230005
# i) Convert BGR and RGB to HSV and GRAY

import cv2
color_image = cv2.imread('dicaprio.jpg')
cv2.imshow('Original image',color_image)
hsv_image = cv2.cvtColor(color_image, cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV' ,hsv_image )
gray_image1 = cv2.cvtColor (color_image, cv2.COLOR_RGB2GRAY)cv2.imshow('RGB2GRAY', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()


# ii)Convert HSV to RGB and BGR

import cv2
color_image = cv2.imread('dicaprio.jpg')
cv2.imshow('Original image', color_image)
hsv_image = cv2.cvtColor(color_image, cv2.COLOR_HSV2RGB)
cv2.imshow('HSV2RGB' ,hsv_image )
gray_image1 = cv2.cvtColor (color_image, cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2BGR', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()




# iii)Convert RGB and BGR to YCrCb

import cv2
color_image = cv2.imread('dicaprio.jpg')
cv2.imshow('Original image',color_image)
gray_image1 = cv2.cvtColor (color_image, cv2.COLOR_RGB2YCrCb)cv2.imshow('RGB2YCrCb', gray_image1)
gray_image1 = cv2.cvtColor (color_image, cv2.COLOR_BGR2YCrCb)cv2.imshow('BGR2YCrCb', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()


# iv)Split and Merge RGB Image

import cv2
image = cv2.imread('dicaprio.jpg')
blue=image[:,:,0]
green=image[:,:,1]
red=image[:,:,2]
cv2.imshow('B-Channel',blue)
cv2.imshow('G-Channel',green)
cv2.imshow('R-Channel',red)
Merged_BGR=cv2.merge((blue,green,red))
cv2.imshow('Merged BGR Image',Merged_BGR)
cv2.waitKey(0)
cv2.destoryAllWindows()



# v) Split and merge HSV Image

import cv2
image = cv2.imread('dicaprio.jpg')
hsv = cv2.cvtColor(image, cv2.COLOR_BGR2HSV)
h,s,v = cv2.split(hsv)
cv2.imshow('Hue-Image',h)
cv2.imshow('Saturation-Image',s)
cv2.imshow('Gray-Image',v)
Merged_HSV = cv2.merge((h,s,v))
cv2.imshow('Merged HSV Image',Merged_HSV)
cv2.waitKey(0)
cv2.destoryAllWindows()

```
## Output:
### i) BGR and RGB to HSV and GRAY
<br>![dip3-1](https://user-images.githubusercontent.com/75235601/162794195-6f1828f1-6430-4e37-a61b-c13119df528e.jpg)
<br>![dip3-2](https://user-images.githubusercontent.com/75235601/162794363-7cad87bb-f815-4357-84a0-190d2cff79f4.jpg)
<br>![dip3-3](https://user-images.githubusercontent.com/75235601/162794496-fe97094f-59bc-41a3-bbdc-7377073d9149.jpg)

### ii) HSV to RGB and BGR
<br>![dip3-4](https://user-images.githubusercontent.com/75235601/162794529-5feb72cf-02b5-4978-9d22-7099e9a9f4f7.jpg)
<br>![dip3-5](https://user-images.githubusercontent.com/75235601/162794602-6d336df5-65c9-42e9-865f-588e8f98cd2c.jpg)


### iii) RGB and BGR to YCrCb
<br>![dip3-6](https://user-images.githubusercontent.com/75235601/162794623-b67b7892-7ac4-40db-b6e5-adef049fdd98.jpg)
<br>![dip3-7](https://user-images.githubusercontent.com/75235601/162794647-8daa2678-5387-4d90-a617-8ce3ac22b2d3.jpg)


### iv) Split and merge RGB Image
<br>![dip3-8](https://user-images.githubusercontent.com/75235601/162794696-30d41d69-22fe-4387-9a6b-1012862f5221.jpg)
<br>![dip3-9](https://user-images.githubusercontent.com/75235601/162794720-a63d17be-b0a7-4cd5-bdf1-b49fd4243f46.jpg)
<br>![dip3-10](https://user-images.githubusercontent.com/75235601/162794734-976d9b64-c7d0-4f9a-8833-20b4397bd7d9.jpg)

### v) Split and merge HSV Image
<br>![dip3-11](https://user-images.githubusercontent.com/75235601/162794791-ee374248-7c26-417e-806a-f300948c013e.jpg)
<br>![dip3-12](https://user-images.githubusercontent.com/75235601/162794805-de520ff3-f245-4c62-9444-c45e6224ffda.jpg)
<br>![dip3-13](https://user-images.githubusercontent.com/75235601/162794819-462f7d04-346b-40c9-afe9-dd47dc000414.jpg)
<br>![dip3-14](https://user-images.githubusercontent.com/75235601/162794832-9a5a72bd-55e1-4740-a0df-726809bd41f1.jpg)


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
