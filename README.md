# ECE5340 - Final Project

## How to download the code

All code (excluding dependencies) can be found in my student group folder titled `pollock_joe/ece5345-final-project`. The following links will provide you direct access to the code:
  * SSH: `git@gitlab.com:utahstate/5345-mobilie-robotics/2021/student_groups/pollock_joe/final_project.git`
  * HTTPS: `https://gitlab.com/utahstate/5345-mobilie-robotics/2021/student_groups/pollock_joe/final_project.git`
  
To download the code, including the dependencies, you may utilize the provided `basic.rosinstall` file and the wstool Command-Line Interface (CLI) tool. If you have not already installed Wstool, click [here](http://wiki.ros.org/wstool "wstool - ROS Wiki") for a tutorial on how to download and set-up Wstool. Once you have downloaded Wstool, you may continue.

The following steps allow you to download the code for this project (code blocks followed by "Type:" can be typed directly into the CLI):

  * Setting up directories:
    1. Locate the directory you would like to place the root directory of my code and its dependencies. This location is completely up to you.
    2. Make a directory for the root of my project: Type: `mkdir -p pollock_joe_final_project`
    3. Change your directory to the newly created directory: Type: `cd pollock_joe_final_project`
    4. Make a directory for the source files of my project and its dependencies (this directory must be named src): Type: `mkdir -p src`
    5. Change your directory to the newly created src directory: Type: `cd src`
    6. Place the provided basic.rosinstall file in the src directory.
  
  * Now you will begin using the wstool CLI tool.
  
    7. Type: `wstool init` to initialize the src directory
    8. Type: `wstool merge basic.rosinstall` to merge the basic.rosinstall file into the workspace.
    9. Type: `wstool up` to begin downloading all the directories and files necessary to run my final project. Note: This `basic.rosinstall` file utilizes SSH. If the `basic.rosinstall` file does not work, you need to set-up SSH as described on the last slide of `02 Files Launch and Workspaces.pptx` in the File section of the ECE 5345 Canvas page.

After the process from previous step has completed, you should have all the required code to move on to the next step.
  

## How to compile / set-up the code (all dependencies, etc.)

To compile the code, we are going to use the ROS CLI tool called `catkin_make`. Follow these steps to compile the code:
  1. Make sure you are still in the `src` directory from the previous steps.
  2. Type: `cd ..` to change your directory to the final project root directory (which is directly above the `src` directory).
  3. Type: `catkin_make` to compile all of the code located in the `src` directory.
  
After the process from the previous step has completed, you have successfully compiled all the required code to move on to the next step.

## How to run the code

To run the code, we are going to continue to use the CLI tools provided by ROS. Follow these steps to run the code:

  1. Source your directory if you haven't already. Type `source devel/setup.bash` and press enter.
  2. Type: `roslaunch astar go_to_goal.launch` and press enter.
  3. If you wish to reconfigure the dynamically reconfigurable parameter (look ahead), then type: `rosrun rqt_reconfigure rqt_reconfigure` in another terminal after sourcing your directory in that terminal as well. Whenever you source your directory, always make sure you are in the root directory of your workspace.
  4. Begin running and manipulating the gui as described in the Final Project Documentation.
