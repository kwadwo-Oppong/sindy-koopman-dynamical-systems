# SINDy & Koopman Operator for Dynamical Systems Analysis
This project delves into the exciting world of **dynamical systems**, focusing on identifying the underlying Ordinary Differential Equations (ODEs) from observed trajectories and analyzing their behavior using advanced techniques like the **Koopman operator and Sparse Identification of Nonlinear Dynamics (SINDy)**.

## Project Overview
Our goal is to reverse-engineer a continuous dynamical system from its trajectory and velocity data. We'll then use the powerful framework of the Koopman operator to linearize the nonlinear dynamics in an extended function space, enabling us to understand and predict system behavior through its eigenvalues and eigenfunctions.

## Project Objectives
This repository contains the code and analysis to achieve the following:
- **ODE Reconstruction with SINDy**: Identify the unknown polynomials $P(x,y)$ and $Q(x,y)$ that define the continuous dynamical system $\dot{x} = P(x,y)$, $\dot{y} = Q(x,y)$, where  $P$ and $Q$ are of degree no more than 3. We'll enforce sparsity by setting small coefficients ($<10^{-5}$) to zero.
- **Trajectory Generation**: Use the Euler method to simulate trajectories from the reconstructed ODE.
- **Koopman Operator Approximation**: Construct an approximation K of the Koopman operator for the ODE in a basis of monomials up to degree 5, ensuring its determinant falls within a specified range ($10^{-5} < det(K) < 10^{5}$).
- **Eigenvalue Analysis**: Compute and visualize the eigenvalues of the Koopman matrix $K$ on the complex plane.
- **Eigenfunction Reconstruction**: Reconstruct and plot the eigenfunctions of the Koopman operator corresponding to real eigenvalues using contour plots.
- **Phase Portrait Analysis**: Simulate trajectories of randomly chosen points and identify eigenfunctions whose contour plots resemble the system's phase portrait.

## Data
The analysis is based on two datasets:
- `xy.txt`: Contains the trajectory (position) data points.
- `xydot.txt`: Contains the corresponding velocity vectors.

## Deliverables
Upon running the analysis, the project will output:
- A plot of the **original vector field**.
- The list of **coefficients for the polynomials $P$ and $Q$**.
- The **determinant of the Koopman matrix K**, the **absolute values of its eigenvalues**, and a **scatter plot of the eigenvalues** on the complex plane.
- **Contour plots of the eigenfunctions** and Koopman modes corresponding to the real eigenvalues.
- A **scatter plot of trajectories for 50 randomly chosen points**.
- The **coefficients of the eigenfunction(s)** whose contour plot(s) best resemble the system's phase portrait.


 
 
