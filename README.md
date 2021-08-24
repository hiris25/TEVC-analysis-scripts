# TEVC-analysis-scripts
Python scripts for analysis of TEVC data from Robocyte and manual set ups

----- TEVC_DR --------

Datasource: .dat files from Robo2+ with all features extracted and baseline subtracted.
Data structure: all .dat files for a single construct should be in their own folder and each constrcut run through the script seprately

Overview:
- Takes all .dat files with a specified extension from a folder and combines them into a single dataframe
- converts units and calculates I/Imax for each oocyte
- calculates mean, sd, n and exports into new csv

----- DR_antagonsits ------

Datasource: .dat files from Robo2+ with all features extracted and baseline subtracted.
Data structure: all .dat files for a single construct should be in their own folder and each constrcut run through the script seprately. However multiple antagonists for the same construct can be in one folder

Overview:
As above but groups data by antagonist compound
