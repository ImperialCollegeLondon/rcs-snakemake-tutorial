# RCS Snakemake Tutorial

These instructions describe how to run a lightly-modified version of the official [Snakemake short tutorial](https://snakemake.readthedocs.io/en/stable/tutorial/short.html) on Imperial College's HPC system (the RCS compute service).

## Setup

1. Clone or download this repository to the compute service and make the folder your working directory
2. Retrieve a copy of the tutorial data:

    ```sh
    wget https://github.com/snakemake/snakemake-tutorial-data/archive/v5.4.5.tar.gz
    tar --wildcards -xf v5.4.5.tar.gz --strip 1 "*/data"
    ```

3. Create a Conda environment containing the required tools:

    ```sh
    conda env create --file environment.yml
    ```

## Execute

Run the Snakemake workflow in a job:

```sh
qsub snakemake-tutorial.pbs.sh
```
