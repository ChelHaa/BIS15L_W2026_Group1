MS Title: Nectar bacteria stimulate pollen germination and bursting to enhance their fitness 
MS Authors: S M Christensen, I Munkres, R L Vannette 
MS Journal: 

===================================================================================

**FILES' NAMES AND CONTENTS**
pollen_microbe_data.csv
- The file is a comma delimited file. Data on pollen germination and bursting with different microbial treatments

MALDI_identifications.csv
- The file is a comma delimited file. Data on identifications of microbes after assay completion using MALDI-TOF + Compass Explorer

dose_dependence-data.csv
- The file is a comma delimited file. Data on proportion of grains germinated with different dilutions of A. pollinisSCC477 over time.

tube_lengths_dose_dependence_data.csv
- The file is a comma delimited file. Data on lengths of pollen tubes over time and with different dilutions of A. pollinisSCC477

growthcurver_data_dose_dep_each_well.csv
- The file is a comma delimited file. Data is formatted from 'dose_dependence-data.csv' to work with "GrowthCurver" package.

growthcurver_data_dose_dep_by_treatment.csv
- The file is a comma delimited file. Data is from 'growthcurver_dose_dep_each_well.csv' as averages of the three replicates, and in the format for use by  "GrowthCurver" package.

Apollinis_benefit_data.csv
- The file is a comma delimited file. Data on microbial hemocytometer counts of A. pollinis, when provided different pollen treatments. 

yeast_benefit_data.csv
- The file is a comma delimited file. Data on microbial hemocytometer counts of M. reukaufii, when provided different pollen treatments.

Lowry_data1.csv
- The file is a comma delimited file. Data on protein in solution after pollen (germinable or ungerminable or no pollen) exposure to SCC477 (or no inoculation). 

germ_AN.csv
- The file is a comma delimited file. Data on germination and bursting after pollen (germinable or ungerminable) exposure to SCC477 (or no inoculation). 


===================================================================================

**FILES' STRUCTURES AND UNITS OF MEASUREMENTS**

pollen_microbe_data.csv
The file is a comma delimited file.
Column headings are in the following order and format:

Microbe.group	
- The classification of the microbe added 

Microbetreatment
- The integrally used strain number of the microbe added (coded to species name in R code)
	
Trial.date
- The date of the assay
	
Assay.replicate
- The biological replicate (within microbe treatment) 

Timepoint
- In minutes, the time elapsed since microbes and pollen were mixed in the assay
	
standardized.OD.plate
- The OD600 of the microbe when mixed in the plate (so diluted 1:1 from initial OD600s of .1 and .05)

Total.pollen	
- The total number of pollen grains captured in the image, not including those that touch the outer perimeter of the image
 
number.germ
- The number of pollen grains with protruding pollen tubes in the image that are intact (not "tip burst") 	

number.burst	
- The number of pollen grains with no visible pollen tube, but releasing protoplasm

number.tip.burst
- The number of grains that germinated and the tip of the tube released protoplasm
	
Prop.germ
- The proportion of pollen grains that germinated (eg number.germ/Total.pollen)
	
Prop.burst
- The proportion of pollen grains that burst (eg number.burst/Total.pollen)
	
Prop.tip.burst	
- The proportion of pollen grains that burst at the tip of the pollen tube (eg. number.tip.burst/ Total.pollen)

allgerm	
- The proportion of pollen grains that germinated, including both "number.germ" and "number.tip.burst"  

allburst
- The proportion of pollen grains that expelled protoplasm into solution, including both "number.burst" and "number.tip.burst" 

===================================================================================
MALDI_identifications.csv

The file is a comma delimited file.

Column headings are in the following order and format:

Trial Date
- The date of the assay for which the identifications are being made	

Inoculation source:
- The well of the assay plate that the microbe was plated (onto agar plate) from. 

Microbe Inoculated:	
- The microbe that was added, or if none, what the source of the microbes were (eg pollen plated directly without inoculation) 

Microbe IDed on MALDI:	
- The microbe that the MALDI-TOF + Compass Explorer identified as the top hit for that spot

NCBI identifier	Score	
- The NCBI identifier of the microbe that Compass Explorer identified as the top hit for that spot

Genus match?	
- "yes" if genus IDed was the same as genus inoculated

Species match?	
- "yes" if species IDed was the same as species inoculated

Trial Type
- "Dose Dependence" for the trial of A. pollinis dose comparison, "Microbe Assay" for the trials comparing different microbes for their effects on pollen

notes
- important caveats and information that did not fit elsewhere
===================================================================================
dose_dependence_data.csv

 The file is a comma delimited file. 

Column headings are in the following order and format:

Trial date	
- The date of the assay

image ID	
- The ID of the image used, corresponds to the dilution (letter) and replicate (number)

Microbetreatment
- The dilution of A. pollinis used 
	
Assay replicate	
- The biological replicate, 3 per dilution level

Minutes	
- Time in minutes since microbes and pollen were mixed in the assay

Total.pollen	
- The total number of pollen grains captured in the image, not including those what touch the outer perimeter of the image
 
number.germ
- The number of pollen grains with protruding pollen tubes in the image that are intact (not "tip burst") 	

number.burst	
- The number of pollen grains with no visible pollen tube, but releasing protoplasm

number.tip.burst
- The number of grains that germinated and the tip of the tube released protoplasm
	
Prop.germ
- The proportion of pollen grains that germinated (eg number.germ/Total.pollen)
	
Prop.burst
- The proportion of pollen grains that burst (eg number.burst/Total.pollen)
	
Prop.tip.burst	
- The proportion of pollen grains that burst at the tip of the pollen tube (eg. number.tip.burst/ Total.pollen)

