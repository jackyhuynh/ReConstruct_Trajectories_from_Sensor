# Construct Trajectories from Sensor

## Introduction
The trajectories for Tracking Moving Condition
Project are divide into 4 parts:

### 1. Odometers, Speedometers, and Derivatives

Understanding motion means understanding quantities like position, velocity, and acceleration and how they relate to each other. And it turns out that calculus gives us two incredible tools for understanding these relationships: derivatives and integrals.

In this lesson you will learn about the derivative and what it can tell us about motion. By the end of this lesson you will be able to take a car's odometery data (distance traveled) and use it to infer new knowledge about velocity and acceleration.

<img src="https://github.com/jackyhuynh/Construct_Trajectories_from_Sensor/blob/main/images/odometer2.jpg" width="450" height="300" margin-left:auto margin-right:auto>

### 2. Accelerometers, Rate Gyros, and Integrals

Every self driving car has at least one inertial measurement unit in it. These small sensors are able to measure acceleration in three directions as well as rotation rates around all three axes (pitch, roll, and yaw).

But what can we do with this data? In this lesson you'll learn how the integral can be used to accumulate changes in data (and motion).

<img src="https://github.com/jackyhuynh/Construct_Trajectories_from_Sensor/blob/main/images/imu.jpg" width="450" height="300" margin-left:auto margin-right:auto>

### 3. Two Dimensional Robot Motion and Trigonometry

Required: knowledge about a vehicle's heading and displacement to calculate horizontal and vertical changes in its motion.

<img src="https://github.com/jackyhuynh/Construct_Trajectories_from_Sensor/blob/main/images/vector-components-with-unit-vectors.svg.png" width="450" height="300" margin-left:auto margin-right:auto>

### 4. Reconstructing Trajectories
In the (optional) final project for this course you will use data like this.

timestamp | displacement | yaw_rate | acceleration
0.0	        0	            0.0	        0.0
0.25	    0.0	            0.0	        19.6
0.5	        1.225	        0.0	        19.6
0.75	    3.675	        0.0	        19.6
1.0	        7.35	        0.0	        19.6
1.25	    12.25	        0.0	        0.0
1.5	        17.15	        -2.829	    0.0
1.75	    22.05	        -2.829	    0.0
2.0	        26.95	        -2.829	    0.0
2.25	    31.85	        -2.829	    0.0
2.5	        36.75	        -2.829	    0.0
to reconstruct plots of the vehicle's trajectory like this:

<img src="https://github.com/jackyhuynh/Construct_Trajectories_from_Sensor/blob/main/images/vector-components-with-unit-vectors.svg.png" width="450" height="300" margin-left:auto margin-right:auto>

## Technology
- Python 
- Object Oriented Design
- Jupyter Notebook
- Data Visualization
- Localization
- Data Structures
- Algorithms

## Getting Started
These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.

### Prerequisites
What things you need to install the software and how to install them
- Jupyter Notebook: If you want just test the code, simply go to google and search for jupiter notebook or another Python online IDE. The Jupyter Notebook is an open-source web application that allows you to create and share documents that contain live code, equations, visualizations and narrative text. 
- Anacoda Navigator: Install Anaconda Navigator if you want to develop data sciences using python or R. Anaconda Navigator is a desktop graphical user interface included in Anaconda that allows you to launch applications and easily manage conda packages, environments and channels without the need to use command line commands. 

### Installing

A step by step series of examples that tell you how to get a development enviroment running

* [Install Anacoda Navigator](https://docs.anaconda.com/anaconda/navigator/install/#:~:text=Installing%20Navigator%20Navigator%20is%20automatically%20installed%20when%20you,install%20anaconda-navigator.%20To%20start%20Navigator,%20see%20Getting%20Started.) - If you haven't downloaded and installed Anacoda Navigator yet, here's how to get started.
* [Jupyter Notebook](https://jupyter.org/try) - Click here to go to the online free Jupiter Notebook.


## Running the tests

Explain how to run the automated tests for this system:
- There is no download IDE need, all you need is download all the src to your machine and run it.
- Using Jupiter Notebook
- Navigate to the file .ipynb
- hit:

```
Ctrl + Enter
```
- The notebook will execute in Markdown form and include the visualization of the map.

![alt](https://github.com/jackyhuynh/Route-Planner/blob/main/src/picture/map.PNG)

- The program was working perfectly fine when I code it in the Udacity.com workspace. You may try it [here](https://classroom.udacity.com/nanodegrees/nd113/parts/ff875ac7-e7c7-40ec-8a79-8fce37d93bb2/modules/e3ba7f5e-56e5-4a40-9b21-0f7a130d3074/lessons/b1e11f40-418c-4292-af6f-56ac2603e868/concepts/498d1011-019d-4768-bd46-f476b68c2c4b) if you are member of Udacity. 

## Deployment

Route PLanner class can be deploy and ready to work with any sensor, or moving robotic prediction. Idea for localization and/or GPS application. This is actually what we use for driving direction everyday. According to Sebastian, this technology have been around for 15 years, and still helping human each day.
Please refer to my notebook for a better understanding of implementation.

## Built With

* [Jupyter Notebook](https://jupyter.org/try) 

## Contributing

Please read [CONTRIBUTING.md](https://gist.github.com/PurpleBooth/b24679402957c63ec426) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags). 

## Authors

* **Truc Huynh** - *Initial work* - [TrucDev](https://github.com/jackyhuynh)

## Format
my README.md format was retrieved from
* **Billie Thompson** - *Initial work* - [PurpleBooth](https://github.com/PurpleBooth)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Udacity.com for design an outstanding program for Students.

