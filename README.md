# VBI
Vision Based Interface for impaired users using OpenCV, DLIB and Python so that they can interact with computer using eye movement and blink


68 facial landmark points that can be detected from human face
![facial landmark](https://user-images.githubusercontent.com/5523584/54007972-8b22e180-4132-11e9-9baa-522e3b165775.jpeg)

Using facial points, P37-P42 for left eye and P43-P48 for right eye, we can detect eye blink.
From the above points, we calculate EAR (Eye Aspect Ratio) for both left and right eye. 
EARleft = ( distance(P38, P42) + distance(P39, P41) )/ 2Xdistance(P37, P40)
Similarly, we can calculate the EAR for right eye as well. By averaging both left, right EAR and using some threshold value of EAR, we can determine whether eye is closed or not.

![close](https://user-images.githubusercontent.com/5523584/54007966-83fbd380-4132-11e9-94e2-6d961f67811e.jpeg)
![open](https://user-images.githubusercontent.com/5523584/54007967-83fbd380-4132-11e9-988b-36157cd10c4b.jpeg)

