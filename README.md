# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import numpy module as np and pandas as pd.
<br>

### Step2:
Assign the values to variables in the program.
<br>

### Step3:
Get the values from the user appropriately.
<br>

### Step4:
Continue the program by implementing the codes of required topics
<br>

### Step5:
Thus the program is executed in google colab.
<br>

## Program:

#### DEVELOPED BY: ROSELIN MARY JOVITA.S
#### REG NO: 212222230122
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('masha.webp')
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)

plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis('off')
```

#### OUTPUT

![Screenshot 2024-10-03 105648](https://github.com/user-attachments/assets/2a0b2496-2eba-4ce1-8896-884964fcc78d)

#### i)Image Translation
```
rows, cols, _ = image.shape
M_translate = np.float32([[1, 0, 50], [0, 1, 100]])  
translated_image = cv2.warpAffine(image_rgb, M_translate, (cols, rows))

plt.imshow(translated_image)
plt.title("Translated Image")
plt.axis('off')
```
#### OUTPUT

![Screenshot 2024-10-03 105700](https://github.com/user-attachments/assets/48b03863-4ac9-4a39-9d44-086dff0242bb)


#### ii) Image Scaling
```
scaled_image = cv2.resize(image_rgb, None, fx=1.5, fy=1.5, interpolation=cv2.INTER_LINEAR)

plt.imshow(scaled_image)
plt.title("Scaled Image")
plt.axis('off')

```
#### OUTPUT

![Screenshot 2024-10-03 105710](https://github.com/user-attachments/assets/a8e3bf18-c614-422a-9c35-9597fd31bd19)


#### iii)Image shearing
```
M_shear = np.float32([[1, 0.5, 0], [0.5, 1, 0]])  # Shear with factor 0.5
sheared_image = cv2.warpAffine(image_rgb, M_shear, (int(cols * 1.5), int(rows * 1.5)))

plt.imshow(sheared_image)
plt.title("Sheared Image")
plt.axis('off')
```

#### OUTPUT

![Screenshot 2024-10-03 105720](https://github.com/user-attachments/assets/b65277c6-4df3-4fee-a222-833d6f368d73)


#### iv)Image Reflection
```
reflected_image = cv2.flip(image_rgb, 1)


plt.imshow(reflected_image)
plt.title("Reflected Image")
plt.axis('off')

```

#### OUTPUT

![Screenshot 2024-10-03 105730](https://github.com/user-attachments/assets/b498b982-5115-4e9f-9fa0-adf0459a675e)


#### v)Image Rotation
```
M_rotate = cv2.getRotationMatrix2D((cols / 2, rows / 2), 45, 1) 
rotated_image = cv2.warpAffine(image_rgb, M_rotate, (cols, rows))


plt.imshow(rotated_image)
plt.title("Rotated Image")
plt.axis('off')
```

#### OUTPUT

![Screenshot 2024-10-03 105740](https://github.com/user-attachments/assets/f6d66a1b-d55d-4ad2-b259-6bc89f55a596)


#### vi)Image Cropping
```
cropped_image = image_rgb[50:300, 100:400]
plt.figure(figsize=(12, 8))
plt.tight_layout()
plt.show()

plt.figure(figsize=(4, 4))
plt.imshow(cropped_image)
plt.title("Cropped Image")
plt.axis('off')
plt.show()
```

#### OUTPUT

![Screenshot 2024-10-03 105748](https://github.com/user-attachments/assets/0ee4bd72-c582-460a-a6c8-d941fa80a0b7)







## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
