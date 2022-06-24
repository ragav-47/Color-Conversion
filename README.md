### EX NO : 03
### DATE  : 12.04.2022
# <p align="center">Color Conversion</p>

## AIM
To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.


## Software Required:
Anaconda - Python 3.7

## ALGORITHM:
### Step 1:
Convert BGR and RGB to HSV and GRAY.
### Step 2:
Convert HSV to RGB and BGR.
### Step 3:
Convert RGB and BGR to YCrCb.
### Step 4:
Split and Merge RGB Image.
### Step 5:
Split and merge HSV Image.

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>


## Program:
```python
# Developed By: Vijayaragavan ARR
# Register Number: 212220230059

# i) Convert BGR and RGB to HSV and GRAY
import cv2
image=cv2.imread("rgb.jpg")
cv2.imshow("ORIGINAL IMAGE",image)
RGB_HSV=cv2.cvtColor(image,cv2.COLOR_RGB2HSV)
cv2.imshow("RGB_HSV_IMAGE",RGB_HSV)
RGB_GRAY=cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)
cv2.imshow("RGB_GRAY_IMAGE",RGB_GRAY)
BGR_HSV=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
cv2.imshow("BGR_HSV_IMAGE",BGR_HSV)
BGR_GRAY=cv2.cvtColor(image,cv2.COLOR_BGR2GRAY)
cv2.imshow("BGR_GRAY_IMAGE",BGR_GRAY)
cv2.waitKey(0)

# ii)Convert HSV to RGB and BGR
hsv=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
cv2.imshow("HSV_IMAGE",hsv)
HSV_RGB=cv2.cvtColor(hsv,cv2.COLOR_HSV2RGB)
cv2.imshow("HSV_RGB_IMAGE",HSV_RGB)
HSV_BGR=cv2.cvtColor(hsv,cv2.COLOR_HSV2BGR)
cv2.imshow("HSV_BGR_IMAGE",HSV_BGR)
cv2.waitKey(0)

# iii)Convert RGB and BGR to YCrCb
RGB_YCrCb=cv2.cvtColor(image,cv2.COLOR_RGB2YCrCb)
cv2.imshow("RGB_YCrCb_IMAGE",RGB_YCrCb)
BGR_YCrCb=cv2.cvtColor(image,cv2.COLOR_BGR2YCrCb)
cv2.imshow("BGR_YCrCb_IMAGE",BGR_YCrCb)
cv2.waitKey(0)

# iv)Split and Merge RGB Image
blue = image[:,:,0]
cv2.imshow("blue",blue)
green = image[:,:,1]
cv2.imshow("green",green)
red = image[:,:,2]
cv2.imshow("red",red)
merged=cv2.merge((blue,green,red))
cv2.imshow("merged",merged)
cv2.waitKey(0)

# v) Split and merge HSV Image
hsv=cv2.cvtColor(image,cv2.COLOR_BGR2HSV)
cv2.imshow("ORIGINAL HSV_IMAGE",hsv)
h, s, v = cv2.split(hsv)
cv2.imshow('h_plane', h)
cv2.imshow('s_plane', s)
cv2.imshow('v_plane', v)
mergedhsv=cv2.merge((h,s,v))
cv2.imshow('merged',mergedhsv)
cv2.waitKey(0)
```


## Output:

### i) BGR and RGB to HSV and GRAY

![1](https://user-images.githubusercontent.com/75235488/162452961-3f5e5a98-ac49-4ea7-9e37-5e99dd42c2d8.png)
![2](https://user-images.githubusercontent.com/75235488/162452979-74f196de-f63a-4123-b334-45872ec99b6c.png)

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>


### ii) HSV to RGB and BGR

![3](https://user-images.githubusercontent.com/75235488/162478800-7145382b-c874-4986-a210-9a5ea45435f5.png)

<br/>
<br/>
<br/>

### iii) RGB and BGR to YCrCb

![4](https://user-images.githubusercontent.com/75235488/162471198-fb2f8e6a-274e-4e63-9c5a-e412e82b593a.png)

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>

### iv) Split and merge RGB Image

![5](https://user-images.githubusercontent.com/75235488/162470914-98c896f3-a327-48d4-b4bb-74ed20ba0004.png)

<br/>
<br/>
<br/>

![6](https://user-images.githubusercontent.com/75235488/162470938-d2c180f6-6905-4592-b218-e61f7c7c943d.png)

<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>
<br/>


### v) Split and merge HSV Image

![7](https://user-images.githubusercontent.com/75235488/162471239-615ddb3c-bbfe-4130-ba2b-b131982568e2.png)
![8](https://user-images.githubusercontent.com/75235488/162471252-108d5f5d-2e0a-4bef-bea2-7993fd7eb6ed.png)


## Result:
Thus the color conversion was performed between RGB, HSV and YCbCr color models.
