# ChromeHMM Analysis

### Determination of combination of histone marks that are characteristic of each of N different Epigenetic types by manually assigning to each of the N epigenetic types a possible biological function

### By Joseph Luper Tsenum

Email: tsenumjosephluper@phystech.edu

Phystech School of Biological and Medical Physics (FBMF)

Moscow Institute of Physics and Technology (National Research University)

Russian Federation


### Introduction

#### Input Directory

Luperjoseph > ChromHMM

#### Output Directory 

MYOUTPUT

### Types of Cells Used

#### Assembly

hg18

#### Number of States

10

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

#### Chromosome Used

Human genome (version hg19)

#### Packages Used

ChromHMM for annotaion, UCSC GenomeBrowser, Baum-Welsh algorithm, ChromHMM with BinarizeBam option to convert ChIP-seq profiles (bam files) into a table of 1 and 0 to create bins of the lenght of 200 bp, ChromHMM with LearnModel option to automatically detect parameters for N various genomic regions with the major histon marks and specific combinations.

### Results from ChromHMM

                              The figure below shows the emission parameters for Hmec_10
                          
![image](https://user-images.githubusercontent.com/58364462/208551815-4abf4629-511f-44fc-aad1-685e1bb3fd44.png)


                              The figure below shows Fold Enrichment for Hmec_10
                              
![image](https://user-images.githubusercontent.com/58364462/208552076-6345e433-e0bd-44ab-b973-1e3d8108260c.png)


                              Fold enrichment Hmec_10 RefSeqTES as shown below
                              
![image](https://user-images.githubusercontent.com/58364462/208552353-ff5317d2-dc9e-48df-8dc8-b6240b7634f5.png)


                              Fold enrichment Hmec_10 RefSeqTSS as shown below
                              
![image](https://user-images.githubusercontent.com/58364462/208552562-ed285280-fdd9-4b50-a531-bf05c1229ca0.png)


                              The figure below shows the transition parameters
                              
![image](https://user-images.githubusercontent.com/58364462/208552670-b85f0d40-15d4-4874-b3c5-b907269b3907.png)


#### Table with the Epigenetic States, their Features and Names

This can be found in the attached pdf file


### Visualization in UCSC GenomeBrowser

UCSC GenomeBrowser with various genomic regions and epigenetic states
   
                             Genomic regions of ChromHMM dense.bed is shown below
                             
![image](https://user-images.githubusercontent.com/58364462/208553090-471fe7be-cd14-4469-b915-469d6d007c66.png)


                             Genomic regions of ChromHMM expanded.bed is shown below
                             
![image](https://user-images.githubusercontent.com/58364462/208553231-fc7deb45-7a61-42aa-b455-45630b78aaad.png)


### Visualization of Chromatin States from ChromHMM and corresponding Histone MarksLinks

Links to panels with profiles of histone modifications with epigenetic states

• http://genome.ucsc.edu/s/Josephluper/Histone%20Marks%20in%20CromHMM%20expanded.bed

• http://genome.ucsc.edu/s/Josephluper/Histone%20Marks%20in%20CromHMM%20dense.bed


#### Link to Sessions on UCSC Genome Browser

• http://genome.ucsc.edu/s/Josephluper/Dense.bed%20ChromHMM

• http://genome.ucsc.edu/s/Josephluper/Expanded.bed%20ChromHMM


### List of Commands Used

```bash
cd ChromHMM
```

```bash
java -mx4000M -jar ChromHMM.jar BinarizeBam -b 200
CHROMSIZES/hg19.txt chip_seq cellmarkfiletable.txt
binarizedData
```

```bash
java -mx4000M -jar ChromHMM.jar MakeBrowserFiles -c MYOUTPUT/Colors
MYOUTPUT/Hmec_10_segments.bed Hmec_colored Hmec_colored
```

```bash
java -mx4000M -jar ChromHMM.jar MakeBrowserFiles -c MYOUTPUT/Colors
Hmec_10_segments.bed Hmec_colored Hmec_colored
```

```bash
ln -s ~/bin/ChromHMM/ChromHMM.jar
```

```bash
ln -s ~/bin/ChromHMM/CHROMSIZES
```

```bash
cellmarkfiletable.txt
```
