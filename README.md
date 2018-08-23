# MetabNorm
# Language: R
# Input: prefix
# Output: CSV (normalized counts)
# Tested with: PluMA 1.0, R 3.2.5

PluMA plugin that takes metabolomics data (CSV format) and applies the 
algorithm of Jauhiainen et al (2014).  The model applies mixed mode analysis based
on sampling times, and can accept a file of cohorts and a file of batches
(also in CSV format).  The user supplies a "prefix" in the configuration file,
and the resulting three files assumed by the plugin will be prefix.csv (for the data),
prefix.cohorts.csv and prefix.batches.csv.

The input file of metabolomics data should be assembled such that rows indicate
metabolites and columns indicate samples.  Cohort and batch CSV files specify
their respective data as unique identifiers, each on a separate line (see the example).

The output normalized concentrations will also be in CSV format, with rows corresponding
to metabolites and columns corresponding to samples. 
