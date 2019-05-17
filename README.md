# skeleton_pkg
Modified PythonClient example of NatNetSDK 3.1 for skeleton tracking with Motive 2.1 to make a ROS driver to publish the skeleton data.

Original example here: https://optitrack.com/products/natnet-sdk/

Edited original example to make a ROS publisher to publish geometry_msgs/PoseArray of the skeleton that I am tracking (upper body markerset. 25 markers). Skeleton is streamed in NatNet as a set of rigid bodies. My skeleton is sent as 13 rigid bodies ( neck, hip, left upper arm, left lower arm, etc)

Use NAT_PING in NatNetClient.py-> self.sendCommand() call to receive mo-cap data. 
