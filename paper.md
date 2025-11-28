---
title: 'An interactive meta-analysis of MRI biomarkers of myelin'
tags:
  - Quantitative MRI
  - Myelin imaging
  - Meta analysis
authors:
  - name: Matteo Mancini
    orcid: 0000-0001-7194-4568
    affiliation: "1, 2, 3"
  - name: Agah Karakuzu
    orcid: 0000-0001-7283-271X
    affiliation: "2, 8"
  - name: Julien Cohen-Adad
    orcid: 0000-0003-3662-9532
    affiliation: "2, 4"
  - name: Mara Cercignani
    orcid: 0000-0002-4550-2456
    affiliation: "1, 5"
  - name: Thomas E. Nichols
    orcid: 0000-0002-4516-5103
    affiliation: "6, 7"
  - name: Nikola Stikov
    orcid: 0000-0002-8480-5230
    affiliation: "2, 8"
affiliations:
  - name: Department of Neuroscience, Brighton and Sussex Medical School, University of Sussex, United Kingdom;
    index: 1
  - name: NeuroPoly Lab, Institute of Biomedical Engineering, Polytechnique Montreal, Montreal, Canada
    index: 2
  - name: CUBRIC, Cardiff University, United Kingdom
    index: 3
  - name: Functional Neuroimaging Unit, CRIUGM, Université de Montréal, Canada
    index: 4
  - name: Neuroimaging Laboratory, Fondazione Santa Lucia, Italy
    index: 5
  - name: Wellcome Centre for Integrative Neuroimaging (WIN FMRIB), University of Oxford, United Kingdom
    index: 6
  - name: Big Data Institute, University of Oxford, United Kingdom
    index: 7
  - name: Montreal Heart Institute, University of Montréal, Montréal, Canada
    index: 8
date: 05 October 2021
bibliography: paper.bib
---

+++ { "part": "abstract" }
In this work, we explore important aspect of quantitative magnetic resonance imaging (qMRI): validation [@jcohen:2018]. Focusing specifically on myelin measures, we show the results of our meta-analysis comparing quantitative MRI with histology.
+++

# Introduction

**Why myelin?:** Myelin is a key component of the central nervous system. The myelin sheaths insulate axons with a triple effect: allowing fast electrical conduction, protecting the axon, and providing trophic support. The conduction velocity regulation has become an important research topic, with evidence of activity-dependent myelination as an additional mechanism of plasticity. Myelin is also relevant from a clinical perspective, given that demyelination is often observed in several neurological diseases such as multiple sclerosis.

**How qMRI measures validated?:** Similarly to other qMRI biomarkers, MRI-based myelin measurements are noisy, indirect, and might be affected by other microstructural features. Assessing the accuracy of such measurements, as well as their sensitivity to change, is essential for their translation into clinical practice. That is why histological validation is necessary. The most common validation approach is based on acquiring MR data from in vivo or ex vivo tissue and then comparing those data with the related samples analysed using histological techniques.

**Why meta analysis?:** So far, a long list of studies have looked at MRI-histology comparisons, each of them focusing on a specific pathology and a few MRI measures. Despite these numerous studies, there is still an ongoing debate on what MRI measure should be used to quantify myelin and as a consequence there is a constant methodological effort to propose new measures. We believe that this debate would benefit from a quantitative analysis of all the findings published so far, specifically addressing inter-study variations and prospects for future studies, something that is currently missing from the literature.

# Literature overview

First, how were the studies selected? We used the [Medline database](https://pubmed.ncbi.nlm.nih.gov) and retrieved all the records mentioning (1) myelin, (2) MRI and (3) histology (or a related technique). The full list of keywords is provided in the preprint.


:::{tip} Figure 1
:class: tip
The Sankey diagram shows the screening procdess. You can hover with the mouse on each block and connection to see details about the number of studies and exclusion criteria.
:::

:::{figure} #fig1cell
:label: fig1 

Sankey diagram representing the screening procedure.
:::

We identified 58 studies reporting quantitative comparisons between MRI and histology: these included a variety of methodological choices and experimental conditions, in terms of tissue type (brain, spinal cord, peripheral nerve), condition (*in vivo*, *ex vivo*, *in situ*), species (human, animal), pathology model, and many more. A glimpse of these subdivisions is provided in the following treemap.

:::{tip} Figure 2

You can click on each box to expand the related category, and for each study you can find out more details and the link to the original paper.
:::

:::{figure} #fig2cell
:label: fig2 

Treemap of the selected studies classified according to their sample types and anatomical origins.
:::

Given the number of different variables influencing the results, we decided to focus only on brain studies. As we needed to take into account the sample size for quantitative comparisons, we also further selected only the studies that reported both the number of subjects and the number of ROIs (regions of interest) considered for correlation purposes. This further screening led us to 43 studies. For these studies we wanted to quantitatively evaluate the reported effect size taking into account the respective samples sizes: we chose the coefficient of determination R{sup}`2`, as it was the most common quantitative result we could obtain from these studies.

:::{tip} Figure 3

To have a look at both sample size and effect size for each measure, we prepared an interactive bubble chart, where the size of each bubble is proportional to the sample size. You can hover on the bubbles to obtain additional details.
:::

:::{figure} #fig3cell
:label: fig3

Bubble chart of R{sup}`2` values between a given MRI measure and histology for each study across MRI measures, with the area proportional to the number of samples.
:::

To provide a different way to explore sample size and effect size, we also prepared another treemap, where the studies are organised by measures. For each study, the area of its box is proportional to the sample size, while the color represents the related coefficient of determination.


```{admonition} Figure 4
:class: tip
You can click on each box to expand the related category, and for each study you can find out more details.
```

:::{figure} #fig4cell
:label: fig4

Treemap chart of the studies considered for the meta-analysis, organized by MRI measure. The color of each box represents the reported R{sup}`2` value while the size box is proportional to the sample size.
:::


## Quantitative comparisons

Can we express quantitatively what we observed in the previous plots? This is where the meta-analysis tools come in: we used the R package [metafor](http://www.metafor-project.org/doku.php) to fit a mixed-effect (ME) model to the data reported for each measure. In this way, we can estimate an overall interval of R{sup}`2` values based on the effect sizes and the sample sizes. We can also estimate the interval of R{sup}`2` that we can expect in future studies (this is called prediction interval). 

```{admonition} Figure 5
:class: tip
A compact way to represent these results is given by forest plots: for each study, we represent the effect size and the related sample size using a square and a horizontal error bar; then for each measure, we represent the results from the ME model using a diamond and an additional error bar; finally to represent the prediction interval we use two hourglasses and a dotted line.
```




# Acknowledgements

MM was funded by the Wellcome Trust through a Sir Henry Wellcome Postdoctoral Fellowship [213722/Z/18/Z]. TEN was supported by NIH grant R01MH096906.

# References