# EX-6 IMPLEMENTATION OF FILTERS
### Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.
### Software Required:
Anaconda - Python 3.7
### Algorithm:
- Step1: Import the require libraries.
- Step2: Read the image and convert to RGB mode.
- Step3: Apply various filter methods.
- Step4: Display the Output Images.
- Step5: End the Program.
### Program:
```
Developed By: ROHIT JAIN D
Register Number: 212222230120
```
<table>
<tr>
<td>

#### 1.) Smoothing Filters
##### i) Using Averaging Filter
```Python
import cv2
import matplotlib.pyplot as plt
import numpy as np
img=cv2.imread("blue.jpg")
img=cv2.cvtColor(img,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/169
Avg_Fil=cv2.filter2D(img,-1,kernel)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(img)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(Avg_Fil)
plt.title("Average Filter Image")
plt.axis("off")
plt.show()
```
</td>
<td>
  
#### OUTPUT:<br>
<img src="https://github.com/ROHITJAIND/IMPLEMENTATION-OF-FILTERS-IN-IMAGES/assets/118707073/651b0051-1e3b-416d-b184-d9155bf0413d">
</td>
</tr>
</tr>
<td>

##### ii) Using Weighted Averaging Filter
```Python
import cv2
import matplotlib.pyplot as plt
import numpy as np
img=cv2.imread("blue.jpg")
img=cv2.cvtColor(img,cv2.COLOR_BGR2RGB)
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
Wgt_Avg_Fil=cv2.filter2D(img,-1,kernel1)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(img)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(Wgt_Avg_Fil)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()
```

</td>
<td>
  
#### OUTPUT:<br>
<img src="https://github.com/ROHITJAIND/IMPLEMENTATION-OF-FILTERS-IN-IMAGES/assets/118707073/ec12d024-2b3d-4f61-b019-7efcc4ff0178">
</td>
</tr>
</tr>
<td>
  
##### iii) Using Gaussian Filter
```Python
import cv2
import matplotlib.pyplot as plt
import numpy as np
img=cv2.imread("blue.jpg")
img=cv2.cvtColor(img,cv2.COLOR_BGR2RGB)
gaussian_blur=cv2.GaussianBlur(img,(33,33),0,0)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(img)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()
```

</td>
<td>
  
#### OUTPUT:<br>
<img src="https://github.com/ROHITJAIND/IMPLEMENTATION-OF-FILTERS-IN-IMAGES/assets/118707073/6ed5810f-4768-488c-be58-634b2d57b2fe">
</td>
</tr>
</tr>
<td>
  
##### iv) Using Median Filter
```Python
import cv2
import matplotlib.pyplot as plt
import numpy as np
img=cv2.imread("blue.jpg")
img=cv2.cvtColor(img,cv2.COLOR_BGR2RGB)
median=cv2.medianBlur(img,13)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(img)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Median Blur")
plt.axis("off")
plt.show()
```

</td>
<td>
  
#### OUTPUT:<br>
<img src="https://github.com/ROHITJAIND/IMPLEMENTATION-OF-FILTERS-IN-IMAGES/assets/118707073/39703063-9937-4ede-87cb-49003b65964f">
</td>
</tr>
</tr>
<td>

#### 2.) Sharpening Filters
##### i) Using Laplacian Kernal
```Python
import cv2
import matplotlib.pyplot as plt
import numpy as np
img=cv2.imread("blue.jpg")
img=cv2.cvtColor(img,cv2.COLOR_BGR2RGB)
kernel=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
Lapla_Kernel=cv2.filter2D(img,-1,kernel)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(img)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(Lapla_Kernel)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()
```

</td>
<td>
  
#### OUTPUT:<br>
<img src="https://github.com/ROHITJAIND/IMPLEMENTATION-OF-FILTERS-IN-IMAGES/assets/118707073/2d27a1bb-cad7-45d9-a228-20a4d56f3c97">
</td>
</tr>
</tr>
<td>

##### ii) Using Laplacian Operator
```Python
import cv2
import matplotlib.pyplot as plt
import numpy as np
img=cv2.imread("blue.jpg")
img=cv2.cvtColor(img,cv2.COLOR_BGR2RGB)
Lapla_Opertr=cv2.Laplacian(img,cv2.CV_64F)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(img)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(Lapla_Opertr)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()
```

</td>
<td>
  
#### OUTPUT:<br>
<img src="https://github.com/ROHITJAIND/IMPLEMENTATION-OF-FILTERS-IN-IMAGES/assets/118707073/e9a40619-bfdc-4169-932b-aa3bf923d2cb">
</td>
</tr>
</table>

### Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
