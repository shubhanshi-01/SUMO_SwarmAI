# SUMO Traffic Simulation Project

This project contains a **SUMO (Simulation of Urban Mobility)** traffic simulation using **Swarm Intelligence** techniques, such as **Ant Colony Optimization (ACO)**, to optimize vehicle routes and traffic light timings. The repository includes the necessary SUMO configuration files and a Jupyter notebook that demonstrates how to use TraCI (Traffic Control Interface) to interact with SUMO for dynamic traffic management.

## Table of Contents
- [Project Overview](#project-overview)
- [Features](#features)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Running the Simulation](#running-the-simulation)
- [Configuration Files](#configuration-files)

## Project Overview
The goal of this project is to simulate traffic flow in an urban environment using **SUMO**. Vehicles dynamically adjust their routes based on real-time traffic conditions using **Ant Colony Optimization (ACO)**, and traffic lights adapt their green-light timings based on the number of vehicles at intersections, leveraging **Swarm Intelligence** principles.

## Features
- **Dynamic vehicle routing** using Ant Colony Optimization (ACO).
- **Real-time traffic light control** based on vehicle queues at intersections.
- Simulation visualization using SUMO-GUI.
- Python integration with SUMO via TraCI for interactive control.

## Project Structure
```bash
├── config/
│   ├── myconfis.sumocfg              # Main SUMO configuration file
│   ├── network.net.xml               # SUMO road network file
│   ├── routes.rou.xml                # Vehicle routes file
├── sumo.ipynb                        # Jupyter notebook for running the simulation
└── README.md    

```



- **`config/`**: Contains the configuration files needed for the SUMO simulation, including the road network and vehicle routes.
- **`sumo.ipynb`**: Jupyter notebook that runs the SUMO simulation and applies swarm intelligence techniques for dynamic traffic control.

## Installation

Follow these steps to set up and run the simulation on your local machine:

### 1. Install SUMO
- Download and install **SUMO** from the [official website](https://sumo.dlr.de/docs/Downloads.php).
- Ensure that **TraCI** (Traffic Control Interface) is installed alongside SUMO.

### 2. Install Required Python Libraries
Install the necessary Python libraries by running the following:

```bash
pip install numpy pandas sklearn traci matplotlib

```
### 3. Clone the repository
Clone this repository to your local machine:
```bash
git clone https://github.com/your-username/sumo-traffic-simulation.git
cd sumo-traffic-simulation

```

## Running The Simulation

### 1. Open Jupyter notebook
Start Jupyter Notebook and open the sumo.ipynb file:
```bash
jupyter notebook sumo.ipynb
```
### 2. Run the Simulation

- Make sure your SUMO binary is correctly set in the notebook.
- Run the cells in the notebook to start the simulation. The notebook will:
- Start SUMO with the given configuration files.
- Dynamically adjust vehicle routes and traffic light timings using the ACO and Swarm Intelligence algorithms.

### 3. View Simulation
 If you're using sumo-gui, you can visually observe the simulation and how vehicles adapt their routes and how traffic lights are controlled in real-time.

 ## Configuration Files
**myconfis.sumocfg:**
This is the main configuration file that ties together the road network (network.net.xml) and the routes (routes.rou.xml). You can modify this file to include different parameters for your simulation.

**network.net.xml:**
This file defines the road network used in the simulation, including intersections, lanes, and edges.

**routes.rou.xml:**
This file specifies the vehicle routes, including the number of vehicles and their starting and destination points.