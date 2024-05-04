# Code Comparison Project

This repository hosts a code comparison project aimed at comparing the results of different codes used for afterglow light curve calculations. The project involves running code implementations provided by various contributors and comparing their output flux as a function of time.

## Directory Structure

- **tests**: Contains test cases for code comparison.
  - **case\***: Test case folders, where * represents the number of the test case.
    - **problem-setups.json**: JSON file describing model parameters needed for afterglow light curve calculation.
    - **Your_Working_Folder**: Contributors should create a working folder at the same level as `problem-setups.json`, with a name of their choice.
      - **flux.csv**: Comma-separated value file storing the output flux as a function of time. The first column represents time in seconds, and the second column represents flux in erg/cm^2/s.

## Running Your Code

Contributors can run their code based on the provided `problem-setups.json` file for each test case. After running their code, ensure that the results are saved in a `flux.csv` file within your working folder. It's important to maintain this directory structure to facilitate comparison.

## Contributing

Contributors who have run their code and obtained output data can submit pull requests with their output data files (`flux.csv`). Once you have finished running your code and generated the output data, please ensure that your `flux.csv` files are saved within your working folder as described in the directory structure section. You can then submit your output data by creating a pull request. This will allow for easy comparison of results from different code implementations. Thank you for your contribution!

## Plotting Comparison

To visualize and compare the results, you can use the `plot.ipynb` Jupyter Notebook provided in the repository. This notebook facilitates plotting the flux as a function of time for different code implementations, allowing for easy comparison.
