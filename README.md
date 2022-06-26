## EX NO:06
## DATE:3.5.22
# <p align="center">Implementation-of-Filters
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
### Developed By   : PRASHETHAA R
### Register Number: 212220230036
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
</br>
</br>
</br>
</br>
</br>
</br>
</br>
</br>
</br>
</br>
</br>
</br>
</br>

## OUTPUT:
### 1. Smoothing Filters
</br>

i) Using Averaging Filter

![avg](https://user-images.githubusercontent.com/75234942/168730788-5a020475-e84a-405a-9340-76d35d6cd11c.jpeg)

</br>
</br>
</br>
</br>
</br>

ii) Using Weighted Averaging Filter

![weightedavg](https://user-images.githubusercontent.com/75234942/168730862-b534038b-8ad0-4bf9-807b-d83e734d671b.jpeg)


</br>
</br>
</br>
</br>
</br>
</br>
</br>
</br>
</br>
</br>
</br>
</br>


iii) Using Gaussian Filter

![gauss](https://user-images.githubusercontent.com/75234942/168730966-77634123-67ca-4d20-9bb0-29ed639102c7.jpeg)


</br>
</br>
</br>
</br>
</br>

iv) Using Median Filter

![median](https://user-images.githubusercontent.com/75234942/168731031-4ccf64be-0346-47f3-848e-a274fc03d37d.jpeg)


</br>
</br>
</br>
</br>
</br>
</br>
</br>
</br>
</br>
</br>

### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal

![lapkernel](https://user-images.githubusercontent.com/75234942/168731057-e9740921-331e-46b7-a7f6-9158a66c29e7.jpeg)


</br>
</br>
</br>
</br>
</br>

ii) Using Laplacian Operator

![lapoperator](https://user-images.githubusercontent.com/75234942/168731157-e03d55b5-a9ad-47d2-8979-a821304d6f90.jpeg)


</br>
</br>
</br>
</br>
</br>

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
