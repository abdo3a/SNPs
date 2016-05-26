# SNPs
A Simple Pipeline to Assess Genetic Diversity Between Bacterial Genomes

This simple tool calculates pairwise SNPs for every possible combination in the genomes provided as input.

-	SSRG.pl generates FASTQ datasets from fasta files at user specified read lengths, with coverages of 50X or 100X. Note that this works only for haploid genomes. This tool is especially useful to compare genomes in databases for which sequencing reads are unavailable.
-	get_SNPs.pl maps FASTQ files provided against references genomes using BWA, Bowtie2 or HISAT2, as specified by the user. SNPs and indels (optional) are then calculated with Samtools + VarScan2.
-	SNPs reported in the VCF files can be summarized with count_SNPs.pl.

Requirements:
Unix/Linux or MacOS X
Perl 5
BWA - http://bio-bwa.sourceforge.net/
Bowtie2 - http://bowtie-bio.sourceforge.net/bowtie2/index.shtml
HISAT2 - https://ccb.jhu.edu/software/hisat2/index.shtml
Samtools - http://www.htslib.org/
VarScan2 - http://dkoboldt.github.io/varscan/