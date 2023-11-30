Forked from amethyst project [Amethyst](https://github.com/rckarns8/amethyst)
Written 2023, by Rachael Storo. Based on a workflow written by Nastassia Patin.
v. 1.0
# Important notes:
- Amethyst requires python >3.6 
- Amethyst requires data files to be located in amethyst/00_data/fastq, separated in R1 for forward reads, R2 for reverse.

# Setup

# Conda Environments
```
mamba create -n snakemake -c conda-forge -c bioconda snakemake
mamba create -n amethyst-testing-qc -c conda-forge -c bioconda fastqc multiqc  
mamba create -n amethyst-testing-mt -c conda-forge -c bioconda -c kgerhardt multitrim pigz fastp seqtk falco faqcs
mamba create -n amethyst-testing-as -c conda-forge -c bioconda megahit seqkit
```

# Running the workflow
```
mamba activate snakemake
snakemake --use-conda --cores
```
