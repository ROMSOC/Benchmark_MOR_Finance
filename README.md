<img src="images/romsoclogo-logo.png" alt="ROMSOC logo"  width="150"/>

# Benchmarks for model order reduction in finance
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.5171809.svg)](https://doi.org/10.5281/zenodo.5171809) [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/ROMSOC/benchmarks-MOR-finance/HEAD?labpath=source/Benchmark2_1.ipynb)

## Summary
Benchmark cases for yield curve simulation, classical and adaptive greedy sampling approaches developed in https://doi.org/10.1186/s13362-021-00105-8.

## Description
It is essential to be aware of the financial risk associated with an invested product. The risk analysis of financial instruments often requires the valuation of such instruments under a wide range of future market scenarios. The market scenarios (e.g., interest rates) are then input parameters in a valuation function that delivers the fair value of such financial instruments.  These models are calibrated based on market scenarios that generate a high-dimensional parameter space. In short, to perform the risk analysis, the financial model needs to be solved for such a high dimensional parameter space, and this requires efficient algorithms. These two benchmark cases present the model order reduction approach based on the proper orthogonal decomposition approach with greedy sampling approaches for parameter sampling. The first case generates the 10000 simulated yield curves, which are then used to calibrate the financial model parameters. The second case presents both the classical and adaptive greedy sampling approaches.

## Directory structure
In the source directory, one can find all source files required to run the benchmark cases. The directory benchmark contains the input data with the executable files. The ``Benchmark1_1.m`` file executes the yield curve simulation while the ``Benchmark1_2.nb`` file runs the parameter calibration. The classical greedy and adaptive greedy sampling techniques can be executed using ``Benchmark2_1.m`` and ``Benchmark2_2.m`` files. One can find a PDf file with a detailed step-by-step description of the benchmark case in the directory documentation. 

## Benchmark execution
The benchmark case can be run using the script files Benchmarkx_x.m. 

## Run Jupyter notebooks
The entire benchmark repository can be executed in a provided Docker container where a full installation of Octave is available. Once you have clone or downloaded this repository, to build the container just type
```bash
docker build -t benchmarks-MOR-finance . 
```
and for running it locally:
```bash
docker run -it --rm -p 8888:8888 benchmarks-MOR-finance jupyter-lab --ip=0.0.0.0 --port=8888 --allow-root
```
Alternatively, please use the following link to run a user-friendly Jupyter Notebook (``*.ipynb``) with different benchmark scenarios. For instance, Benchmark 2.1 (classical greedy sampling) is implemented at:
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/ROMSOC/benchmarks-MOR-finance/HEAD?labpath=source/Benchmark2_1.ipynb) Please, notice that mybinder cloud computations are limited to 2GB of RAM memory.

## Disclaimer
In downloading this SOFTWARE you are deemed to have read and agreed to the following terms:
This SOFTWARE has been designed with an exclusive focus on civil applications. It is not to be used
for any illegal, deceptive, misleading or unethical purpose or in any military applications. This includes ANY APPLICATION WHERE THE USE OF THE SOFTWARE MAY RESULT IN DEATH,
PERSONAL INJURY OR SEVERE PHYSICAL OR ENVIRONMENTAL DAMAGE. Any redistribution of the software must retain this disclaimer. BY INSTALLING, COPYING, OR OTHERWISE
USING THE SOFTWARE, YOU AGREE TO THE TERMS ABOVE. IF YOU DO NOT AGREE TO
THESE TERMS, DO NOT INSTALL OR USE THE SOFTWARE

## Acknowledgments
<img src="images/EU_Flag.png" alt="EU Flag"  width="150" height="100" />

The ROMSOC project has received funding from the European Union’s Horizon 2020 research and innovation programme under the Marie Skłodowska-Curie Grant Agreement No. 765374.
This repository reflects the views of the author(s) and does not necessarily reflect the views or policy of the European Commission. The REA cannot be held responsible for any use that may be made of the information this repository contains.
