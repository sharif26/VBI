# VBI
Vision Based Interface for impaired users using OpenCV, DLIB and Python so that they can interact with computer using eye movement and blink


68 facial landmark points that can be detected from human face:
![Picture1](https://user-images.githubusercontent.com/5523584/54092435-6b720000-4362-11e9-80cd-c7815d7a4e64.png)

Using opencv, that can be done for still images:
![facial landmark](https://user-images.githubusercontent.com/5523584/54007972-8b22e180-4132-11e9-9baa-522e3b165775.jpeg)

Using facial points, P37-P42 for left eye and P43-P48 for right eye, we can detect eye blink.
From the above points, we calculate EAR (Eye Aspect Ratio) for both left and right eye. 
EARleft = ( distance(P38, P42) + distance(P39, P41) )/ 2Xdistance(P37, P40)
Similarly, we can calculate the EAR for right eye as well. By averaging both left, right EAR and using some threshold value of EAR, we can determine whether eye is closed or not.

For the below image, the EAR value is 0.20 which is less than the threshold 0.25, so we detect it as close eye.![close](https://user-images.githubusercontent.com/5523584/54007966-83fbd380-4132-11e9-94e2-6d961f67811e.jpeg)

For the below image, the EAR value is 0.37 which is greater than the threshold 0.25, so we detect it as open eye.![open](https://user-images.githubusercontent.com/5523584/54007967-83fbd380-4132-11e9-988b-36157cd10c4b.jpeg)

The below gif shows real time facial landmark detection using laptop's front camera:
![giphy3](https://user-images.githubusercontent.com/5523584/54092998-14bbf480-4369-11e9-9fef-54a27989023b.gif)

The below gif shows eye blink detection in real time using laptop camera:
![giphy2](https://user-images.githubusercontent.com/5523584/54092709-b2adc000-4365-11e9-90c9-4d6dae63f5f7.gif)

The below gif shows that using eye blink in real time, scrolling can be done on browser:
![giphy](https://user-images.githubusercontent.com/5523584/54092434-6b720000-4362-11e9-9c1c-1362e09046c6.gif)

Once we can control mouse to scroll, we can use it to zoom in google maps.  
The below gif shows that using eye blink in real time, zooming can be done in google maps:  
![giphy](https://media.giphy.com/media/YTQw0NmVjtgqlD4bjI/giphy.gif) 

Similarly we can detect if mouth is open or closed and use it to control another gesture in mouse, and the mouse position can be determined by the nose locations  
The below gif shows that using eye blink and mouth open/close in real time, left and right can be done respectively:  
![giphy](https://media.giphy.com/media/lQfiE7YhbmLPo9pOa2/giphy.gif)
