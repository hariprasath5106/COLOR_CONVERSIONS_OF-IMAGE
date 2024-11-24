## AIM
Write a Python program using OpenCV that performs the following tasks:

i) Read and Display an Image.

ii) 	Draw Shapes and Add Text.

iii) Image Color Conversion.

iv) Access and Manipulate Image Pixels.

v) Image Resizing

vi) Image Cropping

vii) Image Flipping

viii)	Write and Save the Modified Image


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Load an image from your local directory and display it.
### Step2:
o	Draw a line from the top-left to the bottom-right of the image.
o	Draw a circle at the center of the image.
o	Draw a rectangle around a specific region of interest in the image.
o	Add the text "OpenCV Drawing" at the top-left corner of the image.

### Step3:
o	Convert the image from RGB to HSV and display it.
o	Convert the image from RGB to GRAY and display it.
o	Convert the image from RGB to YCrCb and display it.
o	Convert the HSV image back to RGB and display it.

### Step4:
o	Access and print the value of the pixel at coordinates (100, 100).
o	Modify the color of the pixel at (200, 200) to white.

### Step5:
o	Resize the original image to half its size and display it.
### Step6:
o	Crop a region of interest (ROI) from the image (e.g., a 100x100 pixel area starting at (50, 50)) and display it.
### Step7:
o	Flip the original image horizontally and display it.
o	Flip the original image vertically and display it.

### Step8:
o	Save the final modified image to your local directory.


##### Program:
### Developed By: HARI PRASATH S
### Register Number: 212222240034


## Output:

