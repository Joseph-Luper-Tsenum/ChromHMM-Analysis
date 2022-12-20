# ChromeHMM Analysis

### Determination of combination of histone marks that are characteristic of each of N different Epigenetic types by manually assigning to each of the N epigenetic types a possible biological function

### By Joseph Luper Tsenum

Email: tsenumjosephluper@phystech.edu

Phystech School of Biological and Medical Physics (FBMF)

Moscow Institute of Physics and Technology (National Research University)

Russian Federation


### Data Used

#### Input Directory: Luperjoseph > ChromHMM

#### Output Directory: MYOUTPUT

### Types of Cells Used

#### Assembly: hg18

#### Number of States: 10

The following .bam files were used for the experiment

• wgEncodeBroadHistoneHmecH3k09me3AlnRep1.bam

• wgEncodeBroadHistoneHmecH3k27acStdAlnRep1.bam

• wgEncodeBroadHistoneHmecH3k27me3StdAlnRep1.bam

• wgEncodeBroadHistoneHmecH3k36me3StdAlnRep1.bam

• wgEncodeBroadHistoneHmecH3k4me1StdAlnRep1.bam

• wgEncodeBroadHistoneHmecH3k4me2StdAlnRep1.bam

• wgEncodeBroadHistoneHmecH3k4me3StdAlnRep1.bam

• wgEncodeBroadHistoneHmecH3k79me2AlnRep1.bam

• wgEncodeBroadHistoneHmecH3k9acStdAlnRep1.bam

• wgEncodeBroadHistoneHmecH4k20me1StdAlnRep1.bam

Control: This control .bam file was used for all experiments

• wgEncodeBroadHistoneHmecControlStdAlnRep1.bam

#### Chromosome Used: Human genome (version hg19)

#### Packages Used

ChromHMM for annotaion, UCSC GenomeBrowser, Baum-Welsh algorithm, ChromHMM with BinarizeBam option to convert ChIP-seq profiles (bam files) into a table of 1 and 0 to create bins of the lenght of 200 bp, ChromHMM with LearnModel option to automatically detect parameters for N various genomic regions with the major histon marks and specific combinations.

### Results from ChromHMM

                               Fig.1: (a) Shows emission parameters for Hmec_10 while (b) Shows Fold Enrichment for Hmec_10
                          
![image](https://user-images.githubusercontent.com/58364462/208551815-4abf4629-511f-44fc-aad1-685e1bb3fd44.png)



#### Table with the Epigenetic States, their Features and Names

This can be found in the attached pdf file


