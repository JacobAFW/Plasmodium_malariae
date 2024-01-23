# An automated variant calling pipeline for novel organisms

- fastq > unfiltered VCF.
- designed using Plasmodium knowlesi, but also tested on P. falciparum and P. malariae.
- includes consensus approach to variant calling - call with both GATK and bcftools and take a consensus of outputs to produce conservative variant set.
- config/config.yaml has all inputs that need to be amended to run pipeline.
- pipeline is set up to run within a PBS management system, but can be run without by just running the Snakefile in the terminal with the appropriate environment loaded.
- the Snakefile in the bootstrap directory is a simplified version of the pipeline (no BQSR or indel realignment) needed to produce sets of high quality SNPs and Indels for recalibration steps. We peform hard filtering a set of annotations, which in combination with our consensus variant calling approach produces a set of very high quality variants.