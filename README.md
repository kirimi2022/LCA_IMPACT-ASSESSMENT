# Repository: CIFF-LCA project data cleaning cosultancy guidlines

This repository contains the code, data, surveytools and other supplementary materials for the cosultancy work "Cleaning CIFF LCA farm family endline survey data."

## Background of the consultancy work
The Low Carbon Agriculture (LCA) project, funded by the Childrenâ€™s Investment Fund Foundation (CIFF), is a pilot initiative aimed at demonstrating the potential of LCA practices in transforming agriculture into a carbon sink. The project has been implemented over the past three years by the Aga Khan Foundation and the Aga Khan Rural Support Program (AKRSP) across three states in India: Madhya Pradesh (MP), Uttar Pradesh (UP), and Gujarat. CIFF has engaged CIFOR-ICRAFâ€™s IAA unit to conduct an impact evaluation of the program. As part of this evaluation, we have collected endline survey data, which now needs to be cleaned and analysed and combined with baseline data to generate evidence for the final report. The consultant will support the IAA Unit in the cleaning and constructing indicators for the endline survey for an impact assessment of the CIFF LCA program in India.  The final output will be clean data; constructed indicators ensuring the data cleaning and constructed indicators are consistent with baseline data and prepare some visuals to be used in the endline report.

## Repository Structure
The repository is organized as follows:

```
|-- code
|   |-- Baseline
|   |  | --1_Cleaning_LCA.do
|   |  | --2_Var_Construct_LCA.do
|   |-- Endline
|-- data
|   |-- Baseline
|   |  | --LCA_Baseline_final.csv
|   |  | --LCA_Baseline_final.dta
|   |-- Endline
|   |  | --LCA_Endline_Final.csv
|   |  | --LCA_Endline_Final.dta
|-- README.md
|   |-- sample output
|   |  | --LCA_CIFF_ Baseline_followup survey results_revised.pptx
|   |-- Surveytool
|   |  | --LCA_Baseline_final.xls
|   |  | --LCA_FF_Survey_endline_final.xls
```

### `code`
This file contains two stata dofiles used to clean the raw data and create indicators for the baseline. These stata do file script will assist to replicate the same script in python or R to be used for simlar data cleaning for the endline survey. To run the codes, open the file in Stata and follow the instructions within the code. Ensure that the required datasets are available in the `data/Baseline` directory. You will develop similar script in python or R to be run on endline data. 

### `data`
The `data` folder contains the data sets for the baseline and endline in seprate subfolders. The datasets are provided in csv and stata dta format. The baseline data is provided to enable the consultant to replicate the dofile. 

### `sample output`, 
This folder contains a slidedeck from baseline and followup survey (middline) to show the kind of output we will produce once the data is cleaned.

### `4_Supplementary_Data.Rmd`, `4_Supplementary-Data.pdf`
The R Markdown document `4_Supplementary_Data.Rmd`  contains code to process and analyze supplementary data that accompanies the research paper. The `4_Supplementary-Data.pdf` file is the compiled version of this supplementary data analysis. 

### `Surveytool/`
This directory contains the survey tools for the baseline and endline survey that we used for the data collection with SurveyCTO data collection app. To understand the data, the consultant is expected to review these surveytools and the questions in there. The excel file contains two key tabs - survey and choices. Survey tab contains columns like `type', `name', `label::English'. The `label::English' is the questions asked in English, `name'  is the name of the variable for the respective question and `type'' is the type of variable. The choice tabe containes the options used for questions with multiple choices. For instance if the question is yes or no type, the list_name containing `yes_no'  is provided that takes values of 1 or 0 and labled as `YES' or `NO''. The information is found under the choise tab in the columns `list_name', 'name'', and `label::English'. Understanding the survey tool structure is essential to understand the data and stata dofile script. 






