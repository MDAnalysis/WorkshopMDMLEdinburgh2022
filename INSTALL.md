# Installing the workshop environment

## Overview

This workshop is delivered mainly through a series of [Jupyter notebooks][1]
that allow for interactive Python programming.

To use these, several Python packages must be installed. A full list of these
can be found in [`environment.yml`](environment.yml). See below for
instructions on how to set up a local copy of the Python environment.

## Installing the Python environment

Due to the complexity of the workshop environment, we strongly recommend the
use of the [Anaconda Python distribution][2]. The instructions provided here
assume the use of [conda][3].

### 1. Creating a workshop environment

To create an environment named `mdml_workshop` with all the necessary
Python dependencies:

```bash
conda env create --file=environment.yml
```

See the [conda documentation][4] for more information on how to access and
manage [conda][3] environments.

To then activate this environment:

```bash
conda activate mdml_workshop
```

### 2. Activating the Jupyter extensions

The workshop leverages the extended utility of several Jupyter nbextensions.

To install these, the followed should be run **once** (after having activated
the conda environment):

```bash
jupyter contrib nbextension install --user
jupyter nbextension enable splitcell/splitcell
jupyter nbextension enable rubberband/main
jupyter nbextension enable exercise2/main
jupyter nbextension enable autosavetime/main
jupyter nbextension enable collapsible_headings/main
jupyter nbextension enable codefolding/main
jupyter nbextension enable limit_output/main
jupyter nbextension enable toc2/main
```


[1]: https://jupyter-notebook.readthedocs.io/en/stable/
[2]: https://docs.anaconda.com/anaconda/install/
[3]: https://conda.io/projects/conda/en/latest/index.html
[4]: https://docs.conda.io/projects/conda/en/latest/user-guide/getting-started.html?highlight=conda%20activate#managing-environments
