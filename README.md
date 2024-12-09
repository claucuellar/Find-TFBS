# Find-TFBS
Python code for finding Transcription Factor Binding Sites (TFBSs) in DNA Sequences from fasta files. 

## Overview
This project consists of two scripts for finding user specified Transcription Factor Binding Sites (TFBSs) in multi-sequence .fasta files and analysing the results. 

The first script (`TFBS.py`) finds all the TFBSs in DNA sequences from a fasta file, in both its forward and reverse string. This script returns a tab-separated text file, named `TFBS_found.txt`, with the following information/columns:
* ID :  DNA sequence ID from the fasta file
* Direction : forward or reverse strand
* Sequence : DNA sequence
* TFBS : TFBSs sequence found

The second script (`TFBS_analysis.py`) takes the output file from the first script to run the analysis of the results. First it finds the DNA sequences that did not have any TFBS. Then it finds the top 10 most common TFBSs found in all the sequences from the fasta files. The results are returned in the terminal.

Test are also provided for each script. 

## Installation
### Prerequisites
- Make sure you have Python installed
- Required packages: `biopython`, `pandas`, `seaborn`, `matplotlib`

## How to Run the Code
### Install the required packages
**1. Install the necessary libraries:**
```bash
pip install biopython pandas seaborn matplotlib
```

### Finding the TFBS
**2. Run the first script `TFBS.py`**

To run this code, use the following command:
```
python TFBS.py <fasta_file> <consensus_sequence>
```
_Example:_
```
python TFBS.py RelA.fasta GGGRNWYYCC
```

<ins>Output</ins>

After running this script, it will generate a tab-separated text file named `TFBS_found.txt` as an output file containing all the TFBSs found in each DNA sequence strand from the input file (fasta file).

### Analysing the TFBS found  
**3. Run the second script `TFBS_analysis.py`.**

This code has an optional argument to plot the results, the default being True

To run this code, use the following command:
```
python TFBS_analysis.py <text_file> [True/False]
```
_Example:_
```
python TFBS_analysis.py TFBS_found.txt False
```
or
```
python TFBS_analysis.py TFBS_found.txt
```

### Testing
**4. Run the test codes**

Run the test for both files at the same time:
```
pytest -v
```
or run the test for each file separately:
```
pytest -v test_TFBS.py
```
```
pytest -v test_TFBS_analysis.py
```
