# Servo-Controlled Robotic Arm (3DOF)
Designed and programmed a 3DOF robotic arm using Arduino and servo motors. Implemented calibrated position control and inverse kinematics to compute joint angles for defined end-effector positions.

## System Overview
This project controls a three-servo robotic arm and executes a predefined 10 cm straight vertical descent using precomputed joint-angle waypoints.

The arm:
- Initialises to calibrated zero positions
- Accepts serial commands for motion control
- Executes a smooth 11-point vertical trajectory (200 mm → 100 mm)
- Uses smoothing and rate limiting to reduce jerk and overshoot

## Control Strategy
- Waypoint-based joint angle trajectory
- Exponential smoothing for gradual convergence
- Maximum step limiting to constrain angular velocity
- Pulse-width mapping from radians to calibrated microseconds
