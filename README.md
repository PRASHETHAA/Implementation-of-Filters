# Implementation-of-Filters
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
      Import the necessary modules.
      
### Step2
For performing smoothing operation on a image.
* Average filter
```
avg_kernel=np.ones((13,13),np.float32)/169
average_filter_image=cv2.filter2D(image,-1,avg_kernel)
```
* Weighted average filter
```
wt_avg_kernel=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
wt_average_filter_image=cv2.filter2D(image,-1,wt_avg_kernel)
```
* Gaussian Blur
```
gaussian_blur=cv2.GaussianBlur(image,(31,31),0,0)
```
* Median filter
```
median_blur=cv2.medianBlur(image,11)
```
</br>
</br> 

### Step3
For performing sharpening on a image.

* Laplacian Kernel
```
lap_kernel=np.array([[-1,-1,-1],[-1,8,-1],[-1,-1,-1]])
lap_image=cv2.filter2D(image,-1,lap_kernel)
```

* Laplacian Operator
```
Lap_sharp=cv2.Laplacian(image,cv2.CV_64F)
```
</br>
</br> 

### Step4
Display all the images with their respective filters.
</br>
</br> 


## Program:
### Developed By   : P.SUGANYA
### Register Number: 212220230049
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```Python
average_kernel=np.ones((13,13),np.float32)/169
average_filter_image=cv2.filter2D(image,-1,avg_kernel)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Average Filter image')
plt.imshow(average_filter_image)
plt.show()
```

ii) Using Weighted Averaging Filter
```Python
weight_average_kernel=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
weight_average_filter_image=cv2.filter2D(image,-1,weight_average_kernel)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image[30:200,50:200])
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Weighted average Filter image')
plt.imshow(weight_average_filter_image[30:200,50:200])
plt.show()
```

iii) Using Gaussian Filter
```Python
gaussian_blur=cv2.GaussianBlur(image,(31,31),0,0)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Gaussian Filter image')
plt.imshow(gaussian_blur)
plt.show()
```

iv) Using Median Filter
```Python
median_blur=cv2.medianBlur(image,11)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Median Filter image')
plt.imshow(median_blur)
plt.show()
```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```Python
laplacian_kernel=np.array([[-1,-1,-1],[-1,8,-1],[-1,-1,-1]])
laplacian_image=cv2.filter2D(image,-1,laplacian_kernel)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Laplacian Kernel Filter image')
plt.imshow(laplacian_image)
plt.show()
```

ii) Using Laplacian Operator
```Python
Laplacian_sharp=cv2.Laplacian(image,cv2.CV_64F)
plt.figure(figsize=(10,10))
plt.subplot(1,2,1)
plt.axis("off")
plt.title('Original image')
plt.imshow(image)
plt.subplot(1,2,2)
plt.axis("off")
plt.title('Laplacian Operator Filter image')
plt.imshow(Laplacian_sharp)
plt.show()
```


## OUTPUT:
### 1. Smoothing Filters
</br>

i) Using Averaging Filter
![o1](https://user-images.githubusercontent.com/77089743/167561129-fe58cce5-df70-4afa-a43e-23e96a094ba6.PNG)

</br>
</br>
</br>
</br>
</br>

ii) Using Weighted Averaging Filter
![o2](https://user-images.githubusercontent.com/77089743/167561199-bf65ccf1-842d-4d8f-b1a7-3539184e6d25.PNG)


</br>
</br>
</br>
</br>
</br>

iii) Using Weighted Averaging Filter
![o3](https://user-images.githubusercontent.com/77089743/167561237-f0cb1bd8-2357-48a5-8893-13b29d0bc438.PNG)


</br>
</br>
</br>
</br>
</br>

iv) Using Median Filter
![o4](https://user-images.githubusercontent.com/77089743/167561267-1471118a-dfb8-43e9-8a4f-54e80d94893f.PNG)

</br>
</br>
</br>
</br>
</br>

### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal
![o5](https://user-images.githubusercontent.com/77089743/167561287-7a36663c-109b-40e1-8313-2746d21bac32.PNG)


</br>
</br>
</br>
</br>
</br>

ii) Using Laplacian Operator
![o6](https://user-images.githubusercontent.com/77089743/167561322-06c1abe6-a3c0-45f3-ab7a-62b4bab42d56.PNG)

</br>
</br>
</br>
</br>
</br>

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
