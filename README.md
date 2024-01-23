# Plasmodium_malariae

- This repo contains scripts and pipelines for producing a VCF and performing any associated analyses for the Plasmodim malariae parasite.
- Due to the Pm being a non-model orgnanism, a boostrapping approach had to be taken for calling variants. 
- This involved running a simplified version of [THIS](https://github.com/JacobAFW/Variant_Calling_Pipeline) pipeline, and then runnning the original version of the pipeline using a high-quality subset of the variants produced previously for recalibration steps (updating known_indels_path & known_sites_path in config.yaml).
- This is the GATK [recomended approach](https://gatk.broadinstitute.org/hc/en-us/articles/360035890531-Base-Quality-Score-Recalibration-BQSR-) for non-model organisms.
