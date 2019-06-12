# Documentations for Sapkota _et. al._ 2019

## Data

#### BLUEs_pheno_all.csv - Best linear unbiased estimate (BLUE) phenotype data for all lines
|PI|Subpopulation|Cluster|Race|Origin|DTA|PH|GN|GW|GY|FLH|PL|BL|
|---|---|---|---|---|---|---|---|---|---|---|---|---|
|PI152651|Caudatum|4|0|NA|66|146.61|1286|27.32|43.95|97|14.33333333|57.95|
|PI17548|Kafir|2|0|NA|66|214.06|1167|15.62|26.66|156.8333333|22.83333333|83.41666667|
|PI24969|Durra|3|0|NA|80|182.06|1319|29.92|50.86|162|13.33333333|41.83333333|
|PI329435|Mixed|1|0|NA|80|95.5|1388|15.68|30.47|65.83333333|26|72.58333333|

## Scripts

#### VCF_to_genotype_matrix.R 
This script contains the functions *my.read.vcf* to read SNP files in vcf format, and the *parse.vcf* function to create a genotype matrix (in -1,0,1 format) that can be used in the 'rrBLUP' package.

#### Stratified_Sampling_SAP_cluster.R
R script to create a cross-validation file with individuals proportionally divided from each cluster into five equal folds.

### Cross-validation scripts
R scripts used to implement GBLUP and cross validations using *kin.blup* function in R package 'rrBLUP'.

* CV1_prediction.R      #
* CV2_AR_prediction.R   #
* CV2_WR_prediction.R   #

#### MCMCglmm_CV1_vCov.R
Fits multi-response model in MCMCglmm to calculate variance-covariance components due to conditional expectations from race.

#### Heterozygosity_Pegas.R
R script to calculate heterozygosity per site using R package 'Pegas'.

#### LD_Calculation_HillandWeir.R
Calculations for expected values of $R^2$ under drift equilibrium *Hill and Weir (1988)*. As implemented in *Remington, et al. (2001)*.

#### GenomicHeritability.R
