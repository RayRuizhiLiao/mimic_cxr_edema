# mimic_cxr_edema
Pulmonary edema severity grades based on the [MIMIC-CXR](https://physionet.org/content/mimic-cxr/2.0.0/) dataset.   

# Overview 
This repo contains 3 metadata files that consist of pulmonary edema severity grades extracted from the MIMIC-CXR dataset through different means. The metadata files have subject IDs, study IDs, DICOM IDs, and the numerical grades of pulmonary edema severity. The IDs listed in this repo have the same mapping structure as in [MIMIC-CXR](https://physionet.org/content/mimic-cxr/2.0.0/). 

- **Regular expression labeling from radiology reports.**

  The edema severity grades were extracted from radiology reports using regular expression (regex). More details and the code of this approach can be found [here](https://github.com/RayRuizhiLiao/regex_pulmonary_edema/).

- **Expert labeling from radiology reports.**

  A board-certified radiologist and two domain experts have read 485 radiology reports and give pulmonary edema severity grades based on the reports.
  
- **Consensus labeling from chest radiographs.**

  Three senior radiology residents and one attending radiologist have labeled 141 chest radiographs. They assessed the images indepdnetently, discussed and voted on the ones that they disagreed on until a consensus was reached.  

# Pulmonary edema severity grading