### i)Read and Display an Image
```
import cv2
image=cv2.imread('hari.jpg',1)
cv2.imshow('Image Window', image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![ex1 dipt](https://github.com/user-attachments/assets/b59cb1ad-2bcc-4e01-9309-b94acbbe5545)


### ii)Draw Shapes and Add Text
```
import cv2
image = cv2.imread("hari.jpg")
res = cv2.line(image, (0, 0), (image.shape[1], image.shape[0]), (255,0,0), 10)
cv2.imshow('WINDOW', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![exp11 2](https://github.com/user-attachments/assets/f91d3607-4c2a-4a22-a236-1c4238bf412a)


### iii)Draw a circle at the center of the image
```
import cv2
image = cv2.imread("hari.jpg")
height, width, _ = image.shape
center_coordinates = (width // 2, height // 2)
res = cv2.circle(image, center_coordinates, 120, (0, 255, 0), 10)
cv2.imshow('WINDOW', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![exp11 3](https://github.com/user-attachments/assets/f542b6a7-5547-4d67-a2d2-a20097fce6d8)


### iv)Draw a rectangle around a specific region of interest in the image.
```
import cv2
image = cv2.imread("hari.jpg")
start = (150, 100)
stop = (300, 200)
color = (255, 255, 100)
thickness = 10           
res_img = cv2.rectangle(image, start, stop, color, thickness)
cv2.imshow('WINDOW', res_img)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![image](https://github.com/user-attachments/assets/ce8b6d58-0e85-4e33-b60b-966e41b01603)


### v).Add the text "OpenCV Drawing" at the top-left corner of the image.
```
import cv2
image = cv2.imread("hari.jpg")
text = "Hariprasath"
position = (10, 50)
font = cv2.FONT_HERSHEY_SIMPLEX
font_scale = 1
color = (255, 255, 255) 
thickness = 2
res = cv2.putText(image, text, position, font, font_scale, color, thickness, cv2.LINE_AA)
cv2.imshow('WINDOW', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![exp11 5](https://github.com/user-attachments/assets/04f8ea85-cc25-42ef-9f92-cdc53ab927c0)



### vi)Image Color Conversion
```
import cv2
image = cv2.imread('hari.jpg',1)
cv2.imshow('ORIGINAL IMAGE',image)
hsv = cv2.cvtColor(image,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![exp11 6](https://github.com/user-attachments/assets/ae9962ba-0de3-4dd1-866f-682100483eb1)


### vii) Convert the image from RGB to GRAY and display it.
```
import cv2
image = cv2.imread('hari.jpg',1)
cv2.imshow('ORIGINAL IMAGE',image)
gray = cv2.cvtColor(image,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

![exp11 7](https://github.com/user-attachments/assets/61e67563-af26-4589-9495-dcd5bcb6ac4d)

### viii) Convert the image from RGB to YCrCb and display it.
```
import cv2
image = cv2.imread('hari.jpg',1)
cv2.imshow('ORIGINAL IMAGE',image)
YCrCb = cv2.cvtColor(image, cv2.COLOR_BGR2YCrCb)
cv2.imshow('RGB-2-YCrCb',YCrCb)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![exp11 8](https://github.com/user-attachments/assets/1ee8663a-f6d9-49ba-b87b-b8e159a5b87a)

### ix) Convert the HSV image back to RGB and display it.
```
import cv2
image = cv2.imread('hari.jpg',1)
cv2.imshow('ORIGINAL IMAGE',image)
RGB = cv2.cvtColor(image,cv2.COLOR_HSV2BGR)
cv2.imshow('HSV2RGB',RGB)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![exp11 9](https://github.com/user-attachments/assets/d429111c-7708-4d4b-a679-8f458eff5394)

### x) Access and Manipulate Image Pixels
```
pixel_value = image[100, 100]
print(f"Pixel value at (100, 100): {pixel_value}")
```
![exp11 10](https://github.com/user-attachments/assets/8d803dce-40fb-449c-ac9d-b34c2d932563)

### xi) Modify the color of the pixel at (200, 200) to white
```
import cv2
image = cv2.imread('hari.jpg',1)
cv2.imshow('ORIGINAL IMAGE',image)
image[200, 200] = [255, 255, 255] 
cv2.imshow('MODIFIED IMAGE', image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![exp11 11](https://github.com/user-attachments/assets/42c5c8b7-5e95-45c2-8135-04e1ff8236d9)

### xii) Image Resizing:
```
cv2.imshow('ORIGINAL IMAGE',image)
resized_image = cv2.resize(image, (image.shape[1] // 2, image.shape[0] // 2))
cv2.imshow('RESIZED IMAGE', resized_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![exp11 12](https://github.com/user-attachments/assets/013478b0-a7f0-4a17-b2eb-7d4f13bcb355)

### xiii) Image Cropping
```
import cv2
image = cv2.imread('hari.jpg',1)
image = cv2.resize(image,(400,300))
x, y = 50, 50
width, height = 100, 100
roi = image[y:y + height, x:x + width]
cv2.imshow('CROPPED IMAGE', roi)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![exp11 13](https://github.com/user-attachments/assets/2eb3a014-bb71-4c7e-bf89-76b4c5baa9aa)

### xiv) Image Flipping:
```
import cv2
image = cv2.imread("hari.jpg")
res=cv2.rotate(image,cv2.ROTATE_90_CLOCKWISE)
cv2.imshow('ORIGINAL IMAGE',image)
cv2.imshow('FLIPPED IMAGE', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![exp11 14](https://github.com/user-attachments/assets/54bddb08-53bc-4b2e-8165-b334c6b01ebb)

### xv) Flip the original image vertically and display it.
```
import cv2
image = cv2.imread("hari.jpg")
res=cv2.rotate(image,cv2.ROTATE_90_CLOCKWISE)
cv2.imshow('ORIGINAL IMAGE',image)
cv2.imshow('FLIPPED IMAGE', res)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
![exp11 15](https://github.com/user-attachments/assets/b3ccc24a-80e4-404e-880a-ad2b9edf04db)

### xvi) Write and Save the Modified Image
```
import cv2
img = cv2.imread("hari.jpg")
img = cv2.resize(img,(300,200))
cv2.imwrite('nature_pic.jpg',img)
```
![exp11 16](https://github.com/user-attachments/assets/2cc03a27-ab5e-49da-81c1-02065561773c)

## Result:
Thus the images are read, displayed, and written ,and color conversion was performed  successfully using the python program.







