# Adaptive Traffic Lights System

[![Python version](https://img.shields.io/badge/python-3.11.3-blue.svg)](https://www.python.org/downloads/release/python-3113/)

<h4>This Adaptive Traffic Signal Timer uses live images from the cameras at traffic junctions for traffic density calculation using YOLO object detection and sets the signal timers accordingly, thus reducing the traffic congestion on roads, providing faster transit to people, and reducing fuel consumption.</h4>

</div>

-----------------------------------------
### Inspiration

* Traffic congestion is becoming one of the critical issues with the increasing population and automobiles in cities. Traffic jams not only cause extra delay and stress for the drivers but also increase fuel consumption and air pollution. 

* According to the International Business Machines Corps Commuter Pain survey (2011), the city roads of Nairobi were ranked fourth most congested in the world. The government of Kenya estimates that traffic jams cost 50 million shillings a day in lost productivity and manned hours in the city. Several factors contribute to the problem of traffic congestion in Nairobi and even other parts of the country, firstly, concentrations of employment in the city center and industrial area. Secondly, the extensive ownership and usage of private automobiles, and last but not least, inadequate road network-carrying capacity.

* People are compelled to spend hours stuck in traffic jams, wasting away their precious time commuting. Current traffic light controllers use a fixed timer and do not adapt according to the real-time traffic on the road.

* In an attempt to reduce traffic congestion, we developed an improved traffic management system in the form of a Computer Vision-based traffic light controller that can autonomously adapt to the traffic situation at the traffic signal. The proposed system sets the green signal time adaptively according to the traffic density at the signal and ensures that the direction with more traffic is allotted a green signal for a longer duration of time as compared to the direction with lesser traffic. 

------------------------------------------
### Implementation Details

This project can be broken down into 3 modules:

1. `Vehicle Detection Module` - This module is responsible for detecting the number of vehicles in the image received as input from the camera. More specifically, it will provide as output the number of vehicles of each vehicle class such as car, bike, bus, truck, and rickshaw.

2. `Signal Switching Algorithm` - This algorithm updates the red, green, and yellow times of all signals. These timers are set bases on the count of vehicles of each class received from the vehicle detection module and several other factors such as the number of lanes, average speed of each class of vehicle, etc. 

3. `Simulation Module` - A simulation is developed from scratch using [Pygame](https://www.pygame.org/news) library to simulate traffic signals and vehicles moving across a traffic intersection.

------------------------------------------
### Demo

* `Vehicle Detection`

<p align="center">
 <img height=400px src="vehicle-detection.png" alt="Vehicle Detection">
</p>

<br> 

* `Signal Switching Algorithm and Simulation`

<p align="center">
    <img src="Demo.gif">
</p>

------------------------------------------
### Prerequisites

1. [Python 3.11.3](https://www.python.org/downloads/release/python-3113/)
2. [Microsoft Visual C++ build tools](http://go.microsoft.com/fwlink/?LinkId=691126&fixForIE=.exe.) (For Windows only)

------------------------------------------
### Installation

* Step I: Clone the Repository
```sh
      $ git clone https://github.com/DanielMbithiMusau/Adaptive-Traffic-Lights.git
```

* Step II: Download the weights file from [here](https://drive.google.com/file/d/1flTehMwmGg-PMEeQCsDS2VWRLGzV6Wdo/view?usp=sharing) and create a bin directory and place it there.

* Step III: Install the required packages
```sh
      # On the terminal, move into the project root directory
      $ pip install -r requirements.txt
      $ python setup.py build_ext --inplace
```

* Step IV: Run the code
```sh
      # To run vehicle detection
      $ python vehicle_detection.py
      
      # To run simulation
      $ python simulation.py
```

------------------------------------------
### Contributors

Daniel Mbithi Musau - [Daniel Mbithi Musau](https://github.com/DanielMbithiMusau)

------------------------------------------
### Acknowledgement

I would like to extend my sincere thanks to my mentor Dr. Lawrence Nderu for his kind help and valuable advice. His support and constant supervision was imperative for the successful completion of this project.
