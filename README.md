# Wake-Up-sleepy-live-yawning-eyedrowsiness-detector-using-Dlib-openCV
detect yawning &amp; eye drowsiness(using EAR method) from live video to wake the sleepy person ,this APP built on Surabhi Kumaris paper 
<br/>

built based on this paper(https://link.springer.com/chapter/10.1007/978-981-33-4866-0_28) It is a real-time system which will detect the drowsiness among car drivers by capturing image continuously and will warn the driver whenever they will feel sleepy.
<br/>
The innovation of the present work is established on blinking of eyes and yawn frequency.

The per closure value of eye is examined for detection of drowsiness, and whenever it exceeds a certain value, then the driver is recognized to be sleepy. Similarly, we will inspect the yawn value to detect the drowsiness and whenever it exceeds its minimum threshold value it will give yawn alert.

built using <br/>
-python <br/>
-Dlib <br/>
-OpenCV <br/>

### The algorithm:
Step 1: capture the frame ffrom the live video and re-scaled and transform the frame to gray scale to reduce the computations.

Step 2: cv2 detector detect the face position and cut it from the frame. 

Step 3: Dlib predictor determine facial landmark and find position of eyes andmouth.

Step 4: The coordinates of eyes are taken to calculate the EAR ratio to detremine if the person is closing his eye or not according to its threshold wich is = 20 (EAR value)

Step 5: The coordinates of mouth are taken to calculate the distance between lips to detremine if the person is yawning or not according to its threshold wich is = 20(yawning value)

Step 6: if the (EAR value) or the (yawning value) reaches there threshold wait for some frames (30 in this app) to avoid eyes blinking then if the eyes still closed or still yawning switch the alarm on to Wake up the person or driver to prevent accident.

