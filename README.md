# Construct Trajectories from Sensor

## Introduction
The trajectories for Tracking Moving Condition Project are divide into 4 parts. Each part will contain small exercises that guided step by step to build a complete Tracking Trajectories and its components. The application will take measurement value from various sensors (Rate Gyro, Odometers, Inertial Measurement Unit) and applied calculus to re-construct the vehicle's trajectories.

---

### 1. Odometers, Speedometers, and Derivatives

Understanding motion means understanding quantities like position, velocity, and acceleration and how they relate to each other. And it turns out that calculus gives us two incredible tools for understanding these relationships: derivatives and integrals.

In this lesson you will learn about the derivative and what it can tell us about motion. By the end of this lesson you will be able to take a car's odometery data (distance traveled) and use it to infer new knowledge about velocity and acceleration.

<img src="https://github.com/jackyhuynh/Construct_Trajectories_from_Sensor/blob/main/images/odometer2.jpg" width="450" height="300" margin-left:auto margin-right:auto>

#### Navigation Sensors

We will be discussing the following sensors in this course:

- *Odometers* - An odometer measures how far a vehicle has traveled by counting wheel rotations. These are useful for measuring distance traveled (or displacement), but they are susceptible to bias (often caused by changing tire diameter). A "trip odometer" is an odometer that can be manually reset by a vehicle's operator.

- *Inertial Measurement Unit* - An Inertial Measurement Unit (or *IMU*) is used to measure a vehicle's heading, rotation rate, and linear acceleration using magnetometers, rate gyros, and accelerometers. We will discuss these sensors more in the next lesson.

#### Average Speed

To calculate average speed ( V_avg ), you can use the following equation:

```  
    V_avg = Δx/Δt
```

where Δx means "change in position" and Δt means "change in time".

#### Velocity

- Velocity is the instantaneous rate of change of position
- Velocity is the slope of the tangent line of position
- Velocity is the derivative of position

#### Differential Notation

``` 
    f(t)=lim of Δt→0 * { (f(t+Δt)−f(t))/Δt }
```

