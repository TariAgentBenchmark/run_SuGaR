This repository hosts a GitHub Action to build the SuGaR conda environment from the upstream project and package it with conda-pack.

How to use:
- Trigger the workflow "Build and Pack SuGaR Conda Env" from the Actions tab.
- After it finishes, download the artifact named `sugar-conda-env`.

Notes:
- The workflow copies `environment.yml` from `https://github.com/Anttwo/SuGaR` and builds the `sugar` environment using mamba on Ubuntu 22.04.
- It then runs `conda-pack -n sugar -o sugar-conda-env.tar.gz` and uploads it as an artifact.
