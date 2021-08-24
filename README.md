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

----- TEVC_ManualRampAnalysis ------

Datasource: Manual or Robo current, time, voltage data in .xlxs format

Data Structure: one file per ramp/voltage step protocol, requires +/- agonist for each buffer. All files for one construct will be in one folder. Run script again for new construct.

Must have the following headers:

- Time - ms
- Current - nA
- Voltage - mV
- Oocyte - oocyte ID
- Buffer - ND96 / Gluconate / NMDG
- Comp. 1 - agonist
- conc. 1 - concentration (number only)
- unit 1 - concentration unit
- Start Date - date
- IV Prot. - name of protocol
- Inj. ID 1 - construct info

Overview:
- Takes all .xlxs files with a specified extension from a folder and combines them into a single dataframe
- converts units and calculates I/Imax for each oocyte
- removes time before and after stimulus - you need to change this to fit your protocol
- leak subtraction
- plots leak subtracted cuvres for eahc oocyte in each solution (visual check)
- line fit and calculate Erev for each solution
- calculate delta Erev
- calculates mean, sd, n and exports into new csv
