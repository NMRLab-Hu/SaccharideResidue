
<!-- README.md is generated from README.Rmd. Please edit that file -->

# SaccharideResidue

## Description
<img width="4909" height="3368" alt="Abstract Graphic" src="https://github.com/user-attachments/assets/20240632-4d1d-4290-bca8-d70551ae7d80" />


SaccharideResidue

</p>

</div>

The structural elucidation of polysaccharides by NMR spectroscopy often relies on matching experimental chemical shifts against reference databases. However, existing tools are primarily designed for forward validation of predefined structural hypotheses, and their performance can be compromised by experimental variability (e.g., reference standards, temperature, solvent) and incomplete spin-system assignments. To address these challenges, we developed an enhanced sugar residue matching and screening algorithm supported by a comprehensive chemical shift database. The database was constructed by curating 3410 fully assigned 13C/1H NMR entries from 426 papers on polysaccharide structural analysis (2010–2025), covering 14 monosaccharide types (excluding fructose) and 185 glycosyl types from plants, fungi, and algae. 

The algorithm integrates a systematic reference alignment step to correct global chemical shift deviations, supports matching using either partial or complete 13C/1H chemical shift sets, and incorporates a permutational assignment strategy to resolve ambiguities in unassigned positions. A normalized root-mean-square error (RMSE) is calculated to evaluate goodness-of-fit, enabling robust identification of the most probable monosaccharide residue type. This method significantly improves the reliability of sugar residue identification from experimental NMR data, particularly under conditions of variable experimental setups or incomplete assignment.


## Functions

**See the R help page for more details\!\!\!**

1.  “file_path”: Path to the data file. The file must be an XLSX containing two sheets: sheet1 and sheet2. Sheet1 contains dataset entry data, and sheet2 contains experiment data. For data formats in sheet1 and sheet2, see the Demo file on GitHub.

2.  “output_path”: Path to the result file. The file must be an XLSX containing serlve sheets: sheet1 contains RMSE table of all sugar residues, and other sheets only contain theirselves RMSE table of each sugar residues.

## Workflow for matching experimental NMR chemical shifts against the enhanced sugar residue database

**For Demonstration Purposes Only\!\!\!**

**If you want to run the following code, you need to modify the file
path and some parameters according to your needs\!\!\!**

*install package*

``` r
devtools::install_local ("~/SaccharideResidue_1.0.0.tar.gz”)
```

*step1*

``` r
library (SaccharideResidue)
SaccharideResidue (
  file_path = "D:/LCH/LCH_github/SaccharideResidue_R/P-WAXYL.xlsx",
  output_file = "D:/LCH/LCH_github/SaccharideResidue_R/P-WAXYL_result.xlsx"
)
```

## References



## Contact

If you need the database or have any questions, please do not hesitate to contact us at rainbow@stu.cdutcm.edu.cn or kaifenghu@cdutcm.edu.cn
