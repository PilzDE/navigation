# Navigation
Configuration storage for all mobile robots we are currently using

# Currently Supported Robots

## Neobotix MP-400
`export ROBOT=neobotix`
Our MP-400 that previously had a PRBT on top (and was known as MM-400).

## Volksbot
`export ROBOT=volksbot`
Our Volksbot which is probably similar to Volksbot RT 3.

# Provided launchfiles

## SLAM
Run 
```
roslaunch pilz_navigation slam.launch
```

When your are done mapping run in `pilz_navigation/maps/`
```
rosrun map_server map_saver -f <NAME_OF_MAP>
```

## Basic Navigation
This launchfile starts all that is needed to autonomously navigate the robots to a point.
```
export ROBOT=<MY_ROBOT>
export MAP=<NAME_OF_MAP>
roslaunch pilz_navigation navigation.launch
```
