# Code for: "Spectral characterisation of short-wave infrared (SWIR) tissue chromophores and tissue-mimicking phantom optical properties"

**Authors:** [Melissa J. Watt](https://github.com/melissajanewatt), Layla Malouf, Ran Tao, Isabelle Racicot, Thomas R. Else, Janek Gröhl, Sarah E. Bohndiek. *University of Cambridge*

Contact details: Sarah E. Bohndiek, seb53@cam.ac.uk

Ths repository contains the code used for the paper "Spectral characterisation of short-wave infrared (SWIR) tissue chromophores and tissue-mimicking phantom optical properties" and associated dataset of SWIR tissue chromophore and tissue-mimicking phantom optical properties. The simulation dataset will be provided on Apollo - the University of Cambridge repository - upon acceptance.

## Python environment

This code has been written as Jupyter Notebooks (.ipynb) and requires a Python environment. The deposited version of the code was tested on Mac with Python 3.7.6.

## Code description

1. **`Data/`**: contains the following directories:
   1. **`Download_Spectra/`**: `.txt` and `.npz` files containing the measured absorption and reduced scattering coefficients, ready to download.
      > **Note:** the whole blood is horse blood, which has smaller red blood cell (RBC) diameters than human blood. The measured reduced scattering coefficient is therefore lower than expected for human blood.
   2. **`RBCs/`**: `.csv` files with horse RBC diameters measured by flow cytometry.
   3. **`Reference Spectra/`**: reference datasets of optical properties from the literature (see paper for full description).
   4. **`Shimadzu/`**: `.csv` files containing raw transmittance spectra measured with the Shimadzu SIS system, and a combined processed file with the estimated absorption coefficient for all measured chromophores.
   5. **`Simulation_Spectra/`**: optical properties used in the SIMPA simulations. These combine our measured spectra with reference spectra from the literature (see paper for details).
   6. **`in-house-SIS/`**: subdirectories containing raw data and IAD outputs for each chromophore and tissue-mimicking phantom measured with the in-house SIS system, and a combined processed `.csv` file with the estimated optical properties for all measured chromophores.
   7. **`po2_probe_data/`**: raw data from the oxygen probe.

2. **`Plots_for_Figures.ipynb`**: generates the figures and models of whole blood scattering using Mie theory.

3. **`Post_process_IAD.ipynb`**: post-processes the IAD algorithm outputs.

4. **`Process_spectra.ipynb`**: estimates and processes the absorption and reduced scattering coefficients of the measured tissue chromophores and tissue-mimicking phantoms.

5. **`SIMPA_simulations.ipynb`**: generates and simulates models of tissues and phantoms using the SIMPA Python toolkit.

6. **`Simulation_analysis.ipynb`**: calculates the effective penetration depth from the simulation results.

7. **`Statistical analysis.ipynb`**: statistically compares our characterisations with the reference data.
