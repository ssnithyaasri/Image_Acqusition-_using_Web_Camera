# Record-Image Acquisition using Web Camera
## Aim:
 
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7
## Algorithm
### Step 1:
Use cv2.VideoCapture(0) to access web camera
<br>

### Step 2:
Use cv2.imread to read the video or image
<br>

### Step 3:
Use cv2.imwrite to save the image
<br>

### Step 4:
Use cv2.imshow to show the video
<br>

### Step 5:
End the program and close the output video window by pressing 'q'
<br>

## Program:

### Developed By:NITHYAA SRI S S
### Register No:212222230100

## i) Write the frame as JPG file
```
import cv2

cap = cv2.VideoCapture(0) frame_number = 0 # Initialize frame number

while frame_number < 5:

ret, frame = cap.read()

cv2.imshow('frame', frame)

# Save frame as JPG file cv2.imwrite(f"frame_{frame_number}.jpg", frame) frame_number += 1

if cv2.waitKey(1) & 0xFF == ord('q'):

break

cap.release()

cv2.destroyAllWindows()  
```




## ii) Display the video
```
import cv2
videoCaptureObject = cv2.VideoCapture(0)
while(True):
    ret,frame = videoCaptureObject.read()
    cv2.imshow('RESULT',frame)
    if cv2.waitKey(1) == ord('q'):
        break
videoCaptureObject.release()
cv2.destroyAllWindows()
```




## iii) Display the video by resizing the window
```
import cv2
cap = cv2.VideoCapture(0)
# Create a resizable window
cv2.namedWindow('Video', cv2.WINDOW_NORMAL)
while True:
ret, frame = cap.read()
cv2.imshow('Video', frame)
# Resize the window
cv2.resizeWindow('Video', 10, 200)
if cv2.waitKey(1) & 0xFF == ord('q'):
break
cap.release()
cv2.destroyAllWindows()
```



## iv) Rotate and display the video
```
import cv2
cap = cv2.VideoCapture (0) # Define the rotation angle (in degrees) rotation_angle = 90

while True:
ret, frame = cap.read()
# Rotate the frame rotated_frame = cv2.rotate(frame, cv2.ROTATE_90_CLOCKWISE)
cv2.imshow('Rotated Video', rotated_frame)
if cv2.waitKey(1) & 0xFF == ord('q'):
break
cap.release()
cv2.destroyAllWindows()
```
## Output

### i) Write the frame as JPG image
![image](https://github.com/user-attachments/assets/100c99fb-e52b-4e10-9aff-8bf7e054d37c)

</br>
</br>


### ii) Display the video
![image](https://github.com/user-attachments/assets/dc72a5a1-aede-4cd3-b17d-0556b5ec6de1)

</br>
</br>


### iii) Display the video by resizing the window
![WhatsApp Image 2024-09-26 at 15 51 23_0e96b06e](https://github.com/user-attachments/assets/edf63077-1f80-4b5a-98d8-b508bc6871eb)



</br>
</br>



### iv) Rotate and display the video
![WhatsApp Image 2024-09-26 at 15 39 20_30f034b3](https://github.com/user-attachments/assets/6f5251b1-2995-4b00-b132-3438635a6b32)


</br>
</br>





## Result:
Thus the image is accessed from webcamera and displayed using openCV.
