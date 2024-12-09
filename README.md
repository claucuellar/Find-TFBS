# Find-TFBS
Python code for finding Transcription Factor Binding Sites (TFBSs) in DNA Sequences from fasta files. 

## Description
This project is a tool for finding user specified Transcription Factor Binding Sites (TFBSs) in multi sequence .fasta files. It then also analyses the TFBSs found by finding the top 10 most common TFBSs sequences found in all input sequnces as well as giving the number of sequences from the file that did not contain in TFBS. 

This project consists of two scripts for finding user specified Transcription Factor Binding Sites (TFBSs) in multi-sequence .fasta files and analysing the results. 

The first script (`TFBS.py`) finds all the TFBSs in DNA sequences from a fasta file, in both its forward and reverse string. This script returns a tab-separated text file, named `TFBS_found.txt`, with the following information/columns:
* ID :  DNA sequence ID from the fasta file
* Direction : forward ar reverse strand
* Sequence : DNA sequence
* TFBS : TFBSs sequence found

The second script takes the output file from the first script to run the analysis of the results. First it finds the DNA sequences that did not have any TFBS. Then it finds the top 10 most common TFBSs found in all the sequences from the fasta files. The results are returned in the terminal.   

There are also test for each script. 

## Installation
### Prerequisites
- Python 3.7 or higher
- Required packages: `requests`, `pandas`, `matplotlib`

## Usage 
### First script: Finding the TFBS
The first part of the proyect is the TFBS.py script. 

Explain

To run this code, use the following command:
```
python TFBS.py <fasta_file> <consensus_sequence>
```
Example:
```
python TFBS.py RelA.fasta GGGRNWYYCC
```

#### Output 
After running this script, it will generate a tab-separated text file named "TFBS_found.txt" as an output file containing all the TFBSs found in each DNA sequence strand from the input file (fasta file). 

### Second script: Analysing the TFBS found  
The second part of the project, the TFBS_analysis.py, takes the output file (TFBS_found.txt) from the first script and analyses it. 
Explain

To run this code, use the following command:
```
python TFBS_analysis.py <text_file> [True/False]
```
Example:
```
python TFBS_analysis.py TFBS_found.txt False
```
or
```
python TFBS_analysis.py TFBS_found.txt
```

#### Output 


### Tests
This project includes test for each script. 

To run the test 


#
