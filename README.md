# CarND-Controls-PID
Self-Driving Car Engineer Nanodegree Program

---


## Dependencies

* cmake >= 3.5
 * All OSes: [click here for installation instructions](https://cmake.org/install/)
* make >= 4.1
  * Linux: make is installed by default on most Linux distros
  * Mac: [install Xcode command line tools to get make](https://developer.apple.com/xcode/features/)
  * Windows: [Click here for installation instructions](http://gnuwin32.sourceforge.net/packages/make.htm)
* gcc/g++ >= 5.4
  * Linux: gcc / g++ is installed by default on most Linux distros
  * Mac: same deal as make - [install Xcode command line tools]((https://developer.apple.com/xcode/features/)
  * Windows: recommend using [MinGW](http://www.mingw.org/)
* [uWebSockets](https://github.com/uWebSockets/uWebSockets) == 0.13, but the master branch will probably work just fine
  * Follow the instructions in the [uWebSockets README](https://github.com/uWebSockets/uWebSockets/blob/master/README.md) to get setup for your platform. You can download the zip of the appropriate version from the [releases page](https://github.com/uWebSockets/uWebSockets/releases). Here's a link to the [v0.13 zip](https://github.com/uWebSockets/uWebSockets/archive/v0.13.0.zip).
  * If you run OSX and have homebrew installed you can just run the ./install-mac.sh script to install this
* Simulator. You can download these from the [project intro page](https://github.com/udacity/CarND-PID-Control-Project/releases) in the classroom.

## Basic Build Instructions

1. Clone this repo.
2. Make a build directory: `mkdir build && cd build`
3. Compile: `cmake .. && make`
4. Run it: `./pid`. 

## Discussion

<div align="center">
<a href="https://youtu.be/FLqpYUd19uI" target="_blank"><img src="http://img.youtube.com/vi/FLqpYUd19uI/0.jpg"
alt="youtube link" width="480" height="360" border="10" /></a>
</div>

The following values for components P,I,D have been used:
 Kp = 0.2
 Kd = 0.0001
 Ki = 3.0

Proportional term Kp steers harder the further away we are from the desired trajectory.
Kp alone causes oscilation which is not desirable property so the additional term is needed - Kd.

Differential term Kd is the resistance if the car is moving to quickly toward the desired trajectory line.

Ki is the integral term - adjust to the bias in the system.

Manual tuning has been used. First, tune proportional component Kp, the other terms are zeroed.
After I minimized oscilation I started to tune differential term Kd. At the end, integral term Ki has been
tuned.