allgerm	
- The proportion of pollen grains that germinated, including both "number.germ" and "number.tip.burst"  

allburst
- The proportion of pollen grains that expelled protoplasm into solution, including both "number.burst" and "number.tip.burst" 

===================================================================================
tube_lengths_dose_dependence_data.csv

The file is a comma delimited file. Data is structured in columns, each row representing a single pollen tube. Column headings are in the following order and format:

Minutes
- The number minutes elapsed since T0

Time_l
- The time label, in minutes (m) or hours (h) since T0

Dilution
- The dilution of A. pollinisSCC477 used in that well

Well
- The ID of the well (letter corresponds to dilution, number to replicate) 

Tube number
- Differentiates tubes within a well

length
- The length of the germinated tube, in (um), when traced along the center line of the tube.  
===================================================================================
growthcurver_data_dose_dep_each_well.csv

 The file is a comma delimited file. Data is structured with 'time' as the first column, and individual wells (replicates) as other columns. This is the required format for the growcurver package used in the dose dependence curve analysis R script

time 
- In minutes.

The other columns are named with the letter encoding the dilution, and the number indicating the replicate (3 replicates of each) 
	a= full dose (OD .1 A. pollinis)
	b= 1:2 dilution of OD .1 A. pollinis
	c= 1:3
	d= 1:5
	e= 1:20
	f= 1:100
	g= no microbes added


===================================================================================
growthcurver_data_dose_dep_by_treatment.csv

 The file is a comma delimited file. Data is structured with 'time' as the first column, and averages of the three individual wells (replicates) in the other columns. This is the required format for the growcurver package used in the dose dependence curve analysis R script

Column headings are in the following order and format

time	
- In minutes

full_dose
- The proportion of germinated grains at each timepoint when A. pollinis solution added was the full dose (OD600= 0.1)

dil2
- The proportion of germinated grains at each timepoint when A. pollinis diluted 1:2
	
dil3	
- The proportion of germinated grains at each timepoint when A. pollinis diluted 1:3

dil5	
- The proportion of germinated grains at each timepoint when A. pollinis diluted 1:5

dil20	
- The proportion of germinated grains at each timepoint when A. pollinis diluted 1:20

dil100	
- The proportion of germinated grains at each timepoint when A. pollinis diluted 1:100

no_microbes
- The proportion of germinated grains at each timepoint when sterile BK added, no microbes


===================================================================================
Apollinis_benefit_data.csv
- The file is a comma delimited file.

Column headings are in the following order and format:

Treatment_l
- Indicates the treatment of the pollen and whether or not A. pollinis was added. FP= Fresh pollen (directly from flowers) UP= ungerminable pollen (microwaved for 3 minutes in liquid BK media to render unable to germinate) 

Tube
- The tube label, three replicates per treatment

initial count
- The number of cells per mL at the start of the assay for each replicate, as counted on hemocytometer 

final count-24h 
- The number of cells per mL at the 24 hour timepoint for each replicate, as counted on hemocytometer

Date
- The date the assay was started (day of initial count)

===================================================================================

yeast_benefit_data.csv
- The file is a comma delimited file. Data on microbial hemocytometer counts of M. reukaufii, when provided different pollen treatments. 


Column headings are in the following order and format:

Treatment_l
- Indicates the treatment of the pollen and whether or not M. reukauffi was added. FP= Fresh pollen (directly from flowers) UP= ungerminable pollen (microwaved for 3 minutes in liquid BK media to render unable to germinate) 

initial count
- The number of cells per mL at the start of the assay for each replicate, as counted on hemocytometer 

24h count
- The number of cells per mL at the 24 hour timepoint for each replicate, as counted on hemocytometer

Date
- The date the assay was started (day of initial count)
===================================================================================

Lowry_data1.csv
- The file is a comma delimited file. Data on protein in solution after pollen (germinable or ungerminable or no pollen) exposure to SCC477 (or no inoculation). 

Column headings are in the following order and format:

row	
- Indicates the row of the 96 well plate

column	
- Indicates the column of the 96 well plate 

Timepoint
- The time at which the measurement was taken relative to when microbes and pollen were combined in the plate.	

Well ID	

- The combined column and row values
	
protein 
- The ug/mL of proetein In the well after correction by dilution factor (4)

Treatment
- Combined pollen and microbe treatment

microbetreatment
- Indicates presence (477) or absence (ctrl) of SCC477

pollentreatment
- Indicates pollen treatment (fresh= germinable pollen,  ungerm= ungerminable, or no pollen)

Date
- Date the assay was started (eg time 0)

===================================================================================

germ_AN.csv
- The file is a comma delimited file. Data on germination and bursting after pollen (germinable or ungerminable) exposure to SCC477 (or no inoculation). 

Treatment
- Combined microbe and pollen treatment: 477= presence of SCC477, ctrl= no inoculation, GP= germinable pollen, UP= ungerminable pollen.

pollentreatment	
- pollen treatment: GP= germinable pollen, UP= ungerminable pollen

Timepoint
- The time at which the measurement was taken relative to when microbes and pollen were combined in the plate.	

image name
- Image name corresponds to 96 well plate well location
	
total
- Total pollen grains in image	

burst
- Number of burst grains in image
	
germ
- Number of germinated pollen grains in image
	
tipburst
- Number of pollen grains that have germinated the burst
	
allgerm	
- combined germinated and tip burst

allburst
- combined tip burst and burst
	
Date
- Date the assay was started (eg time 0) 	



**DATA QUESTIONS**
Questions about data can be addressed to Shawn Christensen (smchristensen@ucdavis.edu) 