# codon_analizer
Script to retrieve particular codon positions

by Andrés Culasso PhD
usage:

$ readpositions pos_profile bamdir outdir

This script require bioalcidaejdk, awk and sed to work.
bioalcidaejdk was developed by Pierre Lindenbaum PhD and could be downloaded and insalled
from here: https://github.com/lindenb/jvarkit

The rest of the programs probably are already installed in your linux distribution.
pos_profile must contain three fields:

1.- refname: is the name of chromosome or reference sequence used to assemble the reads
2.- startpos: is the position name (relative to refname sequence) where the codon start
3.- outputname: some suffix used to create a result file, for example the codon desingation

If you want to read more than a codon, change the third line in codon_read_template.js to
include more than 3 nucleotides (change the 3 in "endpos=startpos+3" for your choice)
bamdir: folder where bam (and bai, since alignment must be indexed) files will be read.
outdir: folder where multiple .csv files containig the codon counts for each position listed
        in pos_profile
