
# Getting started

The robot uses ROS (Robot Operating System). Read the [ROS wiki!](http://wiki.ros.org/).

## What is ROS? ([From the wiki](http://wiki.ros.org/ROS/Introduction))

ROS is an open-source, meta-operating system for your robot. It provides the services you would expect from an operating system, including hardware abstraction, low-level device control, implementation of commonly-used functionality, message-passing between processes, and package management. It also provides tools and libraries for obtaining, building, writing, and running code across multiple computers. ROS is similar in some respects to 'robot frameworks,' such as Player, YARP, Orocos, CARMEN, Orca, MOOS, and Microsoft Robotics Studio.

The ROS runtime "graph" is a peer-to-peer network of processes (potentially distributed across machines) that are loosely coupled using the ROS communication infrastructure. ROS implements several different styles of communication, including synchronous RPC-style communication over services, asynchronous streaming of data over topics, and storage of data on a Parameter Server. These are explained in greater detail in our Conceptual Overview.

## The Robot

The robot uses dynamixel servos. Servos are controlled via the `dynamixel workbench` ROS node. Therefore,
all nodes that wish to drive servos must publish message to the `/inmoov/joint_trajectory` topic. See the diagram below and the servo joint configuration: [config/dynamixel.yaml](./config/dynamixel.yaml)

![](img/overview.png)

## Project structure

* src - all packages (3rd party and ours)
* config - servo configuration
* launch - robot launch files

## Servo Table

**Todo Add servo configurations here: max angle, max velocity, etc. Servos can be configured using dynamixel wizard**

| Servo ID | Model | Joint                |     |     |
| -------- | ----- | -------------------- | --- | --- |
| 1        | XL430 | Head tilt right-side |     |     |
| 2        | XL430 | Head tilt up/down    |     |     |
| 3        | XL430 | Head tilt left-side  |     |     |
| 4        | XL430 | Head turn left/right |     |     |

**Note: head tilt range of motion is poor**

**Note: servo angle limits are not configured**

## Next

1. See [Development](./docs/DEVELOPMENT.md)
2. See [Getting started](./docs/GETTING-STARTED.md)
