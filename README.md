# Main Objective of this Project

This project looks at a potential method for computing a non-thermal dark matter distribution's transfer function T(k) without needing the Boltzmann Hierarchy.
This project does so by first translating a distribution in terms of comoving momentum (q = ap/m) to a distribution in real space (s), where f(s) = f(q(s)) (ds/dq)^-1. 
Then the 3d Fourier transform of said distribution can be taken, however, the theta and phi components may be handled analytically leaving a 1D Fourier transform which must be handled numerically. 
The result of this transform can then be compared to the known transfer functions computing using the Cosmic Linear Anisotropy Solving System (CLASS).


## Files in the Project

- **fourier_simpler.ipynb**: The main Jupyter notebook containing the code for:
  - Setting up and importing required libraries (`numpy`, `matplotlib`, `scipy`).
  - Defining and computing the real space distribution f(s).
  - Performing the Fourier transform.
  - Normalizing the Fourier result to compare with the known transfer function computed from the Boltzmann Hierarchy with CLASS.
  - Plotting and visualizing the results, including comparison with CLASS and Mathematica results.
  - Visualizing the integrand used in the Fourier calculations.

- **Fourier_data_files/**: This folder contains the data files required for the project.
  - `fs_list.file`: y values of f(s) which may be exported for numerical integration in Mathematica.
  - `s_list.file`: x values of f(s) which may be exported for numerical integration in Mathematica.
  - `NEW3_ztest_000_pk.dat`: Matter power spectrum P(k) with a NCDM distribution computed externally with CLASS.
  - `lcdm_ztest_000_pk.dat`: Matter power spectrum P(k) for Lambda-CDM computed externally with CLASS.
  - `mathematica_list`: Result of Fourier transform from numerical integration in Mathematica.


## Project Requirements

To run this notebook, you'll need the following Python packages:
- Python 3.x
- Jupyter Notebook
- numpy
- scipy
- matplotlib
