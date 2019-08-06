# ros_decawave
Indoor/Outdoor Positioning System based on Decawave's DWM1001 Ultra Wide Band transceivers.

## Dependencies

### Python Dependencies
```
$ pip install serial
$ pip install struct
```

### ROS Dependencies
```
$ apt install ros-kinetic-hector-trajectory-server
```

## Tutorial
### Pre-Setup
Setup the tag and the anchors using the Android app, and connected the tag using an USB cable to PC.

### Download and Compilation
Download this repo into the ros workspace and compile:
```
$ cd src/
$ git clone https://github.com/verlab/JINT2019-Fast_Mobile_Localization.git
$ cd ..
$ catkin_make ## or catkin build
```

### Using
Run the launch:
```
$ roslaunch ros_decawave decawave_driver.launch
```
![system](media/ros_decawave_rviz.png)


### Topics
```
$ rostopic list
/pose # tag position
/rosout
/rosout_agg
/status # anchors status
/syscommand
/tf 
/tf_static
/trajectory # tag path
```

