# skeleton_pkg README:
Modified PythonClient example of NatNetSDK 3.1 for skeleton tracking with Motive 2.1. This is a ROS driver/node to publish the skeleton data.

Original example here: https://optitrack.com/products/natnet-sdk/

Edited original example to make a ROS publisher to publish geometry_msgs/PoseArray of the skeleton that I am tracking (upper body markerset. 25 markers). Skeleton is streamed in NatNet as a set of rigid bodies. My skeleton is sent as 13 rigid bodies ( neck, hip, left upper arm, left lower arm, etc). Used NAT_PING in NatNetClient.py-> self.sendCommand() call to receive mo-cap data. 

For your use, edit NatNetClient.py-> skeletonMessage() which is a callback triggered when a rigid body data is received.

# Start a roscore and run-

rosrun skeleton_pkg skeletonMain.py
