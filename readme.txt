NOTE: This fork is for CMDR Claw's "sandwich" version of the EDTracker HW (i.e. with the 9150 MPU mounted directly on the back of the Arduino with arduino pins 5, 4 and TX0 providing MPU VCC, GND and INT respectively)
See http://baxpace.com/forumimages/IMG_1700.JPG and http://baxpace.com/forumimages/IMG_1701.JPG

Tested with latest Arduino Beta  1.5.8

copy to edtracker.zip  to Arduino/hardware/  and unzip

So should end up with


	Arduino/Hardware/edtracker/...   etc



In Arduino IDE select Tools->Board->Edtracker EDTracker 2


These sketches use a fork of Richard Barnett's sensor fusion library (originals available here https://github.com/richards-tech/RTIMULib-Arduino)

N.B. Sketch uses 'auto-bias on startup' method of calibration so keep still for a few seconds when pluggin in.


Values to play with on RTIMULib (see comments in code);


RTFusionRTQ.cpp

	RTQF_QVALUE
	RTQF_RVALUE


RTIMU.cpp
	
	COMPASS_ALPHA  - controls low pass filtering on compass value

