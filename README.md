# Sheet Fall Simulation

If you want to review/see the code, open the `sheet_fall.txt` file.

To run the simulation, download the `sheet_fall.mlx` file and run it in MATLAB.

The project report latex source file can be viewed using `sheet_fall_report.zip` file.

# Numerical Simulation of a Freely Falling Rectangular Plastic Sheet

## Project Overview

Project Overview

This project focuses on the numerical simulation of the free fall of a thin rectangular plastic sheet using MATLAB. The simulation framework was designed to capture both translational motion (linear displacement under external forces) and rotational motion (tumbling and angular displacement), thereby providing a comprehensive model of the sheet’s dynamics.

The forces incorporated into the model include:

Gravity, driving the downward motion.

Buoyancy, accounting for the displaced air volume.

Aerodynamic drag, opposing the direction of relative motion.

Lift forces, acting perpendicular to the relative airflow and strongly influencing orientation.

To analyze the motion, we applied Euler’s method for numerical integration, updating position, velocity, orientation, and angular velocity in discrete time steps. Additionally, a custom rotation matrix based on Euler angles (yaw, pitch, roll) was implemented to continuously update the orientation of the sheet in three-dimensional space. This allowed accurate calculation of projected areas and aerodynamic forces at each step.

The project integrates both mathematical modeling and visualization techniques. MATLAB’s 3D patch and quiver objects were used to represent the sheet and its velocity vector, offering an intuitive understanding of the trajectory and orientation changes during the fall. The simulation output was further validated through time-series plots of velocity, force variations, Reynolds number, and angular motion.

The study of such motion is particularly relevant to fluid dynamics, aerospace engineering, and the study of chaotic systems, where objects with large surface-area-to-mass ratios demonstrate complex, non-linear trajectories. By combining theoretical force models with computational simulation, this project highlights how even simple geometries can exhibit intricate falling behavior due to coupled translational and rotational dynamics.

This simulation provides a realistic and visual understanding of thin-body aerodynamics, with potential applications in aerospace design, material sciences, and environmental studies such as the motion of leaves, debris, and lightweight structures.

## Methodology

* Considered forces: Gravity, Buoyancy, Aerodynamic Drag, and Lift.
* Rotational dynamics modeled using Euler angles (yaw, pitch, roll).
* Numerical integration implemented through Euler’s method for updating velocity, position, and angular orientation.
* Visualization:

  * Patch objects used to represent the sheet in 3D.
  * Quiver plots used to indicate velocity magnitude and direction.

## Results and Discussion

* The sheet follows a non-linear, tumbling trajectory rather than falling vertically.
* Drag reduces vertical velocity, while lift and orientation introduce horizontal displacement.
* The Reynolds number increases over time, reflecting transition toward turbulent flow.
* Simulation results align with expected physical behavior, showing downward acceleration, horizontal drift, and rotational motion.

## Implementation

* MATLAB used as the primary tool for simulation and visualization.
* Euler integration applied for clarity, though `ode45` is noted as a more accurate alternative.
* Outputs generated include:

  * Position and velocity vs time
  * Drag and lift variation
  * Reynolds number vs time
  * Orientation and angular velocity profiles


## Repository Structure

```
├── main.m              # MATLAB simulation script
├── functions/          # Helper functions (rotation, force calculations)
├── results/            # Simulation outputs (plots, graphs, animations)
├── report/             # Project report (PDF)
└── media/              # Screenshots and demo files
```

## How to Run

1. Clone the repository:

   ```bash
   git clone https://github.com/Parthsg07/fall_reconstruction.git
   cd fall_reconstruction
   ```
2. Open `main.m` in MATLAB.
3. Run the script to view the simulation.


## Demonstrations

* [Simulation Video](https://drive.google.com/file/d/1vzIcBk4iMInSkBwa29zoJhYEqewebG7Q/view?usp=sharing)
* [Full Report (PDF)](./report/sheet_fall_report.pdf)

## Contributors

* Aryan Sambare
* Krunal Baraskar
* Tushar Shrivastav
* Parth Ganjewar

## References

1. Anderson, J. D. *Fundamentals of Aerodynamics*. McGraw-Hill, 2010.
2. Hibbeler, R. C. *Engineering Mechanics: Dynamics*. Pearson, 2017.
3. MATLAB Documentation, 2023.
