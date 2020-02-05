# Valohai `conda` Examples

This repository contains Anaconda/Miniconda/[conda][ex] usage examples for the [Valohai machine learning platform][vh].

## Running Locally

```bash
# install `conda` locally with e.g. Miniconda or Anaconda
# https://docs.conda.io/en/latest/miniconda.html

git clone https://github.com/valohai/conda-example
cd conda-example
conda env create -n conda-example -f environment.yaml
conda run -n conda-example python check.py
```

## Running on Valohai

1. Create a project at https://app.valohai.com/
2. Save `https://github.com/valohai/conda-example` as the project repository.
3. Click "Fetch repository".
4. Click "Create execution", select any of the examples and click run.

## Adding Libraries

```bash
conda install -y -n conda-example tensorflow-gpu
conda env export -n conda-example --no-builds  | grep -v "^prefix: " > environment.yaml
```

[ex]: https://docs.conda.io/
[vh]: https://valohai.com/
