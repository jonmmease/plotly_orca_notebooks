# Overview
This repo contains some example notebooks for using the static image export
capability coming in plotly.py version 3.2.0.

For an overview of how this all works, see
https://github.com/plotly/plotly.py/pull/1120

# Installation
Static image export relies on the plotly orca command-line utility.
See https://github.com/plotly/orca for more information on orca.  To try
out these examples, follow the instructions below for either conda or
pip. 

## conda
All dependencies needed to support image export can be installed using conda
as follows:

```
$ conda env create -f environment.yaml
$ source activate plotly_conda37
```

**Note:** If you are using Windows you will need to remove the `poppler`
dependency from `environment.yaml`. Poppler is required for the `EPS` image
export, but unfortunately we don't know of an easy way to install poppler
on Windows.  All other image export formats (including `PDF`) are supported
without poppler.

## pip
First, use pip to install the necessary Python dependencies:

```
pip install "plotly >=3.2.0a2" "ipywidgets >=7.2" "notebook>=5.3" psutil numpy 
```

Then install orca (and poppler if you want EPS support) according to the
instructions in the orca README at https://github.com/plotly/orca.
