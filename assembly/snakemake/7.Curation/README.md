# HiC curation data preparation

Snakemake pipeline to generate .pretext and .mcool files to visualise HiC contact maps using PretextView and Higlass, respectively.

##Prerequisites

This pipeline has been tested using `Snakemake v7.32.4` and installation of necessary tools is through conda.

HiC should be present in a folder and paired reads should be named `Library1_1.fastq.gz Library1_2.fastq.gz Library2_1.fastq.gz Library2_2.fastq.gz`. The pipeline can accept any number of paired HiC read-sets, but the naming must be consistent with this format (data can be linked, e.g. with `ln -s`).

A temporary folder must be created and the path given in the config file. This should have enough space to store temporary files when sorting, which can equal the size of the input .pairsam file (100s of GB or even TBs).

## Execution

To execute the pipeline run:

`snakemake --use-conda`

A set of example parameters and an execution command is also provided for submission to a slurm queueing system. Simply run:

`./run_cluster`

after configuring the `cluster.json` file.
