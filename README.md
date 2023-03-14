# READ AND WRITE AN IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.
i) Read, display, and write an image.
ii) Access the rows and columns in an image.
iii) Cut and paste a small portion of the image.

## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Choose an image and save it as a filename.jpg
### Step2:
Use imread(filename, flags) to read the file.
### Step3:
Use imshow(window_name, image) to display the image.
### Step4:
Use imwrite(filename, image) to write the image.
### Step5:
End the program and close the output image windows.
## Program:
### Developed By:V.NAVYA
### Register Number:212221230069 
i) #To Read,display the image
```
import cv2
from google.colab.patches import cv2_imshow
a = cv2.imread('w.jpg',1)
cv2_imshow(a)
cv2.waitKey(0)
  

```
#To Read,display image in diff color
```

a = cv2.imread('w.jpg',1)
cv2_imshow(a)
cv2.waitKey(0)
```
ii) # To write the image
```
colorImage = cv2.imread('w.jpg',1)
cv2.imwrite('w1.jpg',colorImage)
writtenImage = cv2.imread('w1.jpg',1)
cv2_imshow(writtenImage)
cv2.waitKey(0)



```
iii) #Find the shape of the Image
```python3

colorImage = cv2.imread('w1.jpg',1)
print(colorImage.shape)

```
iv) #To access rows and columns

```python3

import random
colorImage = cv2.imread('w1.jpg',1)
for i in range(100):
    for j in range(colorImage.shape[1]):
        colorImage[i][j]=[random.randint(0,255),random.randint(0,255),random.randint(0,255)]
cv2_imshow(colorImage)
cv2.waitKey(0)

```
v) #To cut and paste portion of image
```python3
color_img = cv2.imread('w1.jpg',1)
tag = color_img[100:200,200:400]
color_img[100:200,100:300] = tag
cv2_imshow(color_img)
cv2.waitKey(0)

```

## Output:

### i) Read and display the image

<br>

![image](https://user-images.githubusercontent.com/94165327/225051006-2d287b8a-a82d-40ae-a06c-fe38dfa82bb0.png)

![image](https://user-images.githubusercontent.com/94165327/225051180-b73968b5-8fbd-4cea-99c9-8f9bfdea251d.png)

<br>

### ii)Write the image

<br>

![image](https://user-images.githubusercontent.com/94165327/225051307-ec7ed0d9-0c04-497d-ba4d-4c5b7ddb9e23.png)

<br>

### iii)Shape of the Image

<br>

![image](https://user-images.githubusercontent.com/94165327/225051437-b6aea8fc-11e9-4225-980f-8966848e11f1.png)

<br>

### iv)Access rows and columns
<br>

![image](https://user-images.githubusercontent.com/94165327/225051550-f8aee187-da6c-4321-9ff0-d87854b19544.png)

<br>

### v)Cut and paste portion of image
<br>

![image](https://user-images.githubusercontent.com/94165327/225051802-0c2fe12f-650f-4d73-8233-67e81b9361f8.png)

<br>

## Result:
Thus the images are read, displayed, and written successfully using the python program.


