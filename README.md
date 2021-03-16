# viralrecon_test
Testing the [nf-core/viralrecon pipeline](https://nf-co.re/viralrecon)

Using Nextflow (installed like this: https://nf-co.re/usage/installation) and Docker.


Testing the pipeline with the command `nextflow run nf-core/viralrecon -profile test,docker`.

Could check out the Artic Illumina versin of Nextflow: https://github.com/connor-lab/ncov2019-artic-nf

Command for running only trim and Kraken2
nextflow pull nf-core/viralrecon
NXF_VER="21.03.0-edge" nextflow run nf-core/viralrecon --name TEST -profile docker --genome NC_045512.2 --outdir TEST --max_memory 8.GB --max_cpus 4 --input samplesheet.csv --protocol amplicon --amplicon_bed Data/Primers/swift_primers.bed --skip_sra true --skip_variants --skip_assembly -r dev --platform illumina --save_kraken2_fastq true -c custom.config 

