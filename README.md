#Data Quality-Control
## Requirements
environment.yaml
## Function of every notebook
Anomaly_ratio_computing: compute low quality data ratio of every float
AL_random_high/low: uncertainty, random sampling for high/low ratio float
high/low_random_committe: initial labeled data is selected by random sampling，with active learning committee by query strategy.
unsupervised+al+supervised_low/high: initial labeled data is selected by random sampling，4 unsupervised models computing quality score and using top-rank strategy 
unsupervised+al+supervised_low_top: initial labeled data is selected by quality score

## Datasets
Float & ratio (%)
6903102:0.291678423
3901890:29.36446072