# AMCL limited
This is fork from [original](https://github.com/ros-planning/navigation) ROS repository of navigation stack, but here is removed everything except [AMCL-method](http://wiki.ros.org/amcl).  
AMCL is being changed in a way, that on every step limits of particle can be set.

Limits are set as min and max values of x, y and yaw variables. Such set of variables can be repeated as much as needed. When global localization is called, particles can appear only inside of this sets. Also when resapling is done for filter, new particles also will appear inside of this sets. Probability of appeariance is depend of areas cumulative size.  
Now started limit contains full map size for x and y and \[-pi, pi] range for yaw.

- [x] multi-interval limits
- [x] start limits obtained from map
- [ ] start limits can be set through params
- [x] global localiazation in limits
- [x] resampling in limits
- [x] limits visualization in rViz
- [x] validating particles in limits by map obstacles
- [ ] not allow particles leave limits during motion
- [ ] start position and set 2d pose - must use limits?

### new services 
 - __~set_limits__ (amcl/SetLimits) service to set limits

### new topics
 - __~limits__ (visualization_msgs/Marker) visualization of limits for rViz
