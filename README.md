## RNA-seq Analysis using nf-core/rnaseq

This repository contains a pipeline for RNA-seq analysis using the `nf-core/rnaseq` workflow. The pipeline is designed to be run using Nextflow and Docker/Singularity, ensuring reproducibility and ease of use. 

The nf-core/rnaseq pipeline is a bioinformatics tool designed for the analysis of RNA sequencing data from organisms with an available reference genome and annotation. It processes a samplesheet and FASTQ files, conducting quality control (QC), trimming, and (pseudo-)alignment. The pipeline outputs a gene expression matrix along with a comprehensive QC report. This RNA-seq analysis pipeline employs STAR, RSEM, HISAT2, or Salmon for generating gene and isoform counts, as well as performing thorough quality control checks.


## Methods
Data was processed using nf-core/rnaseq v3.14.0 (doi: https://doi.org/10.5281/zenodo.1400710) of the nf-core collection of workflows (Ewels et al., 2020), utilising reproducible software environments from the Bioconda (Grüning et al., 2018) and Biocontainers (da Veiga Leprevost et al., 2017) projects.

The pipeline was executed with Nextflow v24.04.2 (Di Tommaso et al., 2017) with the following command:

```
nextflow run nf-core/rnaseq --input scripts/samplesheet.csv --outdir results --genome BDGP6 -profile docker -c custom.config
```

## References
* Di Tommaso, P., Chatzou, M., Floden, E. W., Barja, P. P., Palumbo, E., & Notredame, C. (2017). Nextflow enables reproducible computational workflows. Nature Biotechnology, 35(4), 316-319. doi: 10.1038/nbt.3820
* Ewels, P. A., Peltzer, A., Fillinger, S., Patel, H., Alneberg, J., Wilm, A., Garcia, M. U., Di Tommaso, P., & Nahnsen, S. (2020). The nf-core framework for community-curated bioinformatics pipelines. Nature Biotechnology, 38(3), 276-278. doi: 10.1038/s41587-020-0439-x
* Grüning, B., Dale, R., Sjödin, A., Chapman, B. A., Rowe, J., Tomkins-Tinch, C. H., Valieris, R., Köster, J., & Bioconda Team. (2018). Bioconda: sustainable and comprehensive software distribution for the life sciences. Nature Methods, 15(7), 475–476. doi: 10.1038/s41592-018-0046-7
* da Veiga Leprevost, F., Grüning, B. A., Alves Aflitos, S., Röst, H. L., Uszkoreit, J., Barsnes, H., Vaudel, M., Moreno, P., Gatto, L., Weber, J., Bai, M., Jimenez, R. C., Sachsenberg, T., Pfeuffer, J., Vera Alvarez, R., Griss, J., Nesvizhskii, A. I., & Perez-Riverol, Y. (2017). BioContainers: an open-source and community-driven framework for software standardization. Bioinformatics (Oxford, England), 33(16), 2580–2582. doi: 10.1093/bioinformatics/btx192
