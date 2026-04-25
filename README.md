# CGI-Tool-Python
A Python tool for calculating the Grid Convergence Index (GCI) and discretization error on structured and unstructured CFD meshes using the Celik et al. methodology.

This tool is specifically designed to handle both**unstructured meshes** and **structured meshes**, where enforcing a perfectly uniform refinement ratio between grids is unpractical.

## Methodology
This script strictly follows the widely accepted methodology proposed by **Celik et al. (2008)** in the *Journal of Fluids Engineering*: ["Procedure for Estimation and Reporting of Uncertainty Due to Discretization in CFD Applications."](https://doi.org/10.1115/1.2960953)

## Key Features:
* Handles Non-Uniform Refinement: Automatically calculates characteristic lengths based on cell counts ($N$) and solves the transcendental equation for the apparent order of convergence ($p$) using a fixed-point iteration loop.

* Dimensional Awareness: Calculates characteristic grid sizes correctly for both 2D ($1/\sqrt{N}$) and 3D ($1/N^{1/3}$) domains.

* Asymptotic Range Verification: Calculates GCI for both the coarse and fine grids to verify if the solutions fall within the asymptotic range of convergence.

* Automated Plotting: Generates standard CFD convergence plots featuring the CFD results, the Richardson Extrapolated value ($h \rightarrow 0$), and the computed GCI error bar.

## ⚙️ Requirements
* Python 3.x
* NumPy
* Matplotlib
