# mimic_cxr_edema
Pulmonary edema severity grades based on the [MIMIC-CXR](https://physionet.org/content/mimic-cxr/2.0.0/) dataset.   

# Overview 
This repo contains 3 metadata files that consist of pulmonary edema severity grades extracted from the MIMIC-CXR dataset through different means. The metadata files have subject IDs, study IDs, DICOM IDs, and the numerical grades of pulmonary edema severity. The IDs listed in this repo have the same mapping structure as in [MIMIC-CXR](https://physionet.org/content/mimic-cxr/2.0.0/). 

- **Regular expression labeling from radiology reports.**

  [regex_report_edema_severity.csv](https://github.com/RayRuizhiLiao/mimic_cxr_edema/blob/main/regex_report_edema_severity.csv). The edema severity grades were extracted from radiology reports using regular expression (regex). More details and the code of this approach can be found [here](https://github.com/RayRuizhiLiao/regex_pulmonary_edema/). Regex was able to label **6710 radiology reports**.

- **Expert labeling from radiology reports.**

  [expert_report_edema_severity.csv](https://github.com/RayRuizhiLiao/mimic_cxr_edema/blob/main/expert_report_edema_severity.csv). A board-certified radiologist and two domain experts have read **485 radiology reports** and give pulmonary edema severity grades based on the reports. More details can be found [here](https://arxiv.org/pdf/2008.09884.pdf). 
  
- **Consensus labeling from chest radiographs.**

  [consensus_image_edema_severity.csv](https://github.com/RayRuizhiLiao/mimic_cxr_edema/blob/main/consensus_image_edema_severity.csv). Three senior radiology residents and one attending radiologist have labeled **141 chest radiographs**. They assessed the images indepdnetently, discussed and voted on the ones that they disagreed on until a consensus was reached, detailed below. This label set is the *highest-quality* among the three sets, and we recommend holding it out for testing.
  
  ![https://github.com/RayRuizhiLiao/mimic_cxr_edema/blob/main/figures/consensus_image_labeling.png](https://github.com/RayRuizhiLiao/mimic_cxr_edema/blob/main/figures/consensus_image_labeling.png?raw=true)

# Pulmonary edema severity grading

Clinical management decisions for patients with acutely decompensated heart failure and many other diseases are often based on grades of pulmonary edema severity, rather than its mere absence or presence. Clinicians often monitor changes in pulmonary edema severity to assess the efficacy of therapy. Accurate monitoring of pulmonary edema is essential when competing clinical priorities complicate clinical management. The extracted pulmonary edema severity labels in this repo were numerically coded as follows: 0, none; 1, vascular congestion; 2, interstitial edema; and 3, alveolar edema. Examples of the grades are shown below. 

![https://github.com/RayRuizhiLiao/mimic_cxr_edema/blob/main/figures/pe_examples.png](https://github.com/RayRuizhiLiao/mimic_cxr_edema/blob/main/figures/pe_examples.png?raw=true)

# References

The label curation efforts have been presented in the following publications:

G. Chauhan*, R. Liao*, W. Wells, J. Andreas, X. Wang, S. Berkowitz, S. Horng, P. Szolovits, P. Golland. [Joint Modeling of Chest Radiographs and Radiology Reports for Pulmonary Edema Assessment.](https://arxiv.org/pdf/2008.09884.pdf) *International Conference on Medical Image Computing and Computer-Assisted Intervention*, 2020. (* indicates equal contributions.)

S. Horng*, R. Liao*, X. Wang, S. Dalal, P. Golland, S. Berkowitz. [Deep Learning to Quantify Pulmonary Edema in Chest Radiographs.](https://pubs.rsna.org/doi/10.1148/ryai.2021190228) *Radiology: Artificial Intelligence*. (* indicates equal contributions.)

R. Liao, J. Rubin, G. Lam, S. Berkowitz, S. Dalal, W. Wells, S. Horng, P. Golland. [Semi-supervised Learning for Quantification of Pulmonary Edema in Chest X-Ray Images.](https://arxiv.org/pdf/1902.10785.pdf) *arXiv:1902.10785*.


