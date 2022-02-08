# BED_miRNA_seed_extractor

R script that calculates the start and end coordinates of the seed region of a mature miRNA from a BED file and write a BED output file with the coordinates of each seed region.

Basic idea:

-   Calculates the start and end coordinates of the seed region of a mature miRNA taking into account the length of the seed region and the sense of the strand.

------------------------------------------------------------------------

## Requirements

#### Software:

|           Requirement           | Version | Required Commands \* |
|:-------------------------------:|:-------:|:--------------------:|
| [R](https://www.r-project.org/) |  3.4.4  |    See R packages    |

\* These commands must be accessible from your `$PATH` (*i.e.* you should be able to invoke them from your command line).

#### R packages:

| Requirement | Version | Required Commands |
|:-----------:|:-------:|:-----------------:|
|    dplyr    |  1.0.7  |   mutate, %\>%    |

\* These commands must be accessible from your `$PATH` (*i.e.* you should be able to invoke them from your command line).

### Installation

Download BED_miRNA_seed_extractor from Github repository:

    git clone https://github.com/Ed-G655/BED_miRNA_seed_extractor.git

------------------------------------------------------------------------

#### Test

To test BED_miRNA_seed_extractor execution using test data, run:

    Rscript --vanilla extract_mirna_regions.R ./test/sample.bed output_sample.bed

A example output BED file should be writed in your working directory (output_sample.bed):

    chr1    17383   17390   hsa-miR-6859-3p .       -       miRNA_seed
    chr1    17423   17430   hsa-miR-6859-5p .       -       miRNA_seed
    chr1    30438   30445   hsa-miR-1302    .       +       miRNA_seed
    chr1    187905  187912  hsa-miR-6859-3p .       -       miRNA_seed

------------------------------------------------------------------------

### Usage

To run BED_miRNA_seed_extractor go to the R script directory and execute:

    Rscript --vanilla extract_mirna_regions.R <Path to your BED mature miRNA file> <Output BED file name>

### Example input

You should use a BED file with the mature miRNA coordinates, with 6 first features as described on the [UCSC Genome Browser website](https://www.ensembl.org/info/website/upload/bed.html):

    chr1    17368   17391   hsa-miR-6859-3p .       -       .       miRNA
    chr1    17408   17431   hsa-miR-6859-5p .       -       .       miRNA
    chr1    30437   30458   hsa-miR-1302    .       +       .       miRNA
    chr1    187890  187913  hsa-miR-6859-3p .       -       .       miRNA
    chr1    187930  187953  hsa-miR-6859-5p .       -       .       miRNA

#### Autors

José Eduardo García López
