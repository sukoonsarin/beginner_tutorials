[![License](https://img.shields.io/badge/License-BSD%203--Clause-blue.svg)](https://opensource.org/licenses/BSD-3-Clause)
# Beginner Tutorials

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

# Overview

Basic ROS Tutorial to create and build a package with a publisher and subscriber. This tutorial can be found here : (http://wiki.ros.org/ROS/Tutorials/WritingPublisherSubscriber%28c%2B%2B%29)

# Dependencies

Make sure the following dependencies are on your system before you clone this repo

    ROS Melodic
    catkin
    Ubuntu 18.04
    C++ 11

# Standard install via command-line

    cd <<Your_catkin_workspace>>/src
    mkdir beginner_tutorials
    cd beginner_tutorials
    git clone --recursive https://github.com/sukoonsarin/beginner_tutorials
    cd ../..
    catkin_make

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

