# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
## Step1:
Import the required packages
## Step2:
Load the image file in the program.
## Step3:
Use the techniques for Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.
## Step4:
Display the modified image output.
## Step5:
End the program.
## Program:
``
Developed By:BALAJI J
Register Number:212221243001
## i)Image Translation
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image = cv2.imread( "/content/dipt image.png")
input_image = cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis( 'off')
plt.imshow(input_image)
plt.show()
rows,cols,dim =input_image.shape
M =np.float32([[1,0,100],
               [0,1,100],
               [0,0,1]])
translated_image =cv2.warpPerspective(input_image, M, (cols, rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()
```

## ii) Image Scaling
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("/content/dipt image.png")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M=np.float32([[1.5,0 ,0],
              [0,1.8,0],
              [0,0,1]])
scaled_img=cv2.warpPerspective(in_img, M,(cols,rows))
plt.axis('off')
plt.imshow(scaled_img)
plt.show()
```


## iii)Image shearing
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("/content/dipt image.png")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M=np.float32([[1.5,0 ,0],
              [0,1.8,0],
              [0,0,1]])
scaled_img=cv2.warpPerspective(in_img, M,(cols,rows))
plt.axis('off')
plt.imshow(scaled_img)
plt.show()
```


## iv)Image Reflection

```
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("/content/dipt image.png")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
M_x=np.float32([[1,0.5,0],
                [0,1 ,0],
                [0,0 ,1]])
M_y=np.float32([[1,  0,0],
                [0.5,1,0],
                [0,  0,1]])
sheared_img_x=cv2.warpPerspective(in_img,M_x,(int(cols),int(rows)))
sheared_img_y=cv2.warpPerspective(in_img,M_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(sheared_img_x)
plt.show()
plt.axis('off')
plt.imshow(sheared_img_y)
plt.show()
```


## v)Image Rotation

```
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img=cv2.imread("/content/dipt image.png")
in_img=cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
rows,cols,dim=in_img.shape
angle=np.radians(10)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
              [np.sin(angle),np.cos(angle),0],
              [0,0,1]])
rotated_img=cv2.warpPerspective(in_img,M,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()
```
## vi)Image Cropping
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
in_img = cv2.imread("/content/dipt image.png")
in_img = cv2.cvtColor(in_img,cv2.COLOR_BGR2RGB)
plt.imshow(in_img)
plt.show()
cropped_img=in_img[2000:3000 ,1000:2500]
plt.imshow(cropped_img)
plt.show()




```
## Output:
### i)Image Translation

![314085553-4a95f5af-fa9b-4e03-92ab-b43d5013de6a](https://github.com/user-attachments/assets/625becee-9682-4f0d-b107-b9e63eb0d712)


### ii) Image Scaling

![314086086-cd02e76a-7279-4e04-a8fc-0785029f32bd](https://github.com/user-attachments/assets/b5fa5c08-a01e-43bb-8595-f9e18aa263a0)


### iii)Image shea

![314086794-9841f537-e871-4e28-9e1e-3d6cab813046](https://github.com/user-attachments/assets/b0b2987a-b49c-4565-a776-5bb85414a08e)
ring


### iv)Image Reflection


![314087254-8234ac6f-dba2-4563-a06b-4895d8ad9b66](https://github.com/user-attachments/assets/f435751d-694c-4592-a0cf-4b36784c5ab5)


### v)Image Rotation

![314088040-90e72f5f-c838-4b65-b650-bd5b51c4908f](https://github.com/user-attachments/assets/185f3013-63fe-442f-9389-6c3cbfb15871)




### vi)Image Cropping

![314091303-d92b9cab-34c9-46e7-9f57-bbf2ba206d9c](https://github.com/user-attachments/assets/cedb4618-f964-4be9-9424-b6858dec0982)


## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
