# Base Kedro Starter

The code in this repository demonstrates best practice when working with Kedro. It contains a Kedro starter template with some initial configuration.

This Kedro starter includes:

* Templates pipelines:
  * feature_engineering
  * training
  * serving
* Makefile example to build performance report
* Bitbucket pipelines example to set validation and experimentation

## Requirements

This project requires:

* kedro
    * See git tags of this project to know what version of kedro is possible to run the project, each tag is a kedro version available
* python 3.8 or later

## Running Locally

### Run (with project clone)

Create a virtual environment and enable it:

* `python -m venv venv`
* `source venv/bin/activate`

Clone the project:

* `git clone https://user@bitbucket.org/indiciumtech/base_kedro_project.git`

Install kedro:

* `pip install kedro==0.18.4`

Finally, use kedro to create the project:

* `kedro new --starter=/path/to/my/dir/base_kedro_project`

### Run (without project clone)

Create a virtual environment and enable it:

* `python -m venv venv`
* `source venv/bin/activate`

Install kedro (Currently, only version 0.18.4 is available for use kedro starter, to see if other versions of kedro can be used, see the git tags, each tag is a kedro version available):

* `pip install kedro==0.18.4`

Finally, use kedro to create the project:

* `kedro new --starter git+https://bitbucket.org/indiciumtech/base_kedro_project/src/main/`

### Install dependencies

The only dependency to run is kedro:

* `pip install kedro==0.18.4`
  
After using the `kedro new --starter=...`, and the project is created, you can install the project's dependencies to continue development:

* `pip install -r src/requirements.txt`

## How to use pre-commit-hooks linter

* First, `pre-commit` package needs to be installed (the package is already in the `src/requirements.txt` file)
* The file `.pre-commit-config.yaml` must be added (the file already exists, if necessary, change the package versions)
* Finally, in the folder where the file was added, use the following command to install the pre-commit:
    * `pre-commit install`
