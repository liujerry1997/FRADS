# FRADS

FRADS: Finding RBP Associations with Disease SNPs. A pipeline for processing ENCODE eCLIP data to find association between RBP binding and disease related SNPS.

## INTRODUCTION:
A 03-713 Bioinformatics Practicum project. It is focused on finding disease-associated SNP in RBP binding sites using eCLIP data and integrating various bioinformatics tools including Cutadapt, PrinSeq, STAR, PureCLIP, bedtools.


### Prerequisites
WARNING: This program needs to run on computers that have slurm activated (i.e. on PSC server, clustering servers).
PrinSeq (0.20.4)
cutadapt(v1.12)
samtools(v1.9)
STAR(v2.7 or above)
PureCLIP(v1.3.1)
bedtools(v2.92.1)


### Installing

To install, clone files from github.
$ git clone 

AFTER INSTALLATION
```
Use $ source Build.sh To install all required software in our pipeline
Enter $ ./FRADS -h to see if software was properly installed.
```


## USAGE

To perform a quick run of the file, enter the fastq file and the assembly line number: (19 or 38)

### Commands:
Check additional information by having -h or --help as the parameter.

Explain what these tests test and why

```
$ python FRADS.py -h
```

Some modules can be modified by specifying them in parameters. For now we support the modification below:
```
    -r1                     Fastq file name of read #1
    -r2                     Fastq file name of read #2
    -ass|--assembly <int>  Specify mapping assembly (‘38’ or ‘19’)
    -o|--output <string>    Specify output file name.
```

### Example:

```
$ python FRADS.py -r1 ENCFF651RTO -r2 ENCFF947CCD -ass 38
```

### OUTPUT:
The output will be a .bed file that contains all the crosslink site SNPs in an ENCODE dataset that are doubly associated with diseases and RBP binding. The output will list the SNP along with the disease it is associated with.

## Authors
Communications Lead:  Sabrina Tsai
Lead Technical Writer: Ruhi Naik
Q&A Lead/Technical Lead: Yen-Tso Cheng
Program Manager: Haodong Liu


## Acknowledgments
Thanks to developers of:
PrinSeq (0.20.4)
cutadapt(v1.12)
samtools(v1.9)
STAR(v2.7 or above)
PureCLIP(v1.3.1)
bedtools(v2.92.1)

