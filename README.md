#*In silico* analysis of the PTCome distribution on PTPs

Mutational databases usually display quantitave data, meaning the number of samples that have been detected with a mutation in certain gene, taking into account the number of times certain mutation has been described. Mutational hotspots can occur both due to the protein output of the mutation or the mutagenic chemical properties of a given nucleotide sequence, or because a mixture of both. As an example of sequences of elevated mutability, CG  TG conversions occur with relatively high frequency in Arg (R) codons (CGA), due to spontaneous reactions of deaminase enzymes. 

Nonsense mutations that led to premature termination codons (PTC) are relatively abundant in PTPs, and understanding how these are distributed along their coding sequence may provide genotype/phenotype information. We have developed this code that can be copied and run in R, to retrieve unique PTC mutations from COSMIC (cancer-associated PTCome) and HGMD (germline-asociated PTCome) databases, and represent them in a plot which we have designated Kernel density plot, based on kernel density estimation. 

##Obtention of datasets containing PTC data

For representing Kernel density plots 3 vectors are obtained using files downloaded from COSMIC (comma delimited file, .csv) and HGMD databases (excel file, .xls), and from a file with the potential PTC residues of a given cDNA obtained using the PTCMAKER program (text file, .txt; obtained using the Python-based code in the https://github.com/translational-readthrough-on-ptps/ptc-maker repository or via a program that can be installed using the .exe file for Windows in https://github.com/translational-readthrough-on-ptps/stop-codon-pulido-17). 

##Kernel density plot representation

These files are processed by three sections in this code (section #1 for the potential PTCome, section #2 for the germline-associated PTCome and section #3 for the cancer-associated PTCome). These PTComes are then represented in a kernel density plot in section #4. Of importance is that gene name and protein length must be introduced in lines 40 and 41 (PTEN name and protein length are given as examples).

