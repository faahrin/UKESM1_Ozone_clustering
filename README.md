# Ozone clustering in UKESM

 [![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
 <a href="https://zenodo.org/badge/latestdoi/479902597"><img src="https://zenodo.org/badge/479902597.svg" alt="DOI"></a>

## Requirements
- Python 3.8+
- Docker Image https://hub.docker.com/repository/docker/dannes/ozonegmm

## Getting started
You can use Docker to get this code running quickly. Use these commands for a Jupyter notebook server:
```
cd <where-you-want-to-work>
docker pull dannes/ozonegmm
docker run --rm -it -p 8888:8888 -v $PWD:/work -w /work dannes/ozonegmm jupyter-lab --no-browser --ip=0.0.0.0
```
Note that Docker can only see "down the tree", so make sure that any data and files that you want to work with are within the tree. To test the source code in `src`, you can use this same Docker image to run `ipython`:
```
docker run --rm -it -p 8808:8808 -v $PWD:/work -w /work dannes/ozonegmm bash
ipython3
```

## Project Organization
```
├── LICENSE            <- The top-level README for developers using this project.
├── README.md          <- The top-level README for developers using this project
├── data_in            <- Subset of UKESM1 ozone data analysed in this work (accessed via Pangeo)
├── figures            <- Figures from the paper
├── models             <- Saved parameters for the GMM model
├── requirements       <- Requirements file (redundant due to Docker image)
├── *.ipynb            <- Example notebooks with source code 


