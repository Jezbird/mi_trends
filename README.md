# mi_trends

Reference Information
=====================

Provenance for this README
--------------------------

* File name: README_Dataset-MacSeabirdTrends_v0.1.0.txt
* Authors: Jeremy P. Bird
* Date created: 2022-11-07
* Date modified: 2022-11-07

Dataset Version and Release History
-----------------------------------

* Current Version:
  * Number: 1.0.0
  * Date: 2022-11-07
  * Persistent identifier: 
  * Summary of changes: n/a

* Embargo Provenance: n/a
  * Scope of embargo: n/a
  * Embargo period: n/a

Dataset Attribution and Usage
-----------------------------
# Title of Dataset: Data for the article "Comparing the responses of extant and extirpated seabirds to the world’s largest multi-predator eradication"
---

* License: Use of these data is covered by the following license:
  * Title: CC0 1.0 Universal (CC0 1.0)
  * Specification: https://creativecommons.org/publicdomain/zero/1.0/; the authors respectfully request to be contacted by researchers interested in the re-use of these data so that the possibility of collaboration can be discussed. 

* Suggested Citations:

  * Dataset citation:
    > Bird, Jeremy (2022), Comparing the responses of extant and extirpated seabirds to the world’s largest multi-predator eradication, Dataset, Github https://github.com/Jezbird/mi_trends

  * Corresponding publication:
    > Bird, J.P., Fuller, R.A. and Shaw, J.D. 2022. Comparing the responses of extant and extirpated seabirds to the world’s largest multi-predator eradication.

Contact Information
-------------------

  * Name: Jeremy P. Bird
  * Affiliations: Centre for Biodiversity and Conservation Science, University of Queensland; Institute for Marine and Antarctic Studies, University of Tasmania
  * ORCID ID: https://orcid.org/0000-0002-7466-1755
  * Email: jezbird@gmail.com 
  * Alternate Email: jez.bird@utas.edu.au
  * Alternate Email 2: jez.bird@uq.edu.au
  * Address: e-mail preferred

- - -

Additional Dataset Metadata
===========================

Acknowledgements
----------------
The authors thank Noel Carmichael and Tasmania Parks and Wildlife Service for their support facilitating this project. The analysis includes data collected and curated by the Department of Natural Resources and Environment. Thanks to Toby Travers for suggestions for data manipulation and analysis, and to past Wildlife Rangers from Macquarie Island for their help interpreting data, in particular Helen Achurch, Julie McInnes, Marcus Salton and Penny Pascoe. We thank Rachael Alderman, Aleks Terauds and Nigel Brothers for insightful discussions and historical context. 

* Approvals/permits: All methods were approved by the University of Queensland Native/Exotic Wildlife and Marine Animals (NEWMA) animal ethics committees (AE29713), the Macquarie Island Research Advisory Group and the Department of Primary Industries, Parks, Water and Environment (TFA 17305). Access to Macquarie Island was granted by the Tasmania Parks and Wildlife Service (Access Authority No. 17-18 5).

* Funding sources: This study was supported by funding from the Australian Government’s National Environmental Science Program through the Threatened Species Recovery Hub, and the Australian Antarctic Science program (AAS 4305). JB was supported by a Research Training Program scholarship, an Antarctic Science International Bursary, National Environmental Science Programme Threatened Species Recovery Hub Research Support and a BirdLife Australia Stuart Leslie Bird Research Award.  

Description of data
-------------------

* For analysis of species distributions whole-island raster layers of predicted Antarctic Prion and White-headed Petrel density, and a vector grid of observed Blue Petrel and Grey Petrel densities on Macquarie Island were used. These layers were taken from Bird, J.P., Terauds, A., Fuller, R.A., Pascoe, P.P., Travers, T.D., McInnes, J.C., Alderman, R. and Shaw, J.D., 2022. Generating unbiased estimates of burrowing seabird populations. Ecography, p.e06204.

* For adjusting burrow density to population density estimates of burrow occupancy were used. These estimates were taken from Bird, J.P., Fuller, R.A., Pascoe, P.P. and Shaw, J.D., 2022. Trialling camera traps to determine occupancy and breeding in burrowing seabirds. Remote Sensing in Ecology and Conservation, 8(2), pp.180-190.

* For comparing contemporary distributions with historic distributions of Antarctic Prions and White-headed Petrels from the 1970s we used data from Brothers, N. P. 1984. Breeding, distribution and status of burrownesting petrels at Macqaurie Island. – Aust. Wildl. Res. 11: 113–131.

