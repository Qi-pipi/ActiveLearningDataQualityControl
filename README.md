# Data Quality-Control

## Requirements
 environment.yaml
 
## Function of every notebook
 argo_split: split the training data 70%, test data 30%. using ShuffleSplit to ensure these two sets have the same ratio.  
 Anomaly_ratio_computing: compute low quality data ratio of every float.  
 Preprocessing_argo: Data exploration and preprocessing.  
 AL_random_high/low: uncertainty, random sampling for high/low ratio float.  
 high/low_random_committe: initial labeled data is selected by random sampling，with active learning committee by query strategy.    
 unsupervised+al+supervised_low/high: initial labeled data is selected by random sampling，4 unsupervised models computing quality score and using top-rank strategy.    
 unsupervised+al+supervised_low_top: initial labeled data is selected by quality score.    
 Visualization: visual results.  
 
## Dataset
 Dataset_2: Original data.  
 Dataset: Preprocessed data (normalization, generate label).  
 Randomtrain/Randomtest: ShuffleSplit data randomly with same ratio (70%,30%).  
 Firsttrain/Lasttrain: Find the last 30% data with the same low quality data ratio. The rest data is training data.   

## Data
 Float & ratio (%).  
 6903102: 0.291678423.  
 3901890: 29.36446072.  
 Seadatanet: 0.6948851.  
 
## resultes
### result: All experiment results
  auto/if/oc_score_low_top.csv: all training data ranked by scores.  
  auto/if/oc_score_low/high.csv: unlabled data(initial labled data selected by random sampling).  
  last_f1/kappa_Number.csv: random and uncertainty sampling result of float Number.   
  last_f1/kappa_Number_committee.csv: committee sampling result of float Number.  
  random_high/low_un_1000.csv: random initial labeled data and top-rank strategy, 1000 query.  
  random_low_un_300/1000_top.csv: initial labeled data selected by top-rank stategy.
### image
  F1/Kappa_high/low_random/last : random + Uncertainty. 
  F1/Kappa_high/low_random/last_committee: committee    
  F1_high/low_random_compare: best committee + uncertainty.  
  un_random/high_xx:query xx with random initial labeled data. Unsupervised top rank strategy.  

  
