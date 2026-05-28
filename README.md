# microbiome_compost_aphid

Code and data in this repository correspond to "Aphid populations vary in a soil microbiome-dependent and compost application-independent manner" by Dixon et a. 2026. Briefly, while compost changes soil microbial communities, its application does not alter aphid populations. The soil microbiome, however, does affect aphid population dynamics.

Dixon, MM; McAnally EJ; Bloom EH, Casteel CL

Sequencing data is stored in the NCBI database (PRJNA1468248).

## Project description

Compost use is an important cultural practice, particularly for organic agricultural systems. Microbiomes from organically managed agriculture tend to be associated with diminished pest pressure and altered microbial communities. Here, we evaluated how compost application regulates soil microbial communities in response to aphid pressure in field and laboratory conditions. Soils were collected from across New York state, and in the field, compost application did not shift Shannon diversity or community composition. However, farm location was a possible driver of change in the microbiome. To investigate mechanisms of change driven by farm site, a laboratory trial was carried out in which sterile potting media was amended with microbiome slurries from four farms. Kale was grown in these pots, and aphids were applied. In the laboratory trial, the source of the microbiome inoculum altered the subsequent composition of microbial communities. Further, compost markedly increased Shannon diversity and decreased beta dispersion for bacteria and fungi, but it did not affect aphid populations. Although aphids were unaffected by compost, they were affected by the inoculum source, thus indicating that microbiome composition influences aphid population. These results reveal a complexity in the ecology of plant-microbe interactions in which present soil microbial communities shape plant-insect interactions.

# Descriptions of code files

-   **"Bloom_SiteLocations.csv"**: Contains lat/long data for the farm locations used in this study. From Bloom et al. 2024. Used in fig 1.
-   **"Formatted data on samples used in analysis.xlsx"**: Excel file of farmer data. From Bloom et al. 2024. Contains alpha diversity measures used in figure 1.
-   **"Bloom_sample_info.csv"**: Contains sample information for participants that had composted/uncomposted fields and contains alpha diversity measures. Used in figure 1, figure 6.
-   **"Bloom_taxonomy_table_Bac.csv"**: Tax table for bacteria in field trial. From Bloom et al. 2024. Used in figure 1, figure 6.
-   **"Bloom_taxonomy_table_Fun.csv"**: Tax table for fungi in field trial. From Bloom et al. 2024. Used in figure 1, figure 6.
-   **"Bloom_otu_table_Bac.csv"**: OTU table for bacteria in field trial. From Bloom et al. 2024. Used in figure 1, figure 6.
-   **"Bloom_otu_table_Fun.csv"**: OTU table for fungi in field trial. From Bloom et al. 2024. Used in figure 1, figure 6.
-   **"seed_farm_locations.csv"**: Contains lat/long data for the farm locations used in the lab trial. Used in figure 2.
-   **"EJM-CLS-22B_pct98.csv"**: Contains OTU and TAX information for the bacteria sequenced in the laboratory trial. Used in figure 2, figure 3, figure 4, figure 5, figure 6.
-   **"EJM-CLS-22F_pct98.csv"**: Contains OTU and TAX information for the Fungi sequenced in the laboratory trial. Used in figure 2, figure 3, figure 4, figure 5, figure 6.
-   **"Sequencing_data_formatted_for_analysis(01.28.2026).xlsx"**: Contains sample info for the sequencing data from the laboratory trial. Used in figure 2, figure 3, figure 4, figure 5, figure 6.
-   **"sample_data_field_corrected_samples_mmd.csv"**: Contains samples information for the ordination of sequencing data from the laboratory trial. Used in figure 2, figure 3
-   **"HATCH_compost_bioassay_data.xlsx"**: Contains aphid population data for the lab trial. Used in figure 2.
-   **"Bacterial_alpha_div_data.csv"**: Contains alpha diversity data for the lab trial. Used in figure 4.
-   **"Fungal_alpha_div_data.csv"**: Contains alpha diversity data for the lab trial. Used in figure 4.


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
-   Results corresponding to figure 6
