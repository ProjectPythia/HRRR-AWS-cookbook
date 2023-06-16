# HRRR on AWS Cookbook

<img src="thumbnail.svg" alt="thumbnail" width="400"/>

[![nightly-build](https://github.com/ProjectPythia/HRRR-AWS-cookbook/actions/workflows/nightly-build.yaml/badge.svg)](https://github.com/ProjectPythia/HRRR-AWS-cookbook/actions/workflows/nightly-build.yaml)
[![Binder](https://binder.projectpythia.org/badge_logo.svg)](https://binder.projectpythia.org/v2/gh/ProjectPythia/HRRR-AWS-cookbook.git/main)

In this Project Pythia Cookbook, you will access and create a map from archived data from NCEP's High-Resolution Rapid Refresh (HRRR) model, which is served in an S3 bucket on AWS.

## Motivation
This cookbook provides the essential materials to learning how to work with gridded NCEP model output that is served on AWS' S3 buckets, in a data format called Zarr.

Once you go through this material, you will have mastered the following skills:

1. Understand what *object store* refers to, and how it relates to AWS's S3 buckets
1. Familiarized yourself with the Zarr data representation model, and why it is an optimal format for data stored on S3
1. Access, analyze, and visualize gridded fields from the HRRR

Throughout this cookbook, we build on the core foundational Python material covered in the [Foundations Book](https://foundations.projectpythia.org/landing-page.html)

## Authors

[Kevin Tyle](https://github.com/ktyle)

### Contributors

<a href="https://github.com/ProjectPythia/HRRR-AWS-cookbook/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=ProjectPythia/HRRR-AWS-cookbook" />
</a>

## Structure
This cookbook will have two main sections - "Foundations" and "Example Workflows."

### Foundations
**Currently under development** 
The foundational content will include:
- NCEP Model data on AWS' S3 
  - an overview of how to access NCEP's real-time and archived NWP model output on AWS
  - an introduction to the Zarr data format
  - How to read in a Zarr-formatted HRRR grid with Xarray

### Example Workflows
Here, we **apply** the lessons learned in the foundational material to various analysis workflows, including everything from reading in the data to plotting a beautiful visualization at the end. We include the additional dataset-specific details, focusing on building upon the foundational materials rather than duplicating previous content.

1. Plot a map of 2-meter temperature from a past HRRR run
1. **Currently under development** Plot a time series of wind speed from a past HRRR run
1. **Currently under development** Plot a sequence of forecast maps for the most recent run of the HRRR

## Running the Notebooks
You can either run the notebook using [Binder](https://binder.projectpythia.org/) or on your local machine.

### Running on Binder

The simplest way to interact with a Jupyter Notebook is through
[Binder](https://binder.projectpythia.org/), which enables the execution of a
Jupyter Book in the cloud. The details of how this works are not
important for now. All you need to know is how to launch a Pythia
Foundations book chapter via Binder. Simply navigate your mouse to
the top right corner of the book chapter you are viewing and click
on the rocket ship icon, (see figure below), and be sure to select
“launch Binder”. After a moment you should be presented with a
notebook that you can interact with. I.e. you’ll be able to execute
and even change the example programs. You’ll see that the code cells
have no output at first, until you execute them by pressing
`Shift` `Enter`. Complete details on how to interact with
a live Jupyter notebook are described in [Getting Started with
Jupyter](https://foundations.projectpythia.org/foundations/getting-started-jupyter.html).

### Running on Your Own Machine
If you are interested in running this material locally on your computer, you will need to follow this workflow:

1. Clone the ["HRRR-AWS-cookbook"](https://github.com/ProjectPythia/HRRR-AWS-cookbook) repository
    ```bash
    git clone https://github.com/ProjectPythia/HRRR-AWS-cookbook.git
    ```

2. Move into the `HRRR-AWS-cookbook` directory
    ```bash
    cd HRRR-AWS-cookbook
    ```

3. Create and activate your conda environment from the `environment.yml` file
    ```bash
    conda env create -f environment.yml
    conda activate HRRR-AWS-cookbook-dev
    ```

4.  Move into the `notebooks` directory and start up Jupyterlab
    ```bash
    cd notebooks/
    jupyter lab
    ```

At this point, you can interact with the notebooks! Make sure to check out the ["Getting Started with Jupyter"](https://foundations.projectpythia.org/foundations/getting-started-jupyter.html) content from the [Pythia Foundations](https://foundations.projectpythia.org/landing-page.html) material if you are new to Jupyter or need a refresher.
