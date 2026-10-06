# GENE ion-temperature-gradient and fast-ion scan inputs

This repository contains GENE simulation input files for an ion-temperature logarithmic-gradient scan with and without a kinetic fast-ion species.

## Files

The `inputs/` directory contains 21 files:

- `g022663.005340`: common magnetic-equilibrium input.
- Ten `parameters_*` files: GENE simulation configurations.
- Ten `iterdb_sample_*` files: corresponding ITERDB profiles.

## Simulation cases

Five ion-temperature logarithmic-gradient scale factors are included:

**0.80, 0.90, 1.00, 1.10, and 1.20.**

Each scale has two cases:

- `no_fastion`: electrons, main ions, and carbon.
- `tfast_over_te_22p9382`: electrons, main ions, fast ions, and carbon.

The profiles contain 51 RHOTOR points from 0 to 1 at a single time of 5.34 s. Temperatures are labelled in eV and densities in m^-3.

The fast-ion temperature ratio in the filename applies at RHOTOR = 0.4. In the no-fast-ion cases, fast-ion density is transferred to the main-ion density.

## Preparing the inputs

Select a parameter file and an ITERDB profile with the same case suffix.

In a separate working directory:

1. Copy the selected parameter file as `parameters`.
2. Copy the corresponding profile as `iterdb_sample`.
3. Copy `g022663.005340` into the same directory.
4. Create an `out` directory.

The supplied configurations specify 384 MPI ranks for no-fast-ion cases and 512 MPI ranks for fast-ion cases.

In no-fast-ion profiles, `TI2/NM2` represents carbon. In fast-ion profiles, `TI2/NM2` represents fast ions and `TI3/NM3` represents carbon.

## Citation

A version-specific Zenodo DOI will be added after the release is archived.

Please cite the archived input dataset and the relevant GENE method/software references.

## License

The input dataset and repository documentation are licensed under Creative Commons Attribution 4.0 International (CC BY 4.0).

GENE software is obtained separately under its own licensing terms.