* For analysing species habitat use we compared the density layers above with environmental variables derived from a 5-m resolution digital elevation model and QuickBird satellite imagery from Bricher, P. K. et al. 2013. Mapping sub-Antarctic cushion plants using random forests to combine very high resolution satellite imagery and terrain modelling. – PLoS One 8: e72093.

* For analysing species trends we repeated visits to established monitoring plots on Macquarie Island in 2017-2018 completing burrow searches and burrow checks to develop burrow counts and breeding data. These were compared with equivalent data from previous years reported in:

Warham, J., 1967. The white-headed petrel Pterodroma lessoni at Macquarie Island. Emu-Austral Ornithology, 67(1), pp.1-22.
Brothers, N. P. 1984. Breeding, distribution and status of burrownesting petrels at Macqaurie Island. – Aust. Wildl. Res. 11: 113–131.
Schulz, M. et al. 2006. Breeding of the grey petrel Procellaria cinerea on Macquarie Island: population size and nesting habitat. Emu 105: 323–329.
Brothers, N. and Bone, C. 2008. The response of burrow-nesting petrels and other vulnerable bird species to vertebrate pest management and climate change on sub-Antarctic Macquarie Island. – Pap. Proc. R. Soc. Tasman. 142: 123–148.
Department of Natural Resources and Environment, Tasmania, unpublished data.


- - -

Methodological Information
==========================

* Methods of data collection/generation: see manuscript for details

- - -

Data and File Overview
======================

Table of Contents
-----------------

* analysis.Rmd
* analysis_data1.RData
* analysis_data2.RData
* analysis_data3.RData
* lambda.xlsx

Setup
-----

* Recommended software/tools: RStudio 2022.07.1 ; R version 4.2.1

- - -

File/Folder Details
===================

This dataset contains an R Markdown file which runs the analysis presented in Bird et al. 2022 using three .RData files:

## analysis_data1.RData

The RData file contains a number of R objects used in the analysis. In alphabetical order these are:
"ap_occ" - Antarctic Prion burrow occupancy estimate for adjusting burrow density to population density. From Bird et al. 2021
"ap_raster" - raster layer of predicted Antarctic Prion burrow density from Bird et al. 2022
"ccoast" - spatial layer of Macquarie Island coastline for plotting
"dem" - digital elevation model for environmental analysis. From Bricher et al. 2013
"dsm_ap_nb3" - density surface model of Antarctic Prion density in relation to spatial environmental variables. From Bird et al. 2022
"gdat_bp" - spatial grid of Blue Petrel density
"gdat_gp" - spatial grid of Grey Petrel density

Missing variables import into R as "NA". 

## analysis_data2.RData

The RData file contains a number of R objects used in the analysis. In alphabetical order these are:
"bros" - spatial grid of 1970s Antarctic Prion and White-headed Petrel estimated abundance from Brothers 1984
"bros_q" - quantiles used to define categories of estimated abundance from Brothers 1984
"dat" - time series data of burrow counts and breeding data from species monitoring plots derived from Warham 1967, Brothers 1984, Schulz et al. 2006, Brothers and Bone 2008, DNRE unpublished data and this study
"dsm_whp_tw2" - density surface model of White-headed Petrel density in relation to spatial environmental variables. From Bird et al. 2022
"seg_ap" - raw transect data for Antarctic Prions, divided into segments for habitat analysis. From Bird et al. 2022
"seg_whp" - raw transect data for White-headed Petrel, divided into segments for habitat analysis. From Bird et al. 2022 
"whp_cocc" - White-headed Petrel burrow occupancy estimate for adjusting burrow density to population density. From Bird et al. 2021   
"whp_raster" - raster layer of predicted White-headed Petrel burrow density from Bird et al. 2022

Missing variables import into R as "NA". 

## analysis_data3.RData

The RData file contains an R object used in the analysis:
"sta" - raster stack of spatial environmental layers for habitat analysis. Derived from Bricher et al. 2013

Missing variables import into R as "NA". 

## lambda.xlsx

This file contains calculations of lambda (population growth rate) presented in the paper


Sharing/access Information
==========================

Links to other publicly accessible locations of the data: The data will be available via the Australian Antarctic Data Centre - https://data.aad.gov.au/

Was data derived from another source? No
If yes, list source(s): NA
