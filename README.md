# PID Controller

A PID controller is implemented in C++ to maneuver the vehicle around the track.

---

## Prerequisites

* Term 2 Simulator with uWebSocketIO
* cmake >= 3.5
* make >= 4.1
* gcc/g++ >= 5.4

If you want to install the libraries on linux Operating System use install-linux.sh(./install-linux.sh) or for OSX use install-mac.sh(./install-mac.sh).

---

## Basic Build Instructions

1. Clone this repo.
2. Select build directory: `cd build`
3. Compile: `cmake .. && make` 
4. Run it: `./pid `

---

## PID Components - Proportional Integral Derivate

### Proportional

- Controls the error proportionally. 
- If this parameter has a high value the car will oscillate a lot and will jump off the road. 
- If the parameter is set to a very low value the controller will react really slowly. (pid.cpp line. 28)

### Integral

 - Controls the accumulating error. 
 - It tries to eliminate a possible bias on the controller. (pid.cpp line. 29)

### Derivate

 - Controls the rate of change of error. 
 - It tries to correct the overshoot produced by the proportional (pid.cpp line. 27)

---

## Final hyperparameters

Hyperparameters have been done through manual tuning, by trial and error. I started with [0, 0, 0] and the car was moving straight. After that I started choosing a P value, and it started to go in circles. Then, I added a D value to compensate the P. A small value for I has been chosen, because with a higher value the car started to go out of the road. 
The final hyperparameters are : P , I , D = 0.15 , 0.0001 , 3.6.

---

## Results

The results can be visualized in the video file 'demo video.mp4'. 
