# Setup and Installation Instructions for Workshop

These instructions describe setup using `conda` or `mamba`. It is not strictly necessary
to use either of these. See the section
[Alternate Installation Methods](#alternate-installation-methods) at the end
of this document.

For the commands shown, `%` (and anything to the left of it) represents the
terminal prompt. You do not need to copy it; instead only copy the command to the
right of `%`.

## Updates to materials will be made through Thursday afternoon

Please plan to download workshop materials Thursday ecvening after 5PM EDT or Friday morning. The required Python environment will **not** change. You can (and should) set that up now.

## If you want to use a conda-based python and do not have it instaleld

The recommended distribution, because it is small and works out of the box on newer M1 macs, is `miniforge`.

Obtain an installer for your
operating system: https://github.com/conda-forge/miniforge#miniforge3.
Then follow the installation instructions at
https://github.com/conda-forge/miniforge#install

If you prefer, you can install the Anaconda Python Distribution, but it will include a bunch of things you don't need for this workshop.


## `conda`/`mamba` users

### 1. Install `mamba` (optional)

If you regularly use `conda` we recommend that you install `mamba` and use it instead of `conda`. `mamba` is a replacement for `conda` that typically runs faster.

Install mamba with:

```
conda install -c conda-forge mamba
```

### 2. Open the mamba command prompt

*miniforge includes an environment manager called mamba. Environments
allow you to have multiple sets of Python packages installed at the same
time, making reproducibility and upgrades easier. You can create,
export, list, remove, and update environments that have different versions of
Python and/or packages installed in them. For this workshop, we will configure the
environment using the mamba command prompt.*

Open a terminal window and verify that mamba is working:

    % mamba info

If you are having trouble, check your shell in a terminal window:

    % echo $SHELL

then run the initialization if needed, in that same terminal window:

    % mamba init $SHELL

On Windows, look for the "Anaconda prompt" or "Miniconda prompt" under the start menu.

### 3. Get the workshop materials: Download a ZIP file or clone the repository

You can download the ZIP file by opening the
green *Code* button at
https://github.com/mwcraig/astropy-workshop/tree/aavso-2023 and selecting *Download ZIP*.

If you already use `git`, you can clone the workshop repository instead using
[git](https://help.github.com/articles/set-up-git/):

    % git clone https://github.com/mwcraig/astropy-workshop

After you clone the repository be sure to check out the branch for this workshop:

    % git checkout -b aavso-2023  origin/aavso-2023

### 4. Create a mamba environment for the workshop

*miniforge includes an environment manager called mamba. Environments
allow you to have multiple sets of Python packages installed at the same
time, making reproducibility and upgrades easier. You can create,
export, list, remove, and update environments that have different versions of
Python and/or packages installed in them.*

Create a mamba environment for this workshop using a yml file.
The python version and all needed packages, including astropy, are listed in the
[environment.yml](https://github.com/astropy/astropy-workshop/blob/main/00-Install_and_Setup/environment.yml) file.

Open a terminal window using the appropriate one for your operating system.

Now navigate to this directory in the terminal. For example, if you installed
the astropy-workshop directory in your home directory, you could type the
following.

    % cd astropy-workshop/00-Install_and_Setup/

And finally, on any platform, to install and activate the astropy-workshop environment, type:

    % mamba env create --file environment.yml
    % mamba activate astropy-env-aavso

Note, you will need mamba version 1.0.0 and conda version 22.9 and later. If you need to update your version use `mamba update mamba`.

### 5. Check Installation

The name of the new mamba environment created above should be displayed next
to the terminal prompt: `(astropy-env) %`

In the terminal you used in the preceding step, inside the `astropy-workshop/00_Install_and_Setup/`
directory, run the `check_env.py` script to
check the Python environment and some of the required dependencies:

    (astropy-env) % python check_env.py

If the script reports that some of the versions do not match, check first
whether the package was installed using mamba or pip, then update accordingly.
The example below a fake package called `packagename`; replace it with the
actual package that you need to update.

    (astropy-env) % mamba list packagename

If it was installed with mamba, you will see (the channel column might or
might not be populated):

    # packages in environment at .../mambaforge/envs/astropy-env:
    #
    # Name                    Version                   Build  Channel
    packagename               X.Y.Z         py37hf484d3e_1000

Otherwise, if it was installed with pip, you will see the channel stating the
name `pypi`:

    # packages in environment at .../mambaforge/envs/astropy-env:
    #
    # Name                    Version                   Build  Channel
    packagename               X.Y.Z                     pypi_0    pypi

To update the reported package with mamba:

    (astropy-env) % mamba update packagename

Otherwise, to update with pip:

    (astropy-env) % pip install packagename --upgrade

The exception to this is if the `astroquery` package is reported as
out-of-date, always update to its pre-release version with pip:

    (astropy-env) % pip install astroquery --pre --upgrade

### 6. Starting Jupyter Lab

In the terminal window you used with the mamba environment created above,
change directory to the top level `astropy_workshop` directory.

    (astropy-env) % cd ..

Make sure the current directory in your terminal contains all the numbered notebook
directories. Then start Jupyter notebook:

    (astropy-env) % jupyter lab

If successful, your browser would open a new page/tab pointing to
`localhost` and show you a listing of the directory including all the numbered
notebook subdirectories.

## Alternate Installation Methods

### Use `pip`/`venv`

Although we recommend Miniforge, you can use either the [conda package
manager](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#creating-an-environment-from-an-environment-yml-file)
with the `environment.yml` file,  or
[pip/venv](https://packaging.python.org/en/latest/guides/installing-using-pip-and-virtual-environments/)
with the `requirements.txt` file in this directory.

The brief instructions for creating a virtual environment with pip/venv are:

1. In a terminal/command prompt, navigate to the folder you want to create the
virtual environment in, then:

```
% python -m venv astropy-env-aavso   # This will create the venv in the current folder
% source astropy-env-aavso/bin/activate
```

2. Navigate to the folder where you downloaded the workshop materials and then install the packages you need

```
% cd astropy-workshop/00-Install_and_Setup/
% pip install -r requirements.txt
```

After that, check your installation as described above.

### Use your base Python installation (the [YOLO](https://en.wikipedia.org/wiki/YOLO_(aphorism)) option)

After downloading the materials, install everything needed for the workshop with:

```
% cd astropy-workshop/00-Install_and_Setup/
% pip install -r requirements.txt
```

You run the risk of this breaking your base environment...


## Additional Resources

- [Set up git](https://help.github.com/articles/set-up-git/)
- [Mamba Documentation](https://mamba.readthedocs.io/)
- [Astropy Install Instructions](http://docs.astropy.org/en/latest/install.html)
- [Instructions for keeping this repo up to date](UPDATING.md)
