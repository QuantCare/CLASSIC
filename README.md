#CLASSIC

An improved in-silico method for pathogenic classification of missense genetic variants.

##Use

For inputs of CADD v1.0 (C), RVIS (R), and PROVEAN (P), calculate the CLASSIC metric as:

f(C,R,P) = 0.55141463C - 0.44124492R - 0.2671904P - 1.94571548

If more than one PROVEAN score is available, due to multiple protein isoforms, utilise the mean.

##Performance

CLASSIC performs significantly better than CADD when comparing AUC (p=1.97e-57; two-tailed, paired t-test). Comparison methods are implemented in the files described below, and outlined in the CLASSIC manuscript.

##Files

*CLASSIC.ipynb* and *CLASSIC.py* are identical in contents except that the former is a Python notebook whereas the latter is a raw Python file. They demonstrate the working to obtain the above equation. Developed and tested with Python v3.4.0.

*all-scores.tsv* is a subset of the variants supplied in the description of CADD (doi: [10.1038/ng.2892][http://dx.doi.org/10.1038/ng.2892]). The first column contains binary classification where 1 = pathogenic. Columns 2-4 contain CADD, RVIS, and mean PROVEAN scores respectively.