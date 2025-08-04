# Tracking and Object-Based Analysis of Clouds in Global Km-scale Model Simulations

<img src="thumbnail.png" alt="thumbnail" width="300"/>

[![nightly-build](https://github.com/ProjectPythia/storm-tracking-cookbook/actions/workflows/nightly-build.yaml/badge.svg)](https://github.com/ProjectPythia/storm-tracking-cookbook/actions/workflows/nightly-build.yaml)
[![Binder](https://binder.projectpythia.org/badge_logo.svg)](https://binder.projectpythia.org/v2/gh/ProjectPythia/storm-tracking-cookbook/main?labpath=notebooks)
[![DOI](https://zenodo.org/badge/475509405.svg)](https://zenodo.org/badge/latestdoi/475509405)

This Project Pythia Cookbook covers ... (replace `...` with the main subject of your cookbook ... e.g., _working with radar data in Python_)

## Motivation

High-resolution weather and climate model simulations are becoming increasingly common, providing valuable insights into atmospheric processes at kilometer-scale resolution. One effective way to analyze the output from such simulations is to track storm systems over time and space and evaluate their statistical properties.

However, many state-of-the-art kilometer-scale models—such as MPAS (Model for Prediction Across Scales)—produce output on unstructured grids, which poses a challenge for many existing storm-tracking algorithms. One such tool is tobac (Tracking and Object-Based Analysis of Clouds), which typically operates on regular, structured grids.

In this notebook, we demonstrate a straightforward workflow to:

Regrid global km-scale output from the MPAS model to a structured grid suitable for object-based analysis.

Apply the tobac tracking algorithm to identify and track storm features.

This example provides a starting point for researchers looking to integrate high-resolution unstructured model output into their storm tracking and statistical analysis workflows.


## Authors

[Julia Kukulies](@first-author), [Orhan Eroglu](@second-author), etc. _Acknowledge primary content authors here_

### Contributors

<a href="https://github.com/ProjectPythia/storm-tracking-cookbook/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=ProjectPythia/storm-tracking-cookbook" />
</a>

## Structure

(State one or more sections that will comprise the notebook. E.g., _This cookbook is broken up into two main sections - "Foundations" and "Example Workflows."_ Then, describe each section below.)

### Introduction to tobac

This notebook gives an introduction to the tracking algorithm tobac (Tracking and Object-Based Analysis of Clouds). 

###  Introduction to MPAS

This notebook gives an introduction to MPAS (Model Prediction Across Scales) and the unstructured grids produces by the MPAS model. 

### Preprocessing of MPAS data 

Here, we show a workflow based on the library xesmf to regrid the unstructured data onto a regular grid and save a sub-selection of variables from the original model output data. This preprocessing step is necessary, in order to run the tracking algorithm tobac with MPAS data. 


### Storm tracking with tobac

In this notebook, we go through the three main module of the tobac library that provide a framework for storm tracking in the high-resolution model data. Specifically, we demonstrate how to first detect features based on customized thresholds and criteria, then define the extent of the storm objects and track the identified storm objects over time. 

### Output analysis and visualization

Finally, we show a simple example for how the output data of the storm tracking can be analyzed and visualized. 


## Running the Notebooks

You can either run the notebook using [Binder](https://binder.projectpythia.org/) or on your local machine.

### Running on Binder

The simplest way to interact with a Jupyter Notebook is through
[Binder](https://binder.projectpythia.org/), which enables the execution of a
[Jupyter Book](https://jupyterbook.org) in the cloud. The details of how this works are not
important for now. All you need to know is how to launch a Pythia
Cookbooks chapter via Binder. Simply navigate your mouse to
the top right corner of the book chapter you are viewing and click
on the rocket ship icon, (see figure below), and be sure to select
“launch Binder”. After a moment you should be presented with a
notebook that you can interact with. I.e. you’ll be able to execute
and even change the example programs. You’ll see that the code cells
have no output at first, until you execute them by pressing
{kbd}`Shift`\+{kbd}`Enter`. Complete details on how to interact with
a live Jupyter notebook are described in [Getting Started with
Jupyter](https://foundations.projectpythia.org/foundations/getting-started-jupyter.html).

Note, not all Cookbook chapters are executable. If you do not see
the rocket ship icon, such as on this page, you are not viewing an
executable book chapter.


### Running on Your Own Machine

If you are interested in running this material locally on your computer, you will need to follow this workflow:

1. Clone the `https://github.com/ProjectPythia/storm-tracking-cookbook` repository:

   ```bash
    git clone https://github.com/ProjectPythia/storm-tracking-cookbook.git
   ```

1. Move into the `storm-tracking-cookbook` directory
   ```bash
   cd storm-tracking-cookbook
   ```
1. Create and activate your conda environment from the `environment.yml` file
   ```bash
   conda env create -f environment.yml
   conda activate storm-tracking-cookbook-dev
   ```
1. Move into the `notebooks` directory and start up Jupyterlab
   ```bash
   cd notebooks/
   jupyter lab
   ```