- This "dot" notation is one of two common ways of representing the derivative.
- Calculus was simultaneously invented by two people: Gottfried Wilhelm Liebniz and Isaac Newton.
- And each came up with his own notation for representing derivatives. The Wikipedia article on [Notation for Differentiation](https://en.wikipedia.org/wiki/Notation_for_differentiation) does a good job of explaining them thoroughly but I will summarize here.	  

##### 0. What Newton and Liebniz share (d/dt)

- In both notations, (d/dt) is an instruction to take the derivative. It means "Take the derivative *with respect* to tt of whatever function shows up to the right."
- When you see something like this: *{df}/{dt}* You should think "the derivative of some function ff with respect to tt"

##### 1. Liebniz Notation (prime)

If some variable yy is a function of xx we can write:

```
    y=f(x)
```

The derivative of yy with respect to xx is given by:

```
    {dy}/{dx} = f'(x) 
```

and this could be spoken as "dee y dee x equals f prime of x"

##### 2. Newton's Notation (dot)

- Newton invented Calculus as a tool to help him understand motion. As a result, he was usually thinking of derivatives with respect to time (not some abstract xx variable).
- Likewise, his functions weren't abstract f(x)f(x)'s and g(f(x))g(f(x))'s. The functions he was interested in actually meant something about the physical world! He wanted to describe:

    position x(t)
    velocity v(t)
    and acceleration a(t)

- And he wanted to capture the relationships between these quantities compactly. So for Newton: differentiation with respect to time is indicated by placing a dot over the variable. So, for example:

```
    v(t)= d/dt * x(t)=  x_dot(t)
```
- or for second derivatives:

```
    a(t)= d/dt * v(t)=  d/dt * x_dot(t) = x_twoDot (t)
```

​*A "Typical" Calculus Problem*
If you’ve taken calculus before you probably have vague recollections of terms like “the chain rule” or “the product rule” or “the quotient rule”... these are all techniques for calculating the derivative of a function when you know the function’s algebraic form. Calculating the derivative of a function is also known as differentiation. And in a typical calculus class you would spend a LOT of time learning how to differentiate various functions…	

---

### 2. Accelerometers, Rate Gyros, and Integrals

Every self driving car has at least one inertial measurement unit in it. These small sensors are able to measure acceleration in three directions as well as rotation rates around all three axes (pitch, roll, and yaw).

But what can we do with this data? In this lesson you'll learn how the integral can be used to accumulate changes in data (and motion).

<img src="https://github.com/jackyhuynh/Construct_Trajectories_from_Sensor/blob/main/images/imu.jpg" width="450" height="300" margin-left:auto margin-right:auto>

#### Differentiation Recap

In the last lesson, you learned about the derivative. This section is just here to remind you of what you learned.

Understanding the Derivative
You saw a few ways to understand the derivative:

1. The "Rate of Change" Interpretation
If f(t) gives the value of a function at any t, then f_dot (t0) gives the instantaneous rate of change of f(t)f(t) at the value t=t_0.

2. The Graphical Interpretation
The slope of the line tangent to f(t) at t=t_0 is f_dot (t0)

3. Acceleration
It can be dangerous to rely on accelerometer data for localization since errors have a tendency to accumulate. This is a weakness of accelerometers.

Fortunately, it takes some time for these errors to accumulate. So when they're used over short time intervals accelerometers can be really helpful.

Take a look at one of Uber's early prototypes of a self driving car:

![img](https://github.com/jackyhuynh/Construct_Trajectories_from_Sensor/blob/main/images/self-driving-uber-prototype-in-san-francisco.jpg)

Look at all those sensors perched on the hood! And you can't even see the IMUs and odometers and GPS sensors inside the vehicle!

Each of these sensors has strengths and weaknesses and each contributes to an improved understanding of the vehicle and it's surroundings. This is where *Sensor fusion* step in.

Sensor fusion is how you use software to stitch together all these disparate data sources into one coherent picture about the vehicle, its motion, and the world around it.

#### Rate Gyro

A car's heading is usually represented by the Greek letter theta: \thetaθ

The angular velocity is the rate of change (derivative) of the heading, so it's represented by "theta dot": θ˙

---
### 3. Two Dimensional Robot Motion and Trigonometry

Required: knowledge about a vehicle's heading and displacement to calculate horizontal and vertical changes in its motion.

<img src="https://github.com/jackyhuynh/Construct_Trajectories_from_Sensor/blob/main/images/vector-components-with-unit-vectors.svg.png" width="450" height="300" margin-left:auto margin-right:auto>

---

### 4. Reconstructing Trajectories
I will use data from sensor to reconstruct Trajectories like this.

<img src="https://github.com/jackyhuynh/Construct_Trajectories_from_Sensor/blob/main/images/example-trajectory.png" width="450" height="300" margin-left:auto margin-right:auto>

---

## Technology
- Python 
- Object Oriented Design
- Jupyter Notebook
- Data Visualization
- Localization
- Data Structures
- Algorithms
- Navigation Sensor
- Speed and Motion theory
- Calculus

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
- There is no download IDE need, all you need is download all the src to your machine and run it. or just open the notebook in GitHub
- Using Jupiter Notebook
- Navigate to the jupiter notebook (.ipynb) an dopen it. Contain will automatic display
- else hit:
```
Ctrl + Enter
```
- The notebook will execute in Markdown form and include the visualization of the map.

## Deployment

The small applications can be deploy and ready to work with any sensor, or moving robotic prediction. Idea for localization and/or GPS application. This is actually what we use for driving direction everyday. According to Sebastian, this technology have been around for 15 years, and still helping human each day.
Please refer to my notebook for a better understanding of implementation.

## Built With

* [Jupyter Notebook](https://jupyter.org/try) 

---
# Odometers, Speedometers, and Derivatives


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

