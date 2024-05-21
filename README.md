# Q-SYS Plugins Documentation

User documentation for the Q-SYS plugins for Designer and Expert.

This is built and deployed to the dl.pharoscontrols.com site, currently under software_help/qsc

## Prerequisites

You need to have [Sphinx](http://www.sphinx-doc.org/en/stable/) installed to build this documentation.

You can install Sphinx and other python dependencies from the requirements file. From the root directory of the project you can run:

    pip install -r requirements.txt

where `pip` might need to be `pip3` or similar if you've installed pip under another name.

The project Makefile assumes your python executable is `python`. If it's anything other than `python` then you should define the `SPHINXBUILD` environment variable to be `{your python executable} -msphinx`, e.g. `python3 -msphinx`.

## Build instructions

From the root directory of the project you can run, on Linux or macOS:

    make html

or on Windows:

    .\make.bat html

This will create the html output for Pharos in the `build` directory (which will be created if building for the first time).

### Building a specific product

The system can generate documentation for either the Designer or Expert product lines. To specify a product, set `PRODUCT` in your environment, e.g.

using Linux or macOS:

    PRODUCT=designer make html

using Windows Command Prompt:

    set PRODUCT=designer
    make.bat html

using PowerShell:

    $env:PRODUCT = 'designer'
    ./make.bat html

Currently supported products are:

* `designer` for Pharos Designer (the default)
* `expert` for Pharos Expert
