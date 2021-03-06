# callpeaks

Custom peak caller for CUT&amp;TAG data relies heavily on the [Regulatory Genomics Toolbox](https://github.com/CostaLab/reg-gen) API. 

## Setup

Clone this repository, or download the file `wget https://github.com/maxsonBraunLab/callpeaks/blob/master/callpeaks.py`. Then set up dependencies using conda.

```
# create a conda environment with necessary dependencies
conda create -n callpeaks numpy pandas scipy python
conda activate callpeaks
pip install rgt

./callpeaks.py -h
usage: callpeaks.py [-h] -b BAM -o OUTFILE -cs CHROMSIZES [-pv PVALUE] [-md MAXDUPS] [-cp CORRECT_PVAL]

Call peaks on CUTTAG bam files

optional arguments:
  -h, --help            show this help message and exit
  -b BAM, --bam BAM     Bam file
  -o OUTFILE, --outfile OUTFILE
                        Output prefix (filename without extension)
  -cs CHROMSIZES, --chromsizes CHROMSIZES
                        Genome chromsizes file
  -pv PVALUE, --pvalue PVALUE
                        Pvalue threshold for binomial peak test (default 0.05)
  -md MAXDUPS, --maxdups MAXDUPS
                        Maximum number of duplicates to keep for coverage signal (-1: all, 0: none, default: -1)
  -cp CORRECT_PVAL, --correct-pval CORRECT_PVAL
                        Correct p-values for multiple testing using Benjamini/Hochberg ("bh") or Benjamini/Yekutieli ("by") method
```

