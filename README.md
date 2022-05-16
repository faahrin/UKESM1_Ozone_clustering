# Ozone clustering in UKESM

 [![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)

## Requirements
- Python 3.8+

## Getting started
At present, you can use Docker to get this project installed and running. (We could go with a simpler docker container in the future). These commands work for me:
```
cd <where-you-want-to-work>
docker pull dannes/ozonegmm
docker run --rm -it -p 8888:8888 -v $PWD:/work -w /work dannes/ozonegmm jupyter-lab --no-browser --ip=0.0.0.0
```
Note that Docker can only see "down the tree", so make sure that any data and files that you want to work with are within the tree. To test the source code in `src`, you can use this same Docker image to run `ipython`:
```
docker run --rm -it -p 8808:8808 -v $PWD:/work -w /work dannes/ozonegmm bash
```
and then run `ipython3`. 


## Project Organization
```
├── LICENSE
├── README.md          <- The top-level README for developers using this project.
├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
├── report             <- Generated analysis as HTML, PDF, LaTeX, etc.
├── requirements       <- Directory containing the requirement files.



