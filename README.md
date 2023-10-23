# OPENING--CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:

**Step 1 :** Import the necessary packages.

**Step 2 :** Create the Text using cv2.putText

**Step 3 :** Create the structuring element.

**Step 4 :** Use Opening operation.

**Step 5 :** Use Closing Operation.
 
## Program:
```
Developed BY : G Jayanth Yadav
Reg No : 212221230030
```
``` Python
# Import the necessary packages :

import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText :

img=np.zeros((100,400),dtype='uint8')
font=cv2.FONT_ITALIC
cv2.putText(img,'Jayanth',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.axis('off')
plt.imshow(img)
plt.show()

# Create the structuring element :

kernel=cv2.getStructuringElement(cv2.MORPH_RECT,(9,9))

# Use Opening operation :

image_open=cv2.morphologyEx(img,cv2.MORPH_OPEN,kernel)
plt.axis('off')
plt.imshow(image_open)
plt.show()

# Use Closing Operation :

image_close=cv2.morphologyEx(img,cv2.MORPH_CLOSE,kernel)
plt.axis('off')
plt.imshow(image_close)
plt.show()

```
## Output:

### Display the input Image

![image](https://github.com/JayanthYadav123/OPENING--CLOSING/assets/94836154/070d6ec0-d811-406d-b37f-618f97296249)


### Display the result of Opening

![image](https://github.com/JayanthYadav123/OPENING--CLOSING/assets/94836154/92d99692-62ea-467f-8dfc-5461592ef50b)


### Display the result of Closing

![image](https://github.com/JayanthYadav123/OPENING--CLOSING/assets/94836154/447a5fb0-a018-4f5e-9ddc-08c5cff712b7)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
