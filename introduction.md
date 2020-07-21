The quest for measuring myelin with MRI – An interactive meta-analysis
=========================================================
 
<br>

This Jupyter Notebook explores an important aspect of quantitative magnetic resonance imaging (qMRI): **validation**. Focusing specifically on **myelin measures**, we show the results of our **meta-analysis comparing quantitative MRI with histology**. [The full preprint is available on bioRxiv.](https://www.biorxiv.org/content/10.1101/2020.07.13.200972v2)

**Why myelin?** Myelin is a key component of the central nervous system. The myelin sheaths insulate axons with a triple effect: allowing fast electrical conduction, protecting the axon, and providing trophic support. The conduction velocity regulation has become an important research topic, with evidence of activity-dependent myelination as an additional mechanism of plasticity. Myelin is also relevant from a clinical perspective, given that demyelination is often observed in several neurological diseases such as multiple sclerosis.

**How are qMRI measures validated?** Similarly to other qMRI biomarkers, MRI-based myelin measurements are noisy, indirect, and might be affected by other microstructural features. Assessing the accuracy of such measurements, as well as their sensitivity to change, is essential for their translation into clinical practice. That is why histological validation is necessary. The most common validation approach is based on acquiring MR data from *in vivo* or *ex vivo* tissue and then comparing those data with the related samples analysed using histological techniques.

**Why a meta-analysis?** So far, a long list of studies have looked at MRI-histology comparisons, each of them focusing on a specific pathology and a few MRI measures. Despite these numerous studies, there is still an ongoing debate on what MRI measure should be used to quantify myelin and as a consequence there is a constant methodological effort to propose new measures. We believe that this debate would benefit from a quantitative analysis of all the findings published so far, specifically addressing inter-study variations and prospects for future studies, something that is currently missing from the literature.
<br>

---
**A bit more about this Jupyter Notebook**

The main idea for this Jupyter Notebook is to let you interactively explore our dataset. For this reason, in the next pages you will find brief descriptions of what has been done, but the figures (realized with [plotly](https://plotly.com)) are the main content. You will not find sections discussing or interpreting these results: for that, please check the [preprint](https://www.biorxiv.org/content/10.1101/2020.07.13.200972v2).

---