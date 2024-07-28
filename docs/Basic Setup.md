- Install ROS Noetic; use ROS Documentation
- Setup sources
```
echo "source /opt/ros/noetic/setup.bash" >> ~/.bashrc
source ~/.bashrc
```

- Clone the package the AutoRC package
```
git clone https://github.com/pamin1/AutoRC.git
```
	- will need to make submodule repositories public for public clone access

- Build and Add Package Source Path
```
cd ~/AutoRC/
catkin build
cd && echo "source AutoRC/devel/setup.bash" >> ~/.bashrc
```


Current Setup uses AprilTag system for testing purposes. This setup will ideally be deprecated soon...
- Install AprilTag(ROS)
```
cd ~/AutoRC/src/
git clone https://github.com/AprilRobotics/apriltag.git
git clone https://github.com/AprilRobotics/apriltag_ros.git
cd ..
rosdep install --from-paths src --ignore-src -r -y 
catkin build
```

- Update the AprilTag Configuration
~/AutoRC/src/apriltag_ros/apriltag_ros/config/tags.yaml
```
standalone_tags:
[
{id: 0, size: 0.11}
]
```

~/AutoRC/src/apriltag_ros/apriltag_ros/config/settings.yaml
```
tag_family: 'tag36h11'
tag_threads: 2 # default: 2
tag_decimate: 1.0 # default: 1.0
tag_blur: 0.0 # default: 0.0
tag_refine_edges: 1 # default: 1
tag_debug: 0 # default: 0
max_hamming_dist: 2
publish_tf: true
transport_hint: "raw"
```

