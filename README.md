# Image Acqusition using Web Camera
## Aim
 
#### To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
##### i) Write the frame as JPG 
##### ii) Display the video 
##### iii) Display the video by resizing the window
##### iv) Rotate and display the video

## Software 

### Anaconda - Python 3.7

## Algorithm

### Step 1:

#### Use cv2.VideoCapture(0) to access web camera

### Step 2:

#### Use cv2.imread to read the video or image

### Step 3:

#### Use cv2.imwrite to save the image

### Step 4:

#### Use cv2.imshow to show the video

### Step 5:

End the program and close the output video window by pressing 'q'.

## Program:

### Developed By: PREMKUMAR K
### Register No: 212222230111

#### i) Write the frame as JPG file
```py
import cv2
viedoCaptureObject=cv2.VideoCapture(0)
while(True):
    ret,frame=viedoCaptureObject.read()
    cv2.imwrite("prem".jpg",frame)
    result=False
viedoCaptureObject.release()
cv2.destroyAllWindows()
```
#### ii) Display the video
```py
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    cv2.imshow('rose',frame)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```

#### iii) Display the video by resizing the window
```py
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2, :width//2]=smaller_frame
    image[height//2:, :width//2]=smaller_frame
    image[:height//2, width//2:]=smaller_frame
    image[height//2:, width//2:]=smaller_frame
    cv2.imshow('212222230111-Premkumar K',image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```
#### iv) Rotate and display the video

```py
import numpy as np
import cv2
cap=cv2.VideoCapture(0)
while True:
    ret,frame=cap.read()
    width=int(cap.get(3))
    height=int(cap.get(4))
    image=np.zeros(frame.shape,np.uint8)
    smaller_frame=cv2.resize(frame,(0,0),fx=0.5,fy=0.5)
    image[:height//2, :width//2]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:, :width//2]=smaller_frame
    image[:height//2, width//2:]=cv2.rotate(smaller_frame,cv2.ROTATE_180)
    image[height//2:, width//2:]=smaller_frame
    cv2.imshow('212222230111-Premkumar K',image)
    if cv2.waitKey(1)==ord('q'):
        break
cap.release()
cv2.destroyAllWindows()
```
## Output

### i) Write the frame as JPG image
</br>

![1](https://github.com/premkumarkarthikeyan/Image_Acqusition-_using_Web_Camera/assets/119476243/1821930a-7db9-433b-a38f-83ad21b64cc2)


</br>


### ii) Display the video
</br>

![2](https://github.com/premkumarkarthikeyan/Image_Acqusition-_using_Web_Camera/assets/119476243/876a9962-5257-44f5-9cc4-2c973912560f)

</br>


### iii) Display the video by resizing the window
</br>

![3](https://github.com/premkumarkarthikeyan/Image_Acqusition-_using_Web_Camera/assets/119476243/dd50d5e7-d6db-44ee-a677-5c28541a650b)


</br>



### iv) Rotate and display the video
</br>

![4](https://github.com/premkumarkarthikeyan/Image_Acqusition-_using_Web_Camera/assets/119476243/728dc31d-e88a-44f0-8efc-84936b6928bc)

</br>





## Result:
Thus the image is accessed from webcamera and displayed using openCV.
