# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7
# IMAGE-TRANSFORMATIONS
  
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules  

### Step2:
Choose an image and save it as filename.jpg

### Step3:
Use imread to read the image

### Step4:
Use cv2.warpPerspective(image,M,(cols,rows)) to translation the image

### Step5:
Use cv2.warpPerspective(image,M,(cols2,rows2)) to scale the image

### Step6:
Use cv2.warpPerspective(image,M,(int(cols1.5),int(rows1.5))) for x and y axis to shear the image

### Step7:
Use cv2.warpPerspective(image,M,(int(cols),int(rows))) for x and y axis to reflect the image

### Step8:
Use cv2.warpPerspective(image,M,(int(cols),int(rows))) to rotate the image

### Step9:
Crop the image to remove unwanted areas from an image

### Step10:
Use cv2.imshow to show the image

### Step11:
End the program

## Program:
Developed By:ibrahim fedah s
Register Number: 212223240056

i)Image Translation
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread("img0.jpg")
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
print("Input Image:")
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M=np.float32([[1,0,100],[0,1,200],[0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(cols,rows))
plt.axis('off')
print("Image Translation:")
plt.imshow(translated_image)
plt.show()
```

ii) Image Scaling
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread('img0.jpg')
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
print("Input Image:")
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M=np.float32([[1.5,0,0],[0,1.8,0],[0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(cols*2,rows*2))
plt.axis('off')
print("Image Scaling:")
plt.imshow(translated_image)
plt.show()
```

iii)Image shearing
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread('img0.jpg')
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
print("Input Image:")
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M1=np.float32([[1,0.5,0],[0,1,0],[0,0,1]])
M2=np.float32([[1,0,0],[0.5,1,0],[0,0,1]])
translated_image1=cv2.warpPerspective(input_image,M1,(int(cols*1.5),int(rows*1.5)))
translated_image2=cv2.warpPerspective(input_image,M2,(int(cols*1.5),int(rows*1.5)))
plt.axis('off')
print("Image Shearing:")
plt.imshow(translated_image1)
plt.imshow(translated_image2)
plt.show()
```

iv)Image Reflection
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread('img0.jpg')
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
print("Input Image:")
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
M1=np.float32([[1,0,0],[0,-1,rows],[0,0,1]])
M2=np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
translated_image1=cv2.warpPerspective(input_image,M1,(int(cols),int(rows)))
translated_image2=cv2.warpPerspective(input_image,M2,(int(cols),int(rows)))
plt.axis('off')
print("Image Reflection:")
plt.imshow(translated_image1)
plt.imshow(translated_image2)
plt.show()
```

v)Image Rotation
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
input_image=cv2.imread('img0.jpg')
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
plt.axis('off')
print("Input Image:")
plt.imshow(input_image)
plt.show()
rows,cols,dim=input_image.shape
angle=np.radians(10)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
translated_image=cv2.warpPerspective(input_image,M,(int(cols),int(rows)))
plt.axis('off')
print("Image Rotation:")
plt.imshow(translated_image)
plt.show()
```

vi)Image Cropping
```
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("img0.jpg")
h, w, _ = image.shape
cropped_face = image[int(h*0.2):int(h*0.8), int(w*0.3):int(w*0.7)]
cv2.imwrite("cropped_pigeon_face.jpg", cropped_face)
plt.imshow(cv2.cvtColor(cropped_face, cv2.COLOR_BGR2RGB))
plt.axis("off")
plt.show()
```

## Output:
### i)Image Translation
<img width="297" height="389" alt="download" src="https://github.com/user-attachments/assets/7ee99c3b-f725-4d67-bef9-fc192ba9b0a2" />




### ii) Image Scaling
<img width="297" height="389" alt="download" src="https://github.com/user-attachments/assets/525fe696-4fa1-4b24-b321-aecaaa8c0f9d" />




### iii)Image shearing
<img width="297" height="389" alt="download" src="https://github.com/user-attachments/assets/7506cedf-a022-4fe0-ab15-f7c7ee780733" />



### iv)Image Reflection
<img width="297" height="389" alt="download" src="https://github.com/user-attachments/assets/6f785549-a87d-4c32-a9c0-2d9466496d48" />




### v)Image Rotation
<img width="297" height="389" alt="download" src="https://github.com/user-attachments/assets/b253d9c9-3b16-4720-9df8-f72a1ef178c1" />


### vi)Image Cropping
<img width="204" height="389" alt="download" src="https://github.com/user-attachments/assets/570bf660-9ccb-4b9d-b31f-4c3e18ecd22b" />



## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.

