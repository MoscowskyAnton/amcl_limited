# AMCL limited
This is fork from [original](https://github.com/ros-planning/navigation) ROS repository of navigation stack, but here is removed everything except [AMCL-method](http://wiki.ros.org/amcl).  
AMCL is being changed in a way, that on every step limits of particle can be set.

## New features:
### Services
 - __set_limits__ (amcl/SetLimits) instance relocalization in area with defined x_min, x_max, y_min, y_max, Y_min, Y_max
