# Image-Transformation
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step 1:

Import the necessary libraries and read the original image and save it as a image variable.

### Step 2:

Translate the image using M=np.float32([[1,0,20],[0,1,50],[0,0,1]]) translated_img=cv2.warpPerspective(input_img,M,(cols,rows)).

### Step 3:

Scale the image using M=np.float32([[1.5,0,0],[0,2,0],[0,0,1]]) scaled_img=cv2.warpPerspective(input_img,M,(cols,rows)).

### Step 4:

Shear the image using M_x=np.float32([[1,0.2,0],[0,1,0],[0,0,1]]) sheared_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows)).

### Step 5:

Reflection of image can be achieved through the code M_x=np.float32([[1,0,0],[0,-1,rows],[0,0,1]]) reflected_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows)).

### Step 6:

Rotate the image using angle=np.radians(45) M=np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]]) rotated_img=cv2.warpPerspective(input_img,M,(cols,rows)).

### Step 7:

Crop the image using cropped_img=input_img[20:150,60:230].

### Step 8:

Display all the Transformed images and end the program

## Program:
```
Developed By: Shyam Kumar A
Register Number: 212221230098
```
i)Image Translation
```

import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread ("cat.jpg")

input_image = cv2. cvtColor (input_image, cv2. COLOR_BGR2RGB)

plt. axis('off')

plt.imshow(input_image)
plt. show()

rows, cols, dim = input_image.shape

M = np. float32([[1, 0, 50],
                 [0, 1, 100],
                 [0, 0, 1]])

translated_image = cv2.warpPerspective (input_image, M, (cols, rows))

plt.axis("off")

plt.imshow(translated_image)
plt.show()

```

ii) Image Scaling
```

import numpy as np
import cv2
import matplotlib.pyplot as plt

input_image = cv2.imread ("cat.jpg")

plt. axis('off')

plt.imshow(input_image)

plt. show()

rows, cols, dim = input_image.shape

M = np. float32([[1.9, 0, 0],
                 [0, 1.9, 0],
                 [0, 0, 1]])

scaled_image = cv2.warpPerspective (input_image, M, (cols*2, rows*2))

plt.axis("off")
plt.imshow(scaled_image)
plt.show()

```


iii)Image shearing

```

import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread("cat.jpg")
input_image = cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_image)
plt.show()
rows,cols,dim = input_image.shape
M_x = np.float32([[1,0.3,0],
                 [0,1,0],
                 [0,0,1]])

M_y = np.float32([[1,0,0],
                 [0.3,1,0],
                 [0,0,1]])

sheared_xaxis = cv2.warpPerspective(input_image,M_x,(int(cols*1.5),int(rows*1.5)))
sheared_yaxis = cv2.warpPerspective(input_image,M_y,(int(cols*1.5),int(rows*1.5)))
plt.axis('off')
plt.imshow(sheared_xaxis)
plt.show()
plt.axis('off')
plt.imshow(sheared_yaxis)
plt.show()

```

iv)Image Reflection
```

import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread("cat.jpg")
input_image = cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_image)
plt.show()
rows,cols,dim = input_image.shape
M_x = np.float32([[1,0,0],
                 [0,-1,rows],
                 [0,0,1]])

M_y = np.float32([[-1,0,cols],
                 [0,1,0],
                 [0,0,1]])

reflected_xaxis = cv2.warpPerspective(input_image,M_x,(int(cols),int(rows)))
reflected_yaxis = cv2.warpPerspective(input_image,M_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(reflected_xaxis)
plt.show()
plt.axis('off')
plt.imshow(reflected_yaxis)
plt.show()

```



v)Image Rotation
```

import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread("cat.jpg")
input_image = cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_image)
plt.show()
rows,cols,dim = input_image.shape
angle = np.radians(20)

M = np.float32([[np.cos(angle),-(np.sin(angle)),0],
               [np.sin(angle),np.cos(angle),0],
               [0,0,1]])

rotated_image = cv2.warpPerspective(input_image,M,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(rotated_image)
plt.show()

```



vi)Image Cropping
```

import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread("cat.jpg")
input_image = cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(input_image)
plt.show()
rows,cols,dim = input_image.shape

cropped_image = input_image[200:400,200:450]

plt.axis('off')
plt.imshow(cropped_image)
plt.show()

```




```
## Output:
### i)Image Translation
![o](a1.png)

### ii) Image Scaling
![o](a2.png)


### iii)Image shearing
![o](a3.png)


### iv)Image Reflection
![o](a4.png)



### v)Image Rotation
![o](a5.png)



### vi)Image Cropping
![o](a6.png)




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
