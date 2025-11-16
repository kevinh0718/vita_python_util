# VItA Python Utils

Shared utility library for the UIUC CISL Head and Mice Phantom projects.

This repo is based on the [VItA](https://github.com/GonzaloMaso/VItA) library for vessel synthesis using CCO algorithm.

> ***It is strongly recommended to read the original VItA paper to understand the concept and parameters for vessel synthesis.***

> ***And, you you also cite the original paper if you find VItA useful in your work.***


> Maso Talou, G. D., et al. "Adaptive constrained constructive optimisation for complex vascularisation processes." Scientific Reports 11.1 (2021): 1-22. - https://www.nature.com/articles/s41598-021-85434-9

This repo provides the functions to enable the use of VItA in Python.

This includes the `save_np_vtk` that reconstructs the surface of a object (3d boolean ndarray)\
and saves it as a `.vtk` file, which is therefore used in VItA.

This repo also includes the use of docker to enable the vessel synthesis\
without the need for installing VItA.

Details of the docker container can be found [here](https://github.com/kevinh0718/vita_container/tree/main?tab=readme-ov-file).

More usages can be found in [usage](#usage).

## Installation

You can install this package directly from GitHub:

```bash
pip install git+https://github.com/kevinh0718/vita_python_utils.git
```

or locally after cloning this repo:

```bash
pip install . # or "pip install -e ." for the need of actively updating the src script
```

## Usage

It's assumed that the user is familiar with the basic vita operation or is using this repo following instructions in some of the phantom generation repo.

If none of the above conditions applied, please follow the `example/demo_usage.ipynb`.

Before running the notebook, please setup the vita docker container or installed VItA following the original [VItA](https://github.com/GonzaloMaso/VItA) repo.

1. Make sure the `vita_setup.sh` and `vita_test.sh` are executable. If not, run:
```bash
chmod u+x vita_setup.sh vita_test.sh
```

2. Execute `vita_setup.sh`. You can examine the setup using `vita_test.sh`.\
If all goes well, you can see `demo_sphere.cco` and `demo_sphere.vtp` being generated.

Note that these two commands should be execute in this repo.\
If not, please update the path to the `example/demo` folder