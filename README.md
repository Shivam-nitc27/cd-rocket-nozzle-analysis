\# 🚀 Convergent-Divergent Rocket Nozzle Analysis



\## 📌 Project Overview

This repository contains thermochemistry analysis using RPA and 2D axisymmetric CFD analysis of convergent-divergent rocket nozzle. The simulation captures the transition from subsonic to supersonic flow, including the formation of shock diamond structures in the exhaust plume.



\## 🧪 RPA Thermochemistry Analysis

Before running the CFD, I performed a thermochemical analysis using Rocket Propulsion Analysis to establish performance targets for the rocket propellant used in CFD. 



\### Performance Targets (Sea Level)

I used the Estimated Delivered values for my CFD analysis, as they account for real-world chemical and kinetic losses.



Setup Values given to RPA



| \*\*Absolute Chamber Pressure ($P\_{c}$)\*\* | 30 bar |

| \*\*Area Ratio for convergent section\*\* | 6.25 | 

| \*\*Area Ratio for divergent section\*\* | 12.25 | 

| \*\*Nozzle Divergent section shape\*\* | Conical nozzle with 15 deg divergent angle |



Result Values obtained from RPA



| Parameter | Theoretical Value (Ideal) | Estimated Value (Delivered) |

| :--- | :--- | :--- | :--- |

| \*\*Effective Exhaust Velocity ($V\_{j}$)\*\* |  2484.951 m/s |  2321.69 m/s |

| \*\*Specific Impulse ($I\_{sp}$)\*\* | 253.39 s | 236.75 s |

| \*\*Thrust Coefficient ($C\_f$)\*\* | 1.4119 | 1.3526 | 



\## 🛠️ Geometry \& Mesh

\* \*\*CAD Design:\*\* Created in Fusion 360 and exported as a universal `.step` file for accessibility.

\* \*\*Mesh Generation:\*\* Developed in ANSYS Meshing with targeted refinement at the throat and walls to capture sonic transition.

\* \*\*Universal Files:\*\* Source geometry is available in the `geometry/` folder as `rocket\_nozzle\_geometry\_universal.step` and source mesh is available in the `mesh/` folder as `rocket\_nozzle\_mesh.msh`



\## ⚙️ Computational Setup

The simulation was conducted in ANSYS Fluent using a density-based transient solver.

\* \*\*Inlet Total Pressure:\*\* 30 bar

\* \*\*Inlet Total Temperature:\*\* 3567.01 K

\* \*\*Turbulence Model:\*\* SST k-omega

\* \*\*Time Step:\*\* $1 \\times 10^{-5}$ s (optimized for convergence stability)



\## 📊 Results \& Observations

\* \*\*Shock Diamonds:\*\* Velocity, Pressure, and density plots clearly show the formation of shock diamonds in the plume, indicating the nozzle's pressure-matching characteristics at sea level.



!\[Velocity Contour](./figures/rocket\_nozzle\_velocity\_contour.png)

!\[Pressure Contour](./figures/rocket\_nozzle\_pressure\_contour.png)

!\[Density Contour](./figures/rocket\_nozzle\_density\_contour.png)

!\[Temperature Contour](./figures/rocket\_nozzle\_temperature\_contour.png)



\## 🧠 Challenges \& Human Insights

\* \*\*Solver Tuning:\*\* Initially, the high pressure at the inlet caused numerical divergence. I solved this by utilizing a smaller time step and a first-order upwind scheme before switching to second-order for final accuracy.

\* \*\*Data Integrity:\*\* I have included the raw `report.xml` and the RPA PDF to provide full transparency of the simulation settings.

