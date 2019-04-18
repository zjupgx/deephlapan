# DeepHLApan

   DeepHLApan is a deep learning approach used for predicting high-confidence neoantigens by considering both the presentation possibilities of mutant peptides and the potential immunogenicity of pMHC.


## Download

Download the latest version of DeepHLApan from https://github.com/jiujiezz/deephlapan
    
    git clone https://github.com/jiujiezz/deephlapan.git

## Installation

Unzip the source code and go into the directory by using the following command:

    tar xvzf deephlapan-*.tar.gz

    cd deephlapan

Invoke the setup script:

    sudo python setup.py install


## General usage

Single peptide and HLA:

    deephlapan -P LNIMNKLNI -H HLA-A02:01 

List of peptides and HLA alleles in a file:

    deephlapan -F [file] -O [output directory]  

## Input files

DeepHLApan takes csv files as input with head of "Annotation,HLA,peptide" (requisite). 
It supports to rank the HLA-peptide pairs if all the mutant peptides belong to one sample. 

For example (demo/1.csv):
    
      Annotation,HLA,peptide
      NCI-3784,HLA-A01:01,MKRFVQWL
      NCI-3784,HLA-A03:01,MKRFVQWL
      NCI-3784,HLA-B07:02,MKRFVQWL
      NCI-3784,HLA-B07:02,MKRFVQWL
      NCI-3784,HLA-C07:02,MKRFVQWL
      NCI-3784,HLA-C07:02,MKRFVQWL
      NCI-3784,HLA-A01:01,KRFVQWLK
      NCI-3784,HLA-A03:01,KRFVQWLK
      NCI-3784,HLA-B07:02,KRFVQWLK
      NCI-3784,HLA-B07:02,KRFVQWLK
      NCI-3784,HLA-C07:02,KRFVQWLK
      NCI-3784,HLA-C07:02,KRFVQWLK
 
 The content in Annotation can be changed as users wanted.
 
