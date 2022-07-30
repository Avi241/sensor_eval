# A package for Sensor Evaluation sensors available are 

1. 2D Lidar (RP Lidar A1M8)
2. Visual Camera (Loigitech HD Webcam)


# Install dependencies 
```
sudo apt-get install ros-melodic-rplidar
sudo apt-get install ros-melodic-uvc-camera
```

# Check the video port of the camera in your laptop (/dev/video0 or /dev/video1 or whatever it is just do "ls /dev/ " )
change the file start.launch accoordig to your video port 

# Usage

## clone this repo into your catkin_ws/src 
```
cd ~/catkin_ws/src
git clone https://github.com/Avi241/sensor_eval
```

## Compile the package
```
cd ~/catkin_ws
catkin_make
source devel/setup.bash
```

## Connect the RP lidar and Camera and Start the nodes 
```
roslaunch sensor_eval start.launch
```

## Start recordings
```
rosbag record -a -O Sensor.bag
```

