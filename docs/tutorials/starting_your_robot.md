# ECE3400 Fall 2018
## Starting Your Robot

*By Kirstin Petersen, Aug 3rd 2018.*

Throughout the labs you've been developing the basic building blocks for your robot, including basic chassis, controllers, sensors and signal processing circuitry, and wireless communication for debugging. Now it is time to build your robot! 

The milestones are meant to help you structure your time towards this goal - but be sure to start this design process early. Complete systems design _take a long time_, and there are plenty of details we've left up to you. In the following text we give a couple of examples of pitfalls, but this list is not complete.

**Power**

Your robot can't have a tether. In milestone 1-2 you ran your robot on a battery, so you might be feeling pretty comfortable about this. BUT it is important to also check 1) if the FPGA runs well on the same supply, 2) if power drawn from the motors cause power surges that could hurt your signal processing circuit, and 3) if the 25MHz clock from the camera emits noise which is picked up by the rest of your cables. Also, knowing how long the battery life is of the robot, and how charged the battery must be before you can trust your robot to complete the maze well.

**Wiring**

Don't underestimate the value of nice, organized wiring. Good connections means less debugging, ordered and labeled wires means less time searching for broken wires, modularity means you can easily update your design as you go along. Be sure to use twisted wires for power/return paths as we discuss in class. Use pluggable connectectors where you know you'll be debugging sub-circuitry often. Add "operator loops" so that you can easily assemble and disassemble your robot without disconnecting everything. Good wiring TAKES TIME!

**Order!**

It will take _lots_ of code to make the robot run. You'll be developing this code over the length of the semester, so be sure to make it modular and full of comments. It is a good idea to keep a block diagram up to date with all of the sub modules and what information they feed each other! 

**Quick Calibration**

You've been optimizing the robot for the lab environment, but the final competition will be in Duffield Hall, where light and acoustics may change. (As the mechanics wear down, you may also want to re-calibrate your servo-speeds.) It is a good idea to make quick calibration routines to let you do this on the fly. E.g. for line following, have a piece of code that samples and averages a bunch of values while you hold the robot over black and white on the field. Be sure to use locally referenced variables, so that you only have to change them in one place without scrolling through pages of codes to fix them right. 

**Debugging**

Through each of the labs we will ask you to do unit tests to make sure that your sub-systems work. Keep these handy! Once you put the entire robot together, debugging will be so much easier!

**Create a Start Button Override**

If your start-signal detection fails during the competition, a “start button” override can be used. This will prompt a penalty, but it’s a good alternative compared to having your robot do nothing at all! Note that during the competition, each team’s robot handler will be standing up (not crouched next to the robot), and if the override button needs to be activated because your robot didn’t start at the whistle sound, then you crouch down to activate your robot’s override.
