[![License](https://img.shields.io/badge/License-BSD%203--Clause-blue.svg)](https://opensource.org/licenses/BSD-3-Clause)
## ENPM808X ROS BEGINNER TUTORIALS

# TODO
1. Navigating the ROS wiki Tutorial - Complete
2. Navigating the File System Tutorial - Complete
3. Create ROS Package Tutorial - Complete
4. Create beginner_tutorials package - Complete
5. Build ROS package Tutorial - Complete
6. Understanding ROS Nodes Tutorial - Complete
7. Understanding ROS topics Tutorial - Complete
8. Writing a ROS publisher and subscriber - Complete
9. Updated CMakeLists.txt for build
10. Examining Publisher and Subscriber Tutorial - Complete
11. Added custom string message - Complete.
12. Modified the tutorial code to follow Google C++ Style Guide- Complete
13. Added CPPCheck and CPPLint results
14. Added Licence
15. Getting started with roswtf Tutorial - Complete
16. Understanding ROS Services and Parameters Tutorial - Complete
17. Using rqt_console and roslaunch Tutorial - Complete
18. Definined srv file
19. Implemented ROS service to change output of publisher node with logger levels
20. Used rqt_console and rqt_logger_levels

# Overview


Basic ROS Tutorial to create and build a package with a publisher and subscriber. This tutorial can be found here : (http://wiki.ros.org/ROS/Tutorials/WritingPublisherSubscriber%28c%2B%2B%29)

# Dependencies

Make sure the following dependencies are on your system before you clone this repo

    ROS Melodic
    catkin
    Ubuntu 18.04
    C++ 11

To install ROS Melodic:
http://wiki.ros.org/melodic/Installation

To install catkin: 
It gets installed by default alongwith ROS
else:  http://wiki.ros.org/catkin

# Standard install via command-line

    cd <<Your_catkin_workspace>>/src
    mkdir beginner_tutorials
    cd beginner_tutorials
    git clone --recursive https://github.com/sukoonsarin/beginner_tutorials
    cd ../..
    catkin_make
    source devel/setup.bash

## Execution Steps ( Without launch file)
In 3 terminal windows, run the following commands:

**Terminal 1:**

    roscore

**Terminal 2:**

    cd <<Your_catkin_workspace>>
    source devel/setup.bash
    rosrun beginner_tutorials talker

**Terminal 3:**

    cd <<Your_catkin_workspace>>
    source devel/setup.bash
    rosrun beginner_tutorials listener



### Add custom message using rosservice

Execute the files and then open a new terminal and type:
```
cd <<Your_catkin_workspace>>
catkin_make
source devel/setup.bash
rosservice call /UpdateString "Enter-NewString-Here"
```
**Example:**

    rosservice call /UpdateString "Hello ROS!"


After entering the text, you will notice the change in the message. 

### Execution Steps (with launch file)
```
cd <<Your_catkin_workspace>>
catkin_make
source devel/setup.bash
roslaunch beginner_tutorials Week9_HW.launch 
```

### Change Loop Frequency
Launch the file following the commands and then add the frequency parameter at the end:
```
cd <<Your_catkin_workspace>>
source devel/setup.bash
roslaunch beginner_tutorials Week9_HW.launch frequency:=<any integer above zero>
```

**Example:**

    roslaunch beginner_tutorials Week19_HW.launch frequency:=10
