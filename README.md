# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
<br>

### Step2:
<br>

### Step3:
<br>

### Step4:
<br>

### Step5:
<br>

## Program:
```python
Developed By:
Register Number:
```
### Original Image 
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("dog.jpg")
image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
plt.axis('off')
plt.imshow(image)
plt.show()
```
### i)Image Translation
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("dog.jpg")
image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
plt.axis('off')
rows,cols,dim = image.shape
M = np.float32([[1,0,514],[0,1,-100],[0,0,1]])
translated_image = cv2.warpPerspective(image,M,(cols,rows))
plt.axis('off')
plt.imshow(translated_image)
plt.show()
```

### ii) Image Scaling
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("dog.jpg")
image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
plt.axis('off')
rows,cols,dim = image.shape
M = np.float32([[2.4,0 ,0],[0,1.9,0],[0,0,1]])
scaled_image = cv2.warpPerspective(image,M,(cols*2,rows*2))
plt.axis('off')
plt.imshow(scaled_image)
plt.show()
```


### iii)Image shearing
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("dog.jpg")
image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
plt.axis('off')
rows,cols,dim = image.shape
M_x= np.float32([[1,0.8 ,0],[0,1,0],[0,0,1]])
M_y = np.float32([[1,0,0],[0.6,1,0],[0,0,1]])
sheared_img_xaxis = cv2.warpPerspective(image,M_x,(int(cols*1.5),int(rows*1.5)))
sheared_img_yaxis = cv2.warpPerspective(image,M_y,(int(cols*1.5),int(rows*1.5)))
plt.axis('off')
plt.imshow(sheared_img_xaxis)
plt.imshow(sheared_img_yaxis)
plt.show()
```



### iv)Image Reflection
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("dog.jpg")
image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
plt.axis('off')
rows,cols,dim = image.shape
M_x= np.float32([[1,0 ,0],[0,-1,rows],[0,0,1]])
M_y = np.float32([[-1,0,cols],[0,1,0],[0,0,1]])
reflected_img_xaxis = cv2.warpPerspective(image,M_x,(int(cols),int(rows)))
reflected_img_yaxis = cv2.warpPerspective(image,M_y,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(reflected_img_xaxis)
plt.imshow(reflected_img_yaxis)
plt.show()
```




### v)Image Rotation
```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("dog.jpg")
image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
plt.axis('off')
rows,cols,dim = image.shape
angle = np.radians(10)
M = np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]])
rotated_img = cv2.warpPerspective(image,M,(int(cols),int(rows)))
plt.axis('off')
plt.imshow(rotated_img)
plt.show()
```



### vi)Image Cropping

```python
import numpy as np
import cv2
import matplotlib.pyplot as plt
image = cv2.imread("dog.jpg")
image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
plt.axis('off')
rows,cols,dim = image.shape
cropped_img = image[700:900,600:900]
plt.axis('off')
plt.imshow(cropped_img)
plt.show()



```
## Output:
### Original Image 
![image](https://github.com/SANTHAN-2006/IMAGE-TRANSFORMATIONS/assets/80164014/17677da0-17a6-4b8f-8507-c7c807b9c418)

### i)Image Translation
![image](https://github.com/SANTHAN-2006/IMAGE-TRANSFORMATIONS/assets/80164014/ee3bf23a-678d-4c14-804b-76bb6572aa1c)

<br>
<br>
<br>

### ii) Image Scaling
![image](https://github.com/SANTHAN-2006/IMAGE-TRANSFORMATIONS/assets/80164014/2224e04f-1da1-49d8-9ff8-f8ba510dfd2d)

<br>
<br>


### iii)Image shearing
![image](https://github.com/SANTHAN-2006/IMAGE-TRANSFORMATIONS/assets/80164014/19dceb9d-5ab5-417f-a713-3ee55c358588)

<br>
<br>
<br>


### iv)Image Reflection
![image](https://github.com/SANTHAN-2006/IMAGE-TRANSFORMATIONS/assets/80164014/28d26666-4a20-4ded-9932-30b0d7c646ab)

<br>
<br>
<br>
<br>



### v)Image Rotation
![image](https://github.com/SANTHAN-2006/IMAGE-TRANSFORMATIONS/assets/80164014/c184478c-ad60-4027-8908-c07699d473e7)

<br>
<br>
<br>
<br>



### vi)Image Cropping
![image](https://github.com/SANTHAN-2006/IMAGE-TRANSFORMATIONS/assets/80164014/b7e86607-db43-4b67-8a29-6059059f29e7)

<br>
<br>
<br>
<br>




## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
