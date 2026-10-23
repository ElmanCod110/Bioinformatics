# Bioinformatics Analysis of Apple-Waste Bioactive Compounds as Potential Inhibitors of *Fusarium* Polygalacturonases

**Molecular docking | Plant-derived bioactive compounds | Fungal enzyme targets | Reproducible research**

[![Research](https://img.shields.io/badge/Research-Bioinformatics-236B8E)](#)
[![Method](https://img.shields.io/badge/Method-Molecular%20Docking-52796F)](#methodology)
[![Status](https://img.shields.io/badge/Status-Research%20Project-6C757D)](#project-status)
[![Reproducibility](https://img.shields.io/badge/Focus-Reproducibility-7057A3)](#reproducibility)

---

## Overview

This repository contains the computational workflow, molecular docking results, analysis tables, and supporting documentation for a bioinformatics study investigating selected apple-waste-associated bioactive compounds as potential inhibitors of fungal polygalacturonases from *Fusarium*.

Polygalacturonases are enzymes involved in the degradation of pectin, a major component of plant cell walls. Their activity can contribute to plant tissue maceration and fungal pathogenicity. Identifying natural compounds that may interact with these enzymes could help generate hypotheses for future antifungal research.

The study uses molecular docking to compare the predicted binding scores of four selected compounds against four polygalacturonase targets. The results provide a computational basis for prioritizing candidates for further investigation.

**Important:** Docking scores are computational predictions. They do not, by themselves, demonstrate enzyme inhibition, antifungal activity, safety, or effectiveness in plants.

## Research Objectives

The primary objectives of this project are to:

- Investigate the predicted interactions of selected bioactive compounds with *Fusarium* polygalacturonase targets.
- Compare docking scores across compounds and target enzymes.
- Identify promising candidates for subsequent experimental validation.
- Document the computational methods and parameters used in the analysis.
- Provide a transparent record of the results and their limitations.

## Compounds Investigated

Four compounds were included in the docking analysis:

| Compound | Research relevance |
|---|---|
| Phlorizin (phloridzin) | A dihydrochalcone associated with apples |
| Quercetin | A flavonoid found in various plant materials |
| Chlorogenic acid | A phenolic acid found in apples and other plants |
| Procyanidin B2 | A flavan-3-ol dimer found in various plant materials |

The presence, abundance, and recoverability of these compounds in a particular apple-waste extract depend on the raw material and extraction procedure. Their inclusion in this computational study does not establish their concentration in the experimental extract.

## Target Enzymes

The docking analysis includes four fungal polygalacturonase targets:

| Target | Identifier used in the docking records | Grid dimensions (Å) |
|---|---|---|
| PG1 | O00094 | 20 × 18 × 22 |
| PG5 | Target-specific identifier to be documented | 24 × 24 × 24 |
| PGX4 | C7B5W4 | 24 × 24 × 24 |
| PGX6 | Target-specific identifier to be documented | 20 × 20 × 18 |

Identifiers and protein sequences should be cross-checked against the original sequence records and structure files before publication. The identifier column above reflects the available docking records and should not be interpreted as a complete accession audit.

## Key Docking Results

The following table summarizes the recorded docking scores in kcal/mol. More negative scores indicate more favorable predicted binding according to the scoring function used; they are not direct measurements of binding affinity.

| Compound | PG1 | PG5 | PGX4 | PGX6 |
|---|---:|---:|---:|---:|
| Phlorizin | −7.3 | −8.412 | **−8.611** | **−9.248** |
| Quercetin | −7.5 | −7.752 | −8.158 | −8.458 |
| Chlorogenic acid | **−7.7** | −8.059 | −8.285 | −8.456 |
| Procyanidin B2 | −7.6 | −8.252 | −7.769 | −7.665 |

### Preliminary interpretation

- **PG1:** Chlorogenic acid has the most negative recorded docking score (−7.7 kcal/mol).
- **PG5:** Phlorizin has the most negative recorded docking score (−8.412 kcal/mol).
- **PGX4:** Phlorizin has the most negative recorded docking score (−8.611 kcal/mol).
- **PGX6:** Phlorizin has the most negative recorded docking score (−9.248 kcal/mol).

Across these four targets, phlorizin has the most negative recorded score for three targets, while chlorogenic acid has the most negative score for PG1.

These rankings are limited to the compounds and docking configurations evaluated here. Scores obtained using different target structures or grid configurations should be interpreted cautiously and should not be treated as equivalent to experimentally measured inhibition.

## Methodology

The computational workflow involves the following general stages:

1. **Target selection:** Select fungal polygalacturonase targets for computational investigation.
2. **Structure preparation:** Prepare the relevant protein structures for molecular docking.
3. **Ligand preparation:** Prepare the selected compounds in compatible formats.
4. **Docking configuration:** Define the search box and docking parameters for each target.
5. **Molecular docking:** Run AutoDock Vina and record the resulting scores.
6. **Result extraction:** Organize the scores by compound and target.
7. **Comparative analysis:** Calculate descriptive statistics and compare candidate rankings.
8. **Interpretation:** Identify computational candidates for future experimental validation.

### Docking parameters

The available run records document the following settings:

| Parameter | Recorded setting |
|---|---|
| Exhaustiveness | 16 |
| Energy range | 4 kcal/mol |
| Number of modes | 10 for PG1, PG5, and PGX4; 20 for PGX6 |
| Grid dimensions | Target-specific; listed above |
| Software | AutoDock Vina; version 1.2.7 is documented for PG5, PGX4, and PGX6 |

The exact grid center coordinates, preparation procedures, software versions for every run, and any additional settings should be recorded in the corresponding methods documentation before the workflow is considered fully reproducible.

## Statistical Analysis

Descriptive statistics can summarize the distribution of docking scores for each target. However, the four compounds are distinct candidates, not independent experimental replicates.

Consequently, descriptive comparisons alone do not establish statistical significance. Inferential tests such as ANOVA and Tukey HSD should only be reported when their assumptions, inputs, and interpretation are scientifically justified.

Docking scores should be interpreted as computational ranking evidence rather than experimental measurements of enzyme inhibition.

## Repository Structure

The repository is intended to organize the research materials in a clear and reproducible format:

```text
apple-waste-fusarium-docking/
├── README.md
├── CITATION.cff
├── LICENSE
├── methods/
│   ├── docking-parameters.md
│   └── analysis-methods.md
├── scripts/
│   └── analyze_docking.py
├── data/
│   └── README.md
├── results/
│   ├── docking-scores.csv
│   └── summary-tables.csv
└── environment/
    └── software-versions.txt
```

This is a proposed structure. Files should only be described as available after they have actually been added to the repository.

## Reproducibility

Reproducibility is a central objective of this project.

Where redistribution is permitted, the repository should provide or reference:

- Protein target identifiers and source records.
- Protein and ligand preparation procedures.
- Docking configuration files and grid center coordinates.
- The exact software versions used for each computational run.
- Raw docking output files or stable links to archived copies.
- Scripts used to extract, validate, and summarize docking scores.
- Machine-readable result tables.
- A record of any manual corrections or exclusions applied during analysis.

Derived tables should be traceable to their source outputs. Reported scores should not be manually changed without documenting the reason and preserving the original result.

## Limitations

This project is computational and hypothesis-generating. Its conclusions are subject to several limitations:

- Docking scores are approximations and may not accurately predict experimental binding affinity.
- Protein structure quality and preparation can influence the results.
- Different grid configurations can affect the comparability of scores.
- Docking does not establish whether a compound inhibits enzyme activity.
- The analysis does not, by itself, establish antifungal efficacy, plant protection, toxicity, or practical application.
- The results do not establish the concentration of the selected compounds in apple-waste extracts.
- Experimental validation is required before drawing conclusions about biological activity.

These limitations should accompany the results whenever they are cited or presented.

## Future Work

Potential next steps include:

- Verifying target accessions, sequences, and structure provenance.
- Archiving complete docking configurations and original output logs.
- Examining predicted binding poses and relevant protein–ligand interactions.
- Validating candidate compounds using appropriate enzyme inhibition assays.
- Comparing computational predictions with experimental observations.
- Evaluating the chemical composition of apple-waste extracts independently.
- Updating the repository as methods and results are validated.

## Citation

If you use this repository, please cite the associated research manuscript when it becomes available.

**Manuscript:** [Insert the final article title]  
**Authors:** [Insert author list]  
**Journal or preprint:** [Insert publication details]  
**DOI:** [Insert DOI when available]

For long-term research citation, consider archiving a fixed release with Zenodo and adding its DOI here.

## Data and Code Availability

The repository is intended to support transparent access to the computational methods and results associated with this study.

Availability of individual raw data files depends on their inclusion in the repository and any applicable redistribution restrictions. Please consult the repository contents and the associated manuscript for the precise scope of the released materials.

## Acknowledgments

[Add the names of supervisors, research groups, institutions, or funding sources that should be acknowledged.]

## License

[Choose and add an appropriate license after confirming the rights associated with the code, data, structures, and other materials.]

---

**Research principle:** Computational predictions are most useful when their methods, assumptions, data, and limitations are openly documented and their conclusions remain proportional to the evidence.
