# ECE 5340 - Final Project
## Project Requirements
To receive any points the following must be done:
    A Readme.md file must be submitted on canvas. It must explain the following:
        How to compile / setup the code (all dependencies, etc.)
        How to download the code
        How to run the code
    Code must compile and run with instructions provided
    All code you develop must exist in the class gitlab student group namespace.
    A writeup on the project must be turned in using pdf format. Details of the writeup are described in "Project Points"
    The robot must continuously update a plan based on sensor data and an updated occupancy grid (the occupancy grid must be populated from sensor data and not preloaded).

## Project points

The project will be scored based on the elements that you choose to include. For each element that you choose, you must have a section in the project pdf providing an explanation of how the element was implemented and where it can be found in the code (if applicable).

Note that the list below adds up to more than 100 points. This gives you the option to pick and choose different elements. I will give you a total of up to 120 points if you earn them (i.e., anything beyond 120 that you implement is purely for your educational benefit).
   * Basic sim abilities
        (15 points) Implemented in C++/Python and uses ROS
        (5 points) Turn in a .rosinstall file which can be used with wstool to make a workspace that runs the code
        (5 points) A single launch file can be called to run the entire sim
        (10 points) Ability to click on the GUI to choose a new destination for the robot. Describe how to do so in the writeup.
        (10 points) Runs using Gazebo without getting stuck. Describe how to run Gazebo in the writeup.
        (5 points) Adaptable look ahead horizon. Describe how it is used in the planning architecture in the writeup and how it is adjusted while the robot it moving.
   * Coordinate systems
        (5 points) A coordinate transform is performed in the simulation. In the writeup you must explain where in the code the transform is performed and what purpose it serves. No points will be given for transforms that are performed for no reason.
   * Planning capability
        (20 points) Create an a-star planner that can be used to plan for the robot. Explain how to configure the sim to run the a-star planner.
        (20 points) Create a sample-based planner that can be used to plan for the robot. Explain how to configure the sim to run the a-star planner. Explain what sample-based planner was implemented.
        (20 points) Implement an alternative planner that can be used to plan for the robot. Explain how to configure the sim to run the alternative planner. Explain the planner in detail.
   * Control capability
        (20 points) Implement a reference following control law. This will require using a planning method that produces smooth plans or smoothing the plan afterwards.
        (20 points) Implement vector field techniques to aid in the following of the plan (must be more than a simple go-to-goal vector field)
        (10 points) Implement an input/output control

## Early submission

Early submissions must be turned in by Monday December 13 with an email sent to the professor stating that you are expecting early evaluation. Early evaluations will be given back by the end of the day on Tuesday, December 14.
