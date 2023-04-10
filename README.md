# Image-Transformation
## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
## Step 1:
Import the necessary libraries and read the original image and save it as a image variable.

## Step 2:
Translate the image using M=np.float32([[1,0,20],[0,1,50],[0,0,1]]) translated_img=cv2.warpPerspective(input_img,M,(cols,rows))

## Step 3:
Scale the image using M=np.float32([[1.5,0,0],[0,2,0],[0,0,1]]) scaled_img=cv2.warpPerspective(input_img,M,(cols,rows))

## Step 4:
Shear the image using M_x=np.float32([[1,0.2,0],[0,1,0],[0,0,1]]) sheared_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))

## Step 5:
Reflection of image can be achieved through the code M_x=np.float32([[1,0,0],[0,-1,rows],[0,0,1]]) reflected_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))

## Step 6:
Rotate the image using angle=np.radians(45) M=np.float32([[np.cos(angle),-(np.sin(angle)),0],[np.sin(angle),np.cos(angle),0],[0,0,1]]) rotated_img=cv2.warpPerspective(input_img,M,(cols,rows))

## Step 7:
Crop the image using cropped_img=input_img[20:150,60:230]

## Step 8:
Display all the Transformed images and end the program.

## Program:
```python
Developed By:Suji.G
Register Number:212222230152
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


### iii)Image shearing
![Screenshot from 2023-04-06 14-38-23](https://user-images.githubusercontent.com/119559822/230817740-30acd2f2-bb9d-43fb-906c-fe852f2d1a50.png)

### iv)Image Reflection

![Screenshot from 2023-04-06 14-38-38](https://user-images.githubusercontent.com/119559822/230817931-64735045-e351-4789-8d78-1aa97075ecf6.png)


### v)Image Rotation
 

![Screenshot from 2023-04-06 14-38-48](https://user-images.githubusercontent.com/119559822/230817921-affbc7b3-08d9-4f8d-bf1e-b221d47af764.png)


### vi)Image Cropping


 
![Screenshot from 2023-04-06 14-39-02](https://user-images.githubusercontent.com/119559822/230817903-7e637570-abb8-4850-afc4-4d0a2a1e7091.png)


## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
