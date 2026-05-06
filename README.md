# microbiome_compost_aphid

Code and data in this repository correspond to "Aphid populations vary in a soil microbiome-dependent and compost application-independent manner" by Dixon et a. 2026. Briefly, while compost changes soil microbial communities, its application does not alter aphid populations. The soil microbiome, however, does affect aphid population dynamics.

# Descriptions of each code file

Each Rmd corresponds to the code used to generate a figure in the paper described above.

## Fig_1_Stats_FieldSoilMapMicrobes.Rmd

Description:

This file corresponds to the code used to generate figure 1. It includes code to generate a map, alpha diversity, and beta diversity.

Inputs: <br>

-   Bloom_SiteLocations.csv (for MAP fig)
-   Formatted data on samples used in analysis.xlsx (for ALPHA and BETA fig)
-   Bloom_otu_table_Bac.csv (for BETA fig)
-   Bloom_otu_table_Fun.csv (for BETA fig)
-   Bloom_taxonomy_table_Bac.csv (for BETA fig)
-   Bloom_taxonomy_table_Fun.csv (for BETA fig)
-   Bloom_sample_info.csv (for BETA fig)

Outputs: <br>

-   Figure 1
-   Figure S1
-   Results corresponding to Figures 1 and S1

## Fig_2_Stats_LabSoilMapMicrobeAphid.Rmd

-   Description: This file corresponds to the code used to generate figure 2. It includes code to generate a map, alpha diversity, and beta diversity.

Inputs:

-   seed_farm_locations.csv (MAP)
-   EJM-CLS-22F_pct98.csv (BETA)
-   EJM-CLS-22B_pct98.csv (BETA)
-   sample_data_field_switch_samples_bac.csv (BETA)
-   sample_data_field_switch_samples_fun.csv (BETA)
-   HATCH_compost_bioassay_data.xlsx (APHID)

Outputs:

-   Figure_2.svg


## Fig_3_Stats_LabVolcanoFarm.Rmd

-   Description: This file corresponds to the code used to generate figure 3. It includes code to generate volcano plots and running ANCOMBC to compare taxa that vary between two farms.  

Inputs: <br>

-   Sequencing_data_formatted_for_analysis(01.28.2026).xlsx
-   EJM-CLS-22F_pct98.csv
-   EJM-CLS-22B_pct98.csv
-   sample_data_field_switch_samples_bac.csv
 

Outputs: <br>

-   figure 3
-   ancom_bac_farm.rds
-   ancom_fun_farm.rds

## Fig_4_Stats_CrossRemAlphaBeta.Rmd


-   Description: This contains the code used to generate figure 4. Alpha and beta diversity are compared for two farms used in this study.


Inputs: <br>

-   EJM-CLS-22F_pct98.csv
-   EJM-CLS-22B_pct98.csv
-   Bacterial_alpha_div_data.csv
-   Fungal_alpha_div_data.csv
 

Outputs: <br>

-   figure 4  


## Fig_5_Stats_CrossRemBetaDisper

-   Description: This file contains code   


Inputs:

-   EJM-CLS-22F_pct98.csv
-   EJM-CLS-22B_pct98.csv
-   Sequencing_data_formatted_for_analysis(01.28.2026).xlsx
 

Outputs:

-   Figure 5

## Fig_6_Stats_LabVolcanoCompost.Rmd  

-   Description: Contains code corresponding to fig 6. This includes volcano plots and running an ANCOMBC for compost/no compost treatments.  

Inputs: <br>

-   EJM-CLS-22F_pct98.csv
-   EJM-CLS-22B_pct98.csv
-   Sequencing_data_formatted_for_analysis(01.28.2026).xlsx
-   Bloom_otu_table_Bac.csv
-   Bloom_otu_table_Fun.csv
-   Bloom_taxonomy_table_Bac.csv
-   Bloom_taxonomy_table_Fun.csv
-   Bloom_sample_info.csv  
 

Outputs: <br>  

-   figure 6
