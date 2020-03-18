+++

title= "Unintended Bias Metrics"
date= "2018-06-28T00:00:00Z"
weight = 20  # Order that this section will appear.

+++


Unintended bias can be uncovered by looking at differences in the score distributions between data mentioning a specific identity-term $s$ (**subgroup** $s$ distribution) and the rest (**background** distribution). Following [[1](#ref1), [2](#ref2)], the three per-term AUC-based bias scores are related to specific subgroups as follows:

- AUC<sub>Subgroup</sub>($s$): calculates AUC only on the data within the subgroup $s$. This represents model understanding and separability within the subgroup itself. *A low value in this metric means the model does a poor job of distinguishing between misogynous and non-misogynous comments that mention the identity*.

- AUC<sub>BPSN</sub>($s$): Background Positive Subgroup Negative (BPSN) calculates AUC on the misogynous examples from the background and the non-misogynous examples from the subgroup. *A low value in this metric means that the model confuses non-misogynous examples that mention the identity-term with misogynous examples that do not, likely meaning that the model predicts higher misogynous scores than it should for non-misogynous examples mentioning the identity-term*.

- AUC<sub>BNSP</sub>($s$): Background Negative Subgroup Positive (BNSP) calculates AUC on the non-misogynous examples from the background and the misogynous examples from the subgroup. *A low value here means that the model confuses misogynous examples that mention the identity with non-misogynous examples that do not, likely meaning that the model predicts lower misogynous scores than it should for misogynous examples mentioning the identity*.
