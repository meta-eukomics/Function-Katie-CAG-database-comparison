# Function-Katie-CAG-database-comparison

This R code creates a dataframe of the number of proteins annotated in the RNA intercalibration CAG and MAD consolidated assemblies for main functional databases. For each sample, it includes total number of proteins from Transdecoder .pep files, total proteins annotated by Eggnog-mapper, total number of unannotated proteins, and the number of proteins annotated within Eggnog for Pfam, KEGG, and GO. Pairwise and three-way intersections between the databases are also included. 

Two figures were created using these data:
R_plots/CAG_MAD_protein_counts_absolute_barplot.pdf is a stacked barplot of the absolute number of predicted proteins annotated by PFAM only, KEGG only, GO only, PFAM and KEGG, KEGG and GO, PFAM and GO, all three databases, and unannotated.

R_plots/CAG_MAD_protein_counts_relative_barplot_v2.pdf is a relative abundance barplot of each database category divided by the total number of Eggnog annotated reads for each assembly. 

Dataframe headings

"Sample" = sample IDs for CAGs and MAD <br />
"Total_contigs" = number of proteins annotated by Eggnog <br />
"PFAMs" = number of proteins annotated in Eggnog by PFAM <br />
"KEGG_ko" = number of proteins annotated in Eggnog by KEGG <br />
"GOs" = number of proteins annotated in Eggnog by GO <br />
"PFAMs_KEGG_ko" = number of proteins annotated in Eggnog by PFAM and KEGG <br />
"PFAMs_GOs" = number of proteins annotated in Eggnog by PFAM and GO <br />
"KEGG_ko_GOs" = number of proteins annotated in Eggnog by KEGG and GO <br />
"PFAMS_KEGG_ko_GOs" = number of proteins annotated in Eggnog by all three databases <br />
"PFAM_only" = number of proteins annotated in Eggnog by only PFAM; no KEGG or GO annotation <br />
"KEGG_only" = number of proteins annotated in Eggnog by only KEGG; no PFAM or GO annotation <br />
"GO_only"  = number of proteins annotated in Eggnog by only GO; no KEGG or PFAM annotation <br />
"PFAM_KEGG_only" = number of proteins annotated in Eggnog by only PFAM and KEGG; no GO annotation <br />
"PFAM_GOs_only" = number of proteins annotated in Eggnog by only PFAM and GO; no KEGG annotation <br />
"KEGG_GOs_only" = number of proteins annotated in Eggnog by only GO and KEGG; no PFAM annotation <br />
"total_pep_counts" = number of predicted proteins from Transdecoder .pep file <br />
"not_Pfam_KEGG_GO" = number of proteins with no annotation from PFAM, KEGG, or GO <br />
"unannotated" = number of proteins unannotated by anything in Eggnog <br />
"PFAMS_KEGG_ko_GOs_percent" = PFAMS_KEGG_ko_GOs divided by Total_contigs *100 <br />
"PFAM_only_percent" = PFAM_only divided by Total_contigs *100 <br />
"KEGG_only_percent" = KEGG_only divided by Total_contigs *100 <br />
"GO_only_percent" = GO_only divided by Total_contigs *100 <br />
"PFAM_KEGG_only_percent" = PFAM_KEGG_only divided by Total_contigs *100 <br />
"PFAM_GOs_only_percent" = PFAM_GOs_only divided by Total_contigs *100 <br />
"KEGG_GOs_only_percent" = KEGG_GOs_only divided by Total_contigs *100 <br />
"not_Pfam_KEGG_GO_percent" = not_Pfam_KEGG_GO divided by Total_contigs *100 <br />
