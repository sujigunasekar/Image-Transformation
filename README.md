# Image-Transformation
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:


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
i)Image Translation
#plotting of an image :
image = cv.imread("gibli.webp")
image = cv.cvtColor(image, cv.COLOR_BGR2RGB)

plt.axis("off")
plt.imshow(image)
plt.show()

#translation of an image :
rows,cols,dim = image.shape

M = np.float32([[1,0,100], [0,1,50],[0,0,1]])
translated_image= cv.warpPerspective(image, M, (cols, rows))

plt.axis("off")
plt.imshow(translated_image)
plt.show()


ii) Image Scaling
rows,cols,dim = image.shape

M_scale = np.float32([[2,0,0], [0,1.6,0],[0,0,1]])
scale_image= cv.warpPerspective(image, M_scale, (cols, rows))

plt.axis("off")
plt.imshow(scale_image)
plt.show()



iii)Image shearing
M_x = np.float32([[1,1,0], [0,1,0],[0,0,1]])

M_y = np.float32([[1,0,0], [0.4,1,0],[0,0,1]])

shear_imagex= cv.warpPerspective(image, M_x, (cols, rows))
shear_imagey= cv.warpPerspective(image, M_y, (cols, rows))

plt.axis("off")
plt.imshow(shear_imagex)
plt.show()

plt.axis("off")
plt.imshow(shear_imagey)
plt.show()



iv)Image Reflection

M_x = np.float32([[1,0,0],[0,-1,rows],[0,0,1]])

M_y = np.float32([[-1,0,cols], [0,1,0],[0,0,1]])

ref_imagex= cv.warpPerspective(image, M_x, (cols, rows))
ref_imagey= cv.warpPerspective(image, M_y, (cols, rows))

plt.axis("off")
plt.imshow(ref_imagex)
plt.show()

plt.axis("off")
plt.imshow(ref_imagey)
plt.show()



v)Image Rotation
angle=np.radians(10)

matrix=np.float32([[np.cos(angle),-np.sin(angle),0][np.sin(angle),np.cos(angle),0 [0,0,1]])

Rotated_image=cv.warpPerspective(image,matrix,(cols,rows))

plt.axis("off")
plt.imshow(Rotated_image)


vi)Image Cropping

crop_img = image[100:740, 50:400]

plt.axis("off")
plt.imshow(crop_img)
plt.show()




```
## Output:
### i)Image Translation

![Screenshot from 2023-04-06 14-37-52](https://user-images.githubusercontent.com/119559822/230333282-b23e0ccc-7ec7-42d3-9f12-e671b861da0c.png)

### ii) Image Scaling
![Uploading Screenshot from 2023-04-06 14-38-08.png…]()

### iii)Image shearing
![Uploading Screenshot from 2023-04-06 14-38-23.png…]()


### iv)Image Reflection


![Uploading Screenshot from 2023-04-06 14-38-38.png…]()


### v)Image Rotation
 



### vi)Image Cropping


 


## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
