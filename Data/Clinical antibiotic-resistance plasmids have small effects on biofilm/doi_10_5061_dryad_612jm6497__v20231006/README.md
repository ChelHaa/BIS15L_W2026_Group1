# Clinical antibiotic-resistance plasmids have small effects on biofilm formation and population growth in Escherichia coli in vitro

[https://doi.org/10.5061/dryad.612jm6497](https://doi.org/10.5061/dryad.612jm6497)
This folder contains the data for the article:
Brülisauer, L., Leon-Sampedro, R., Hall, A. R. (2023). Clinical antibiotic-resistance plasmids have small effects on biofilm formation and population growth in Escherichia coli in vitro. *Plasmid.*

Comments and requests should be addressed to Laura Brülisauer: laura.bruelisauer@env.ethz.ch. The data is free of use, but I would appreciate being told, and this dataset and the matching article cited if appropriate.

We used a combinatorial approach to test the effects of clinical antibiotic resistance plasmids on biofilm formation and population growth in clinical and laboratory Escherichia coli strains. This dataset contains biofilm and growth data for each of the 25 plasmid-host combinations and the 5 plasmid-free host strains.

## Description of the data and file structure

The file "bf\_replicates.csv" contains all biofilm data collected for 9 replicates of each strain in both LB medium and M9 Minimal medium. We measured biofilm formation using a crystal violet assay in three 96-well microplates. Briefly, we distributed 9 replicates of each strain randomly on the three microplates and incubated them for 24 hours. After incubation, we measured culture optical density (OD) before staining the attached cells with crystal violet (OD\_culture). We determined absolute biofilm formation for each replicate by measuring OD of the dissolved crystal violet (OD\_abs) and calculated a normalised biofilm formation score by dividing the absolute biofilm formation by the culture density before staining (OD\_norm). To assess the effect of plasmid introduction on biofilm formation, we calculated relative biofilm formation by dividing the normalised biofilm score of each plasmid-host combination by the mean of the normalised biofilm formation score of the respective plasmid-free host strain (OD\_norm.rel).

The file "growth\_replicates.csv" contains growth parameter data for 3 replicates of each strain in LB and M9 Minimal medium. We measured culture OD of each replicate every 15 min for 24 h. Using the growthrates (Petzoldt, 2017) and flux (Jurasinski et al., 2022) packages in R, version 0.8.2, we determined the maximum growth rate (mumax), maximum optical density (ODmax) and area under the curve (auc). We calculated relative mumax, ODmax and auc for each replicate by dividing the value of the plasmid-host combination by the mean of the respective parameter of the plasmid-free host strain.

The file "bf\_growth\_sum.csv" contains summarised data used for the figures in the article calculated using the data in "bf\_replicates.csv" and "growth\_replicates.csv", specifically the mean / median values and error measures. The columns are named using the prefixes in the biofilm and growth files with the following suffixes:
\- \.rel: relative to the plasmid\-free recipient
\- \.mean: mean
\- \.median: median
\- \.se: standard error
\- \.errorpro: propagated standard error using the formula from Silva et al\. \(2011\)\. Pervasive Sign Epistatis between Conjugative Plasmids and Drug\-Resistance Chromosomal Mutations\. *PLoS Genet.*

In all data sets, for plasmid-free host strains, the value in the "plasmid" column is NA.