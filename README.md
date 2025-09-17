
Aim:
 
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7

## Program:
``` Python
### Developed By: NITHEESH YEGAVINTI
### Register No:  212224040370

## i) Write the frame as JPG file
import cv2
videoCaptureObject = cv2.VideoCapture(0)
while(True):
ret,frame = videoCaptureObject.read()
cv2.imshow('DAP',frame)
if cv2.waitKey(1) == ord('q'):
break
videoCaptureObject.release()
cv2.destroyAllWindows()



## ii) Display the video
import cv2
videoCaptureObject = cv2.VideoCapture(0)
while(True):
ret,frame = videoCaptureObject.read()
cv2.imshow('DAP',frame)
if cv2.waitKey(1) == ord('q'):
break
videoCaptureObject.release()
cv2.destroyAllWindows()




## iii) Display the video by resizing the window
import cv2
import numpy as np
cap = cv2.VideoCapture(0)
while True:
ret, frame = cap.read()
width = int(cap.get(3))
height = int(cap.get(4))
image = np.zeros(frame.shape, np.uint8)
smaller_frame = cv2.resize(frame, (0,0), fx = 0.5, fy=0.5)
image[:height//2, :width//2] = smaller_frame
image[height//2:, :width//2] = smaller_frame
image[:height//2, width//2:] = smaller_frame
image [height//2:, width//2:] = smaller_frame
cv2.imshow('DAP', image)
if cv2.waitKey(1) == ord('q'):
break
cap.release()
cv2.destroyAllWindows()



## iv) Rotate and display the video
import cv2
import numpy as np
cap = cv2.VideoCapture(0)
while True:
ret, frame = cap.read()
width = int(cap.get(3))
height = int(cap.get(4))
image = np.zeros(frame.shape, np.uint8)
smaller_frame = cv2.resize(frame, (0,0), fx = 0.5, fy=0.5)
image[:height//2, :width//2] = cv2.rotate(smaller_frame,cv2.ROTATE_180)
image[height//2:, :width//2] = cv2.rotate(smaller_frame,cv2.ROTATE_180)
image[:height//2, width//2:] = smaller_frame
image [height//2:, width//2:] = smaller_frame
cv2.imshow('DAP', image)
if cv2.waitKey(1) == ord('q'):
break
cap.release()
cv2.destroyAllWindows()








```
## Output

### i) Write the frame as JPG image
<img width="900" height="802" alt="Screenshot 2025-09-17 181338" src="https://github.com/user-attachments/assets/c8f2a685-d77f-4ba5-86f1-b44c9ca7b4fa" />


### ii) Display the video
<img width="955" height="744" alt="Screenshot 2025-09-17 181415" src="https://github.com/user-attachments/assets/5a59ea1a-a07a-4c60-8b35-cefe86eba3e1" />


### iii) Display the video by resizing the window
<img width="995" height="749" alt="Screenshot 2025-09-17 181440" src="https://github.com/user-attachments/assets/f565b0da-2050-4dc0-855b-6dd066dd5584" />



### iv) Rotate and display the video
<img width="994" height="742" alt="Screenshot 2025-09-17 181456" src="https://github.com/user-attachments/assets/a25a2b27-e554-4a83-b1d3-35cac7e702db" />





## Result:
Thus the image is accessed from webcamera and displayed using openCV.
