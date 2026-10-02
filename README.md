# STRUPHY Cold-Plasma Validation

Computational study of an anisotropy-driven instability in a cold plasma–Vlasov model using the current [STRUPHY](https://github.com/struphy-hub/struphy) structure-preserving simulation framework.

This work is carried out in collaboration with the **Kinetic and Gyrokinetic Models Group, Max Planck Institute for Plasma Physics (IPP), Garching, Germany**, under the guidance of **Dr. Stefan Possanner**, since **July 2026**.

## Overview

The project uses the current STRUPHY implementation to simulate and analyse a one-dimensional hybrid plasma model in which the energetic electron population is treated kinetically and the cold background population is represented by fluid equations.

The simulations combine finite-element field discretisation with kinetic particle dynamics, particle-in-cell coupling, control-variate sampling and structure-preserving time integration. The resulting data are analysed through electromagnetic energy evolution, instability growth and frequency, energetic-particle velocity distributions, energy conservation and (k)-(omega) spectral characteristics.

A 2018 Master's thesis provides the historical numerical benchmark for the study. Its physical and numerical specifications are reconstructed where required and implemented within the current STRUPHY workflow. The purpose is to validate the present numerical implementation against an established reference calculation, while identifying differences arising from model configuration, numerical representation or diagnostic procedures.

## Numerical work

The computational studies include controlled simulations with prescribed electromagnetic perturbations, anisotropic and isotropic energetic-electron populations, varying wavenumber, particle number and finite-element resolution.

Dedicated parameter and post-processing workflows are used to analyse field and particle energy evolution, instability growth and oscillation frequencies, parallel and perpendicular velocity-space redistribution, relative total-energy error, and two-dimensional (k)-(omega) spectra compared with analytical dispersion characteristics.

Particular care is given to reconstructing the historical diagnostic procedures where necessary, including particle-weight normalisation, finite-element field evaluation on the spatial grid and Fourier analysis.

## STRUPHY working branch

The simulations are carried out in the dedicated **`coldplasmaexample`** branch of the upstream STRUPHY repository:

**[STRUPHY — coldplasmaexample](https://github.com/struphy-hub/struphy/tree/coldplasmaexample)**

The relevant working directory is:

`examples/ColdPlasmaVlasov/anisotropic_maxwellian/`

It contains the cold-plasma example together with the parameter files and post-processing developed for the simulation and validation work.

This repository is a research record for my work with the current STRUPHY implementation; the upstream repository remains the authoritative STRUPHY codebase.

## Reference benchmark

**F. Holderied, _Investigation of Finite Element Methods for a 4D Hybrid Plasma Model_, Master's Thesis, Technical University of Munich, 2018.**

The thesis was carried out at the Max Planck Institute for Plasma Physics and provides the historical hybrid-model formulation and numerical benchmark used in this study.

## Research contribution

My work includes translating the benchmark physical and numerical specifications into the current STRUPHY framework, carrying out the simulations, developing dedicated parameter and post-processing workflows, analysing the resulting field and particle data, and investigating discrepancies between the historical and current computational procedures.

The emphasis is on reproducible numerical experiments and on distinguishing differences in simulation setup or diagnostics from differences in the underlying numerical implementation.

## Provenance and licensing

**STRUPHY** is developed collaboratively within the STRUPHY project and is distributed under the **MIT License**. Copyright is attributed in the upstream repository to the STRUPHY developers and the Max Planck Institute for Plasma Physics.

[STRUPHY repository](https://github.com/struphy-hub/struphy) · [MIT License](https://github.com/struphy-hub/struphy/blob/coldplasmaexample/LICENSE)

The 2018 thesis is a separate academic work and remains subject to its own copyright and permissions. It is cited here as the scientific reference for the benchmark and is not represented as part of the STRUPHY software.

Material originating from the upstream STRUPHY project retains its original licensing and attribution. Simulation configurations, post-processing scripts and documentation specifically developed as part of this research are identified as such in the repository history.

## Acknowledgement

This research is carried out with the **Kinetic and Gyrokinetic Models Group, Max Planck Institute for Plasma Physics (IPP), Garching**, under the guidance of **Dr. Stefan Possanner**.

For the numerical framework, please refer to the upstream [STRUPHY project](https://github.com/struphy-hub/struphy).
