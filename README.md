# 2e10-groupx12
 In this engineering design group project, we will conceive, design and implement an autonomous vehicle and race it around a track.
 In 2E10, our robot will operate in a simplified environment: the robot follows a white line on a black mat and only has to halt for obstacles. Our task will be to focus on thecore components required for driving the vehicle and try to optimise for those.

# Overview
To demonstrate each of the challenges your group must show us one buggy successfully completing the challenge as described below. 
Obviously it would be advisable for each group to have a backup buggy available in order to deal with any hardware failures, and so it would be wise for each group to have one working buggy and one buggy under development at all times.
Bronze challenges will first be demonstrated in week 6 of term; if your group does not pass in that week you will be able to re-demo to improve your mark on the demo. 
Silver challenges will first be demonstrated in week 9 of term. Your group must have achieved a pass mark on Bronze before demonstrating Silver. As with Bronze you may re-demo in subsequent weeks in order to pass (but not to proceed to the Gold challenge)
Gold challenges will be demonstrated in week 12.

# Bronze Challenge
In summary: Traverse the track, don’t crash into any obstacles, report events wirelessly.​
In detail:
Assemble your buggy
Starting and stopping the buggy via wireless control, have it traverse the track twice. Pause for any obstacles, reporting these events to the control PC.
Details:
The track will consist of a line forming a loop with a total track length (perimeter) of at least 3m. 
The track itself is a line on a background of contrasting colour (such that it the line can be detected by the IR sensors). A light line on a dark background will be used (if you are building a section of track for testing at home then masking tape on dark card as a background would be suitable). In the weeks leading up to the demo a track will be avilable in the labs.
The track will form a loop (see image below; the track may not look precisely like this but it will approximate the shape, and in particular you will include at least two right-angle turns). The total length will be at least 3m.
The PC control program must:
Provide the user with start and stop buttons that can be used to begin and end the buggy's run on the track.
Provide an output area that displays telemetry received from the buggy during the run. 
The buggy must:
Start the run on receiving a GO command via WiFi  from the controlling PC
Stop the run on receiving a STOP command via WiFi from the controlling PC
Traverse the track twice without derailing, using the IR sensors to follow the line of the track
Pause for obstacles as detected by the US rangefinder. The stopping distance is up to you (but about 10cm is reasonable).
Report to the controlling PC when obstacles are detected and cleared (a simple "obstacle seen" message is sufficient, but you may choose to do something more details, e.g. "stopping for obstacle at 5cm distance"). The reporting does not have to display within the Processing graphics window (you can use the console).

# Silver Challenge
In addition to the Bronze challenge requirements , in the silver challenge:  
You must use a PID implementation to follow an object smoothly using the ultrasonic sensor.  This means that if a static object is held in front of the buggy then it will stop when it comes close to it (as in Bronze), but if the object is moved along the track then the buggy will adjust it's speed to maintain a comfortable distance from the object.
The buggy must maintain a comfortable safe distance from the object
The buggy must avoid both collisions and avoid lagging too far behind. 
You must display telemetry data from the buggy within the GUI. The telemetry data to be displayed is: current speed of the buggy (calculated from the encoder output) and the estimate of the current speed of the object in front of the buggy (combining the ultrasonic readings of the distance and the buggy's own velocity calculation).
You must lead your buggy around the track 2 times (one clockwise loop, and one anticlockwise loop) using a  combination of the line following im plementation devised for the Bronze challenge and your ultrasonic PID implementation.
Right after a successful silver demonstration, you have to submit to blackboard a brief (half-page) explanation on how you tuned your PID controller to achieve the demonstrated performance.  
 
Update: To resolve some questions about this challenge, The buggy must loop around the track 2 times, one clockwise and one anticlockwise. The buggy does not have to reverse or move backwards around the track. We will not penalise any groups that have the buggy backing up; it's not a requirement because it's not practical to try to do line following in reverse gear with the sensors mounted at the front of the buggy.
Note (07/03): this challenge description has been updated. The updates are marked in bold and underline.

# Gold challenge (Creative challenge)
Impress us; get as far as you can and document your work well.  
The one stipulation here is that y ou must use  the Nano 33 IoT’s on-board  IMU and the wheel encoder and make creative use of the acceleration and/or orientation data.  Consider reporting your heading and plotting it on screen.
