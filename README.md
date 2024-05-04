# Code Comparison Project

This repository hosts a code comparison project aimed at comparing the results of different codes used for afterglow light curve calculations. The project involves running code implementations provided by various contributors and comparing their output flux as a function of time.

## Directory Structure

- **tests**: Contains test cases for code comparison.
  - **case\***: Test case folders, where * represents the number of the test case.
    - **problem-setups.json**: JSON file describing model parameters needed for afterglow light curve calculation.
    - **Your_Working_Folder**: Contributors should create a working folder at the same level as `problem-setups.json`, with a name of their choice.
      - **flux.csv**: Comma-separated value file storing the output flux as a function of time. The first column represents time in seconds, and the second column represents flux in erg/cm^2/s.

## Problem Setups Explanation

The `problem-setups.json` file provides the necessary model parameters for afterglow light curve calculation. Here's an example of the JSON structure and its explanation:

```json
{
    "case name": "narrow core GW170817",
    "synchrotron": true,
    "self-absorption": true,
    "inverse compton cooling": true,
    "synchrotron self-compton": false,
    "Klein-Nishina": false,
    "reverse shock": false,
    "jet spreading": false,
    "unit": "cgs",
    "E_iso": 4.0e+53,
    "luminosity distance": 1.23e+26,
    "z": 0.009,
    "jet type": "Gaussian",
    "theta_core": 0.044,
    "theta_wing": 0.6,
    "Gamma0": 300,
    "n_ism": 0.0199526231496888,
    "epsilon_e": 0.01,
    "epsilon_B": 0.00019952623149688788,
    "p": 2.139,
    "theta_view": 0.54,
    "t_obs": [
        8.64e3,
        8.64e8
    ],
    "band pass (kev)": [
        0.3,
        10
    ]
}
```

- `case name`: Name of the test case.
- `synchrotron`: Boolean indicating whether synchrotron radiation is considered.
- `self-absorption`: Boolean indicating whether self-absorption is considered.
- `inverse compton cooling`: Boolean indicating whether inverse Compton cooling is considered.
- `synchrotron self-compton`: Boolean indicating whether synchrotron self-Compton scattering is considered.
- `Klein-Nishina`: Boolean indicating whether Klein-Nishina correction is considered.
- `reverse shock`: Boolean indicating whether reverse shock is considered.
- `jet spreading`: Boolean indicating whether jet spreading is considered.
- `unit`: Unit system used for the parameters.
- `E_iso`: Isotropic equivalent energy in erg.
- `luminosity distance`: Luminosity distance in cm.
- `z`: Redshift.
- `jet type`: Type of the jet.
- `theta_core`: Half-opening angle of the jet core in radians.
- `theta_wing`: Half-opening angle of the jet wing in radians.
- `Gamma0`: Initial Lorentz factor of the jet.
- `n_ism`: Number density of the interstellar medium (ISM) in cm^(-3).
- `epsilon_e`: Fraction of the shock energy given to the electrons.
- `epsilon_B`: Fraction of the shock energy given to the magnetic field.
- `p`: Electron energy distribution index.
- `theta_view`: Viewing angle of the observer in radians.
- `t_obs`: Observation times in seconds [start, end].
- `band pass (kev)`: Energy bandpass in keV. [low, high]

## Running Your Code

Welcome, contributors! To run your code, please use the `problem-setups.json` file provided for each test case. After your code executes, save the results in a `flux.csv` file within your working folder. This helps maintain a consistent directory structure for easy comparison using `plot.ipynb`.

## Contributing

If you've completed your simulations and have output data, please submit a pull request with your `flux.csv` files. Ensure your files are saved in the designated working folder as outlined. Your contributions help enhance our project and facilitate easy result comparisons.

## Plotting Comparison

To visualize and compare your simulation results, utilize the `plot.ipynb` Jupyter Notebook available in our repository. It's designed to help you plot the flux as a function of time across different code implementations, offering a clear view of the variations.


