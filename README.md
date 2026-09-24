# Exoplanet Atmospheric Model Intercomparison

*Will Hannah · MPhys project · Supervised by Dr. Éric Hébrard, University of Exeter*

The study of exoplanet atmospheres relies heavily on modelling to interpret
spectra obtained from observations. However, models from the literature often
use different assumptions and chemical networks, leading to discrepancies in
predicted atmospheric structure and composition. The aim of this project is to
perform an intercomparison study between one-dimensional atmospheric models,
including the radiative-convective model ATMO, the chemical kinetics code
VULCAN, and other models from the literature.

As part of the project, I am working with the **ATMO** and **VULCAN** models.
The initial focus is on bringing the underlying physics of the models into
agreement, before investigating whether differences in chemistry and
chemical kinetics account for remaining discrepancies in their atmospheric
structures and spectra.

This repository contains the model inputs, conversion scripts, analysis
scripts and results used in the intercomparison.

## Repository Structure

```
Exoplanet-Atmosphere-Intercomparison/
├── ATMO
│   ├── Namelist-files
│   │   ├── pt_kin.in
│   │   ├── wasp39b_chem_kin.in
│   │   └── wasp39b_pt_eq.in
│   ├── hd209_chem_kin_kinetics_1e9_nophoto.ncdf
│   ├── hd209_chem_kin_kinetics_1e9_photo.ncdf
│   ├── read_atmo.py
│   ├── wasp39b_chem_kin_1e9_nophotochem.ncdf
│   └── wasp39b_chem_kin_1e9_photochem.ncdf
├── file-conversion
│   ├── atmo_to_vulcan_pt.py
│   ├── bt-settl_convert_to_atmo.py
│   ├── h5_to_ncdf.py
│   ├── photon_to_energy_flux.py
│   └── sflux_atmo_to_vulcan.py
├── model-comparison
│   ├── read_all.py
│   ├── read_atmo_vulcan_pact.py
│   └── read_atmo_vulcan.py
├── stellar-spectra
│   └── read_stellar_spectra.py
├── VULCAN
│   ├── ATMO_P-T_inputs
│   │   ├── atmo_hd209_pt.txt
│   │   └── atmo_wasp39b_pt.txt
│   ├── cfg_HD209_atmo_pt_nophoto.txt
│   ├── cfg_wasp39b_photo_new.txt
│   ├── HD209_atmo_pt_nophoto.vul
│   ├── HD209_atmo_pt_photo.vul
│   ├── vulcan_cfg_WASP39b.py
│   ├── wasp39b_nophoto_new.vul
│   └── wasp39b_photo_new.vul
└── README.md
```
