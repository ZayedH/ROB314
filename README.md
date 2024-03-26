# ROB314

rosrun tello_twist_control tello_twist_control.py cmd_vel:=/tello/cmd_vel

#
cd catkin_ws/

source devel/setup.bash 


rostopic pub /tello/takeoff std_msgs/Empty

rostopic pub /tello/land std_msgs/Empty


roslaunch odom_to_tf_broadcaster odom_to_tf_broadcaster.launch


roslaunch tello_driver tello_node.launch tello_ip:="192.168.10.1"
