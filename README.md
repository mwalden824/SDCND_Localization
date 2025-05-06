# 3D Car Localization via Sequential Laser Scan Matching

## 🧭 Introduction

This project focuses on localizing a self-driving car in 3D space using only scan matching with sequential LiDAR (laser) scans. Instead of relying on GPS or other external sensors, the system estimates the car's trajectory by matching each incoming laser scan with the previous ones, using scan-matching algorithms. The approach leverages techniques such as Iterative Closest Point (ICP) and NDT to incrementally build the trajectory of the vehicle over time with each new processed lidar scan.

## ⚙️ Setup and Run

### Prerequisites

- Carla Simulator 

### Installation

Clone the repository:

```bash
git clone https://github.com/mwalden824/SDCND_Localization.git
cd SDCND_Localization
```

## Instructions to Execute the Project

1. Review the starter files. You must find the following files in your current working directory.
    ```bash
    .
    ├── CMakeLists.txt
    ├── README.md
    ├── c3-main.cpp
    ├── helper.cpp
    ├── helper.h
    ├── make-libcarla-install.sh
    ├── map.pcd
    ├── map_loop.pcd
    ├── rpclib
    └── run_carla.sh
    ```


2. Ensure that the **libcarla-install/** folder is present in your current working directory. This folder contains the static binaries built for the target VM workspace environment. You will need to regenerate it using the following commands in order:
    ```bash
    chmod +x make-libcarla-install.sh
    ./make-libcarla-install.sh
    ```

3. Compile the project using the following commands. 

    ```bash
    cmake .
    make
    ```
    These steps will generate the **clooud_loc** executable. 

4. Open a new Terminal tab and execute the following command to start the simulator.

    ```bash
    ./run_carla.sh
    ```  

5. Open another Terminal tab and execute the following to run the project.
    ```bash
    ./cloud_loc 
    ```
If you encounter core dump on start up, just rerun and try again. Crash doesn't happen more than a couple of times. 



Here is a glimpse of the running project.

![a glimpse of the running project](L7_Project.png)