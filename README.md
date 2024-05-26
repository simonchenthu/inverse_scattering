# Inverse Scattering with Husimi Data

The source code for the paper [S. Chen, Z. Ding, Q. Li, L. Zepeda-Núñez. High-frequency limit of the inverse scattering problem: asymptotic convergence from inverse Helmholtz to inverse Liouville. SIAM Journal of Imaging Science 16.1 (2023), pp. 111–143.](https://epubs.siam.org/doi/10.1137/22M147075X).

Self contained, Light-weight code for solving the inverse scattering problem with Husimi data via optimization based methods.

This repo contains all the necessary code to simulate time-harmonic wave propagation using finite differences and Lippmann-Schwinger solver in Matlab. 

In addition, we provide a simple mean squared misfit against a reference Husimi data, and its derivatives using adjoint-state methods. 

For the reconstruction, the fminunc (quasi-newton) is as an optimization routine.

## Organization

- `src`: contains all the wave propagation and misfit sub routines
- `Husimi`: contains the scripts showcasing the inversion algorithms

The run time could be between several minutes to several hours depending on the parameters, e.g., the wavenumber, the dataset size and the tolerance in iteration.

## Instructions for use

The instructions for running each case are as follows.

- Reconstruction using Husimi data (Lippmann-Schwinger as reference and finite difference as inversion): Run `FWI_husimi_LS.m`, `FWI_husimi_LS_delocalized.m` and `FWI_husimi_LS_SheppLogan.m` for different media.
- Reconstruction using Husimi data (finite difference as reference and inversion): Run `FWI_husimi_FD.m`, `FWI_husimi_FD_delocalized.m` and `FWI_husimi_FD_SheppLogan.m` for different media.
- Reconstruction using plane wave and near field data (finite difference as reference and inversion): Run `FWI_FD.m`, `FWI_FD_delocalized.m` and `FWI_FD_SheppLogan.m` for different media.

## Cite this work

If you use this code for academic research, you are encouraged to cite the following paper:

```
@article{ChDiLiZe:2022high,
  title={High-frequency limit of the inverse scattering problem: Asymptotic convergence from inverse Helmholtz to inverse Liouville},
  author={Chen, Shi and Ding, Zhiyan and Li, Qin and Zepeda-N{\'u}{\~n}ez, Leonardo},
  journal={SIAM Journal on Imaging Sciences},
  volume={16},
  number={1},
  pages={111--143},
  year={2023},
  publisher={SIAM}
}
```

## Questions

To get help on how to use the data or code, simply open an issue in the GitHub "Issues" section.