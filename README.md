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
<table>
<tr>
<td width="60%">
  

#### Importing packages and reading image:
```Python
import cv2
import matplotlib.pyplot as plt
import numpy as np
img=cv2.imread("blue.jpg")
img=cv2.cvtColor(img,cv2.COLOR_BGR2RGB)

def plot(img1,nam1,img2,nam2):
  plt.figure(figsize=(9,9))
  plt.subplot(1,2,1)
  plt.imshow(img1)
  plt.title(nam1)
  plt.axis("off")
  plt.subplot(1,2,2)
  plt.imshow(img2)
  plt.title(nam2)
  plt.axis("off")
  plt.show()
```

</td>
<td>
  
```
Developed By: ROHIT JAIN D
Register Number: 212222230120
```
</td>
</tr>
</table>

<table>
<tr>
<td>

#### 1.) Smoothing Filters
##### i) Using Averaging Filter
```Python
kernel=np.ones((11,11),np.float32)/169
AvgFil=cv2.filter2D(img,-1,kernel)
plot(img1,"Original Image",
      AvgFil,"Average Filter")
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
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
WgtAvg=cv2.filter2D(img,-1,kernel1)
plot(img1,"Original Image",
      WgtAvg,"Weighted Average Filter")
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
GauBlur=cv2.GaussianBlur(img,(33,33),0,0)
plot(img1,"Original Image",
      GauBlur,"Gaussian Blur")
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
median=cv2.medianBlur(img,13)
plot(img1,"Original Image",
      median,"Median Blur")
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
kernel=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
LapKel=cv2.filter2D(img,-1,kernel)
plot(img1,"Original Image",
      LapKel,"Laplacian Kernel")
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
LapOpr=cv2.Laplacian(img,cv2.CV_64F)
plot(img1,"Original Image",
      LapOpr,"Laplacian Kernel")
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
