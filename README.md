# emotion-detection-opencv

Install python 3.7

python -m pip install numpy

python -m pip install opencv-python

https://www.learnopencv.com/install-opencv-3-and-dlib-on-windows-python-only/

```
import cv2
print(cv2.**version**)
```

Camera test

```
import numpy as np
import cv2
cap = cv2.VideoCapture(0)
cap.set(3,640) # set Width
cap.set(4,480) # set Height
while(True):
ret, frame = cap.read()
frame = cv2.flip(frame, -1) # Flip camera vertically
gray = cv2.cvtColor(frame, cv2.COLOR_BGR2GRAY)

cv2.imshow('frame', frame)
cv2.imshow('gray', gray)

k = cv2.waitKey(30) & 0xff
if k == 27: # press 'ESC' to quit
break
cap.release()
cv2.destroyAllWindows()
```
