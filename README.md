# Color Conversion

## AIM

To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.

## Software Required

Anaconda - Python 3.7.

## Algorithm

### Step1:

Import cv2 and save and image as filename.jpg.

### Step2:

Use imread(filename, flags) to read the file.

### Step3:

Use cv2.cvtColor(src, code, dst, dstCn) to convert an image from one color space to another.

### Step4:

Split and merge the image using cv2.split and cv2.merge commands.

### Step5:

End the program and close the output image windows.


## Program

```python

# Developed By: Guru Prasad.B
# Register Number: 212221230032

```

### i) Convert BGR and RGB to HSV and GRAY

```python
import cv2
sun_color_image = cv2.imread('kars.jpg')
cv2.imshow('Original image', sun_color_image)
hsv_image = cv2.cvtColor(sun_color_image, cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV' ,hsv_image )
gray_image1 = cv2.cvtColor (sun_color_image, cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()
```

### ii)Convert HSV to RGB and BGR

```python
import cv2
sun_color_image = cv2.imread('kars.jpg')
cv2.imshow('Original image', sun_color_image)
hsv_image = cv2.cvtColor(sun_color_image, cv2.COLOR_HSV2RGB)
cv2.imshow('HSV2RGB' ,hsv_image )
gray_image1 = cv2.cvtColor (sun_color_image, cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2BGR', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()
```

### iii)Convert RGB and BGR to YCrCb

```python
import cv2
sun_color_image = cv2.imread('kars.jpg')
cv2.imshow('Original image', sun_color_image)
gray_image1 = cv2.cvtColor (sun_color_image, cv2.COLOR_RGB2YCrCb)
cv2.imshow('RGB2YCrCb', gray_image1)
gray_image1 = cv2.cvtColor (sun_color_image, cv2.COLOR_BGR2YCrCb)
cv2.imshow('BGR2YCrCb', gray_image1)
cv2.waitKey(0)
cv2. destroyAllWindows()
```

### iv)Split and Merge RGB Image

```python
import cv2
image = cv2.imread('Kars.jpg')
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
```

### v) Split and merge HSV Image

```python
import cv2
image = cv2.imread('kars.jpg')
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

![i1](https://user-images.githubusercontent.com/95342910/227983301-da011d78-58ae-4796-b90e-502c611064c3.png)


### ii) HSV to RGB and BGR

![i2](https://user-images.githubusercontent.com/95342910/227983323-ae498262-de6f-4284-bc37-8e7f95384484.png)


### iii) RGB and BGR to YCrCb

![i3](https://user-images.githubusercontent.com/95342910/227983353-25549c22-f827-47f4-a3f7-b7ea581021bb.png)


### iv) Split and merge RGB Image

![i4](https://user-images.githubusercontent.com/95342910/227983382-dbda7009-bf68-4fad-b968-f942d68ed291.png)


### v) Split and merge HSV Image


![i5](https://user-images.githubusercontent.com/95342910/227983412-c8353253-2415-4e71-994c-9466e9fc9d29.png)


## Result:

Thus the color conversion was performed between RGB, HSV and YCbCr color models.


