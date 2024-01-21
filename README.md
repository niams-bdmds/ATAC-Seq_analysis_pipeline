#ATAC-seq analysis pipeline

## Overview
This repository contains script directory, .yml, .yaml, and configuration files
required for implementing this pipeline. 

## How to run this pipeline
This pipeline requires reference genome, genome-size file and bowtie index file.
Specify the path to these files in the configuration file. Put FASTQ file in fq
directory. FASTQ files reside in fq directory with the following name format. 
            <{smp}_r1_fq.gz>
            <{smp}_r2_fq.gz>
The sample name should start from the letter 's'. Use hg38 prefix snakefile for
human sample. mm10 prefix snakefile for mouse sample.

## Running the script:
            dry run:
                < module load snakemake/6.8.2 >
                < snakemake -s hg38_Snakefile >
            batch job:
                < sbatch hg38_Snakefile >
