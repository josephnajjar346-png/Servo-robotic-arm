# Servo-Controlled Robotic Arm (3DOF)
Designed and implemented a 3DOF servo-driven robotic arm using Arduino. Implemented calibrated position control and inverse kinematics to compute joint angles for defined end-effector positions.

## Key Features
- 3DOF servo-driven robotic arm
- Precomputed waypoint trajectory execution
- Exponential smoothing for stable convergence
- Angular rate limiting to reduce jerk
- Serial command interface for motion control

## System Overview
This project controls a three-servo robotic arm and executes a predefined 10 cm straight vertical descent using precomputed joint-angle waypoints.

The arm:
- Initialises to calibrated zero positions
- Accepts serial commands for motion control
- Executes a smooth 11-point vertical trajectory (200 mm → 100 mm)
- Uses smoothing and rate limiting to reduce jerk and overshoot

## Serial Commands
- `1` → Move to start position (z = 200 mm)
- `2` → Execute full 10 cm vertical descent
- `90` → Return to zero position

## Control Strategy
- Waypoint-based joint angle trajectory
- Exponential smoothing for gradual convergence
- Maximum step limiting to constrain angular velocity
- Pulse-width mapping from radians to calibrated microseconds

## System Architecture
