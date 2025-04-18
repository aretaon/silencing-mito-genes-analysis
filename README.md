# Silencing mitochondrial gene expression in living cells					
## Proteomics analysis scripts

This repository holds the Python code for MS data analysis in the Paper "Silencing mitochondrial gene expression in living cells" (https://doi.org/10.1126/science.adr3498).


## Systems requirements
- Scripts are provided as [Jupyter notebooks](https://jupyter.org/).
- Analysis was performed using modules from [the autoprot project](https://github.com/ag-warscheid/autoprot) which need to be installed on your local computer
  - Autoprot integrates Python and R scripts for proteomics data analysis and therefore requires both languages to be installed
- Software dependencies for autoprot are detailed in the ''requirements.txt'' file in the autoprot repository
  - However, detailed information on all installed packages during execution including version numbers are provided in the respective notebooks (as ''environment.txt'' and ''R_environment.csv'' respectively)
- The scripts were tested with Python 3.9.9 and R 4.2.2. All specific software versions for Python and R are documented with the environment.txt and R_environment.txt files in the respective data analysis folders.


## Installation guide
- Install autoprot on your local computer (see installation instructions on [the autoprot repository](https://github.com/ag-warscheid/autoprot)).
  - All analyses in this repository were performed with autoprot and cannot be run without it.
- Installation time largely depends on the time required to compile the R packages.
  - With a fast internet connection, the installation on a standard desktop computer should take less than 30 minutes.
- No non-standard libraries or hardware are required to run the scripts

## How to run

- The repository contains two subfolders ND2_CYTB and ZNF703_DUSP11_SMIM26 corresponding to the knockdown and FLAG-IP described in the paper, respectively.
  - Within each folder, you must provide the MaxQuant search results for the code to run.
- You can find the data for the knockdowns at https://www.ebi.ac.uk/pride/archive/projects/PXD061846 (use the MaxQ_txt_CYTB_ND2-KDs.zip folder). The resulting directory structure should be as follows
  
```
.
├── ND2_CYTB
├── maxquant
│   └── 2h_nonfrac
│       ├── experimentalDesignTemplate.txt
│       ├── mqpar.xml
│       └── txt
```

- Data for the FLAG-IP analysis can be found at https://www.ebi.ac.uk/pride/archive/projects/PXD061877 (use the MaxQ_txt_FLAG-IPs.zip folder).

```
.
├── ZNF703_DUSP11_SMIM26
└── txt
```

- Execute the ipynb files in each directory. Note: You should import autoprot as `autoprot_dev` to run the code as is or change the import to whatever import alias you use for autoprot.

## How to get help
If something does not work as expected, please reach out to us via the GitHub issues function.