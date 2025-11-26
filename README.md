# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1

Import the required libraries.
### Step2

Convert the image from BGR to RGB.

### Step3

Apply the required filters for the image separately.
### Step4

Plot the original and filtered image by using matplotlib.pyplot.
### Step5

End the program.

## Program:
### Developed By   : Thirisha A
### Register Number: 212223040228


### 1. Smoothing Filters

i) Using Averaging Filter
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("rose.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/169
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Average Filter Image")
plt.axis("off")
plt.show()




```
ii) Using Weighted Averaging Filter
```
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()






```
iii) Using Gaussian Filter
```

gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()




```
iv)Using Median Filter
```

median=cv2.medianBlur(image2,13)
plt.title("Median Blur")
plt.axis('off')
plt.show()





```

### 2. Sharpening Filters
i) Using Laplacian Linear Kernal
```
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()






```
ii) Using Laplacian Operator
```

laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()





```

## OUTPUT:
### 1. Smoothing Filters


i) Using Averaging Filter

<img width="808" height="592" alt="484524936-cbdaf421-1a05-47de-9ab9-e09be16599e5" src="https://github.com/user-attachments/assets/e1407813-14fa-4c28-a587-6ea7881fb14b" />


ii)Using Weighted Averaging Filter

<img width="322" height="472" alt="484525090-e7cd00c9-1732-4591-b697-99a9ed5755f2" src="https://github.com/user-attachments/assets/97ae921e-131d-4696-891e-ee4b70dac179" />

iii)Using Gaussian Filter

<img width="315" height="467" alt="484525178-3ee47109-44e1-4caa-9743-fcfb81da1a2a" src="https://github.com/user-attachments/assets/f54723b1-e8ac-465d-b82c-a2c0e383f390" />


iv) Using Median Filter

<img width="672" height="463" alt="484525270-cced200c-9ac2-484a-b754-f914823f3181" src="https://github.com/user-attachments/assets/5b123e69-c14c-4e33-b9a4-1ee8e8951b1a" />


### 2. Sharpening Filters


i) Using Laplacian Kernal

<img width="335" height="461" alt="484525336-9abe2a03-88a4-4c4e-9217-4dc543e0550b" src="https://github.com/user-attachments/assets/1b3a1ae1-895d-4339-9f70-ae3423aadc6e" />


ii) Using Laplacian Operator

<img width="305" height="463" alt="484525404-bbc20d1d-a55b-4e85-aa09-4f1b09ae2d29" src="https://github.com/user-attachments/assets/b5351a60-43a4-4aad-ab8d-d14cb45404c4" />


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
