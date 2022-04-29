# Scan Matching Localization

Project goal is to localize a car driving in simulation for at least 170m from the starting position and never exceeding
a distance pose error of 1.2m. The simulation car is equipped with a lidar, provided by the simulator at regular intervals
are lidar scans. There is also a point cloud map map.pcd already available, and by using point registration matching 
between the map and scans localization for the car can be accomplished. This point cloud map has been extracted from the
CARLA simulator.


![Alt text](results/full_drive.png "full drive")

### To get started do the following steps:

### 1. Create build directory

    # mkdir build

### 2. Copy rcplib.tgz archive to the build directory

    # cp rcplib.tgz ./build

### 3. Copy map.pcd and map_loop.pcd to the build directory

    # cp map.pcd ./build
    # cp map_loop.pcd ./build

### 4. Navigate to the build directory

    # cd build

### 5. Unarchive rcplib.tgz archive

    # tar -xvvzf rcplib.tgz

### 6.  Compile the code

    # cmake ../
    # make

### 7. Launch the simulator in one terminal tab

Navigate to the parent directory 

    # ./run-carla.sh

### 8. Run the project code in other terminal tab

In the build directory

    # ./cloud_loc
    