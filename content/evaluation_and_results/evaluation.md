+++

title= "Evaluation Metrics"
date= "2018-06-28T00:00:00Z"
weight = 10  # Order that this section will appear.

+++

Each participating team will initially have access only to the training data (both raw and synthetic data). Later, we will release the unlabelled test data (both raw and synthetic data).  After the assessment, the labels for the test data will be released.  


The evaluation will be performed according to the following metric:

- **SubTask A**: The ranking will be computed by averaging the $F_1$ measures estimated for the Misogynous and Aggressiveness classes.

<center>$ score_A = \frac{F_1(\text{Misogynous}) + F_1(\text{Aggressiveness})}{2} $ </center>

- **SubTask B**: The ranking will be computed by the weighted combination of AUC computed on the test raw dataset AUC<sub>raw</sub> and three per-term AUC-based bias scores computed on the synthetic dataset  (AUC<sub>Subgroup</sub>, AUC<sub>BPSN</sub>, AUC<sub>BNSP</sub>).
Let $s$ be an identity-term and $N$ be the number of identity-terms, the evaluation will be performed according to the following metric:
<center>$ score_B = \frac{1}{2} \text{AUC}_{\text{raw}} + \frac{1}{2} \frac{\sum_s\text{AUC}_{\text{Subgroup}}(s) +  \sum_s\text{AUC}_{\text{BPSN}}(s) + \sum_s\text{AUC}_{\text{BNSP}}(s) }{N} $</center> 

