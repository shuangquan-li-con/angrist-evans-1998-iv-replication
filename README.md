(I haved processed the data, however, the data files are so huge that they cannot be uploaded in github. One of them is 348MB,and the other is 366MB. But I successfully switch them to csv. version)


**Angrist & Evans (1998) – IV Replication Project Project Overview**

## Repository Structure

- `01_Data_Cleaning.ipynb`  
  Data import, cleaning, variable preparation, and sample construction.

- `02_Replication.ipynb`  
  Baseline replication of the original identification strategy and main empirical results.

- `03_Extension_and_Results.ipynb`  
  Phase 3 extension, including robustness checks, instrument-strength diagnostics, visualizations, and final conclusions.

- `cleaned_combined_data.xlsx`  
  Cleaned dataset used for the replication and extension analysis.

- `README.md`  
  Project summary and repository guide.

This project replicates the core empirical strategy of Angrist & Evans (1998), a seminal paper in applied econometrics that uses an instrumental variables (IV) framework to estimate the causal effect of family size on parental labor supply.

The study exploits exogenous variation in fertility driven by the sex composition of the first two children. Parents with two children of the same sex are more likely to have a third child. This quasi-random variation provides a credible instrument for family size, allowing for consistent estimation of the causal impact of additional children on parents’ labor force participation and labor supply.

This replication project emphasizes:

（1）Clean identification logic

（2）Manual implementation of Two-Stage Least Squares (2SLS)

（3）Transparent and reproducible data workflow

（4）Industry-style data architecture and version control

**Causal Question**

Does having an additional child reduce parents’ labor supply?

**Identification Strategy**

（1）Endogenous variable: Family size (number of children)

（2）Instrument: Indicator for same-sex composition of the first two children
# Midterm Project: The Replication Study

## Project Overview

This repository contains my full midterm replication project for the course. The project is organized in three phases:

- **Phase 1: Project Initiation and Data Architecture**
- **Phase 2: Core Replication**
- **Phase 3: Extension and AI Integration**

The overall goal of the project is to replicate a classic empirical paper and then extend the analysis using modern robustness checks and transparent human-in-the-loop use of generative AI.

---

## Research Topic

This replication studies the relationship between fertility and maternal labor supply using an instrumental-variables strategy. The core identification strategy uses the **same-sex composition of the first two children** as an instrument for having more than two children.

The main empirical question is whether additional fertility causally reduces maternal labor supply, rather than simply being correlated with it.

---



---

## Phase 3 Extension

In the final phase of the project, I evaluated the robustness of the IV design by testing instrument strength and comparing estimates across alternative specifications. Using the same-sex composition of the first two children as an instrument for having more than two children, I estimated first-stage, reduced-form, OLS, and 2SLS models with and without controls, after excluding second-birth multiple births, and for alternative labor-supply outcomes including employment, weeks worked, and hours worked.

The results show that the instrument remains very strong across all specifications, with first-stage F-statistics far above the conventional weak-instrument threshold. At the same time, the IV estimates are substantially smaller and less precise than the corresponding OLS estimates. This suggests that the raw OLS relationship likely overstates the causal effect of fertility on maternal labor supply.

---

## Main Findings

1. The same-sex instrument is highly relevant in the first stage across all robustness specifications.
2. Weak-instrument concerns are minimal in this sample.
3. OLS estimates suggest a strong negative relationship between larger family size and maternal labor supply.
4. IV estimates are much smaller and less precise, implying that the causal effect is more modest than the raw correlation suggests.

---

## GenAI Transparency

In Phase 3, I used generative AI as a coding assistant and debugging partner. Specifically, I used it to:

- refactor Python code for IV estimation
- generate plotting code for coefficient and robustness visualizations
- troubleshoot pandas and statsmodels issues
- improve the structure of markdown explanations and summaries

All econometric decisions, variable definitions, output validation, and final interpretations were reviewed and verified by me.

---

## Tools Used

- Python
- pandas
- numpy
- statsmodels
- matplotlib
- Google Colab
- GitHub

---

## Final Note

This repository reflects both the replication of the original empirical strategy and an extension designed to test its robustness. The project demonstrates how causal inference can be strengthened by combining careful econometric reasoning with transparent and responsible use of generative AI.

（3）Estimation method: Two-Stage Least Squares (2SLS)

The instrument relies on the assumption that child gender is randomly assigned and affects labor supply only through its impact on fertility decisions.

**Data Source**

Replication data obtained from publicly available academic archives associated with the authors and/or journal publication.
