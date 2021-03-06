
<!-- README.md is generated from README.Rmd. Please edit that file -->
Clinical Depression: Prevalence, SocioDemographic, Chronic Disease Comorbidity, and Costs
=========================================================================================

Author John James (<jjames@datasciencesalon.org>)

Abstract
--------

Depression, studies have shown, costs society $210 billion per year in direct and indirect medical expenditures and lost productivity. In fact, research has indicated that the productive years lost to disability from depression are three times greater than from those to diabetes, eight times greater than those from heart disease, and 40 times those to cancer. Furthermore, patients suffering from chronic illness with co-occurring depression may incur upwards of 50% to 100% greater use in of health care services and costs. This analysis explores the sociodemographics of depression, its co-occurrence with chronic illness, and the marginal, conditional and joint effects of depression and chronic disease on productivity and the use of health care services.

Considering the sociodemographics, depression occurred with greater prevalence among those at the lower income strata; however, the highest rates of depression, controlling for education, were among college graduates across all income levels. With regard to comorbidity, 73% of those with chronic dysfunction also reported a prior diagnosis of depression. The effect on productivity was significant; indeed, those with depression with chronic illness had 44.6 greater loss in productivity than those with one or more non-mental chronic disorders. Lastly, those suffering from comorbid depression and chronic illness had 92.4% higher use of health care services than those reporting one or several chronic diseases, second only to Kidney disease in the number of office visits during the 12 month period preceding the survey.

Though these findings were significant, further time-based studies which evaluate multiple interventions would be required to illuminate the direction, strength, and nature of any cause-effect relationships among sociodemographic, productivity, and cost factors. Notwithstanding, this analysis has shown depression to be the most debilitating of the chronic disorders, with significant productivity effects and personal and societal costs.

Data
----

The Center for Disease Control and Prevention's (CDC) 2013 Behavioral Risk Factor Surveillance System (BRFSS) telephone survey provided the data for this analysis. This state-based, cross-sectional study compiled health, chronic disease, quality of life, behavioral risk factor and use of health service information from nearly 500,000 Americans. The data was statistically investigated to address four fundamental questions: (1) is there a relationship between socioeconomic status and depression, (2) to what degree does depression co-occur with other chronic conditions such as heart disease, diabetes, asthma, kidney disease, asthma and other lung diseases, (3) what are the marginal, conditional, and joint effects of depression on productivity vis-a-vis those of other chronic illnesses and (4) how does depression affect costs in terms of health service utilization, compared to other chronic disorders.

From this raw data, dichotomous independent variables which indicated whether the respondent had ever been diagnosed with either of ten leading chronic illnesses, including, heart disease, skin cancer, diabetes, asthma, lung disease, and arthritis to name a few, were extracted. Income category and highest education level achieved comprised the sociodemographic proxies for "class". The response variables of interest were the number of days of health related restricted activity (lost productivity) during the 30 days preceding the survey and the number of doctor visits (healthcare costs) during prior 12 months.

Analysis
--------

Univariate analyses revealed frequencies and proportions of diagnoses and the distributions of the quantitative response variables. Sample sizes ranged from approximately 420,000 to just over 491,000 responses, comfortably adequate for detecting effects with a power of 0.8 and a significance of 0.05. Given the significant skew in the response variables non-parametric tests of independence were administered to ascertain marginal, conditional and joint associations between independent and response variables.

Reproducing the Analysis
------------------------

This repository is organized as an R Package, providing the functions and raw data to reproduce this analysis. It has been explicitly written for the purpose of this analysis and may not be applicable for general use. The raw data can be found in the data subdirectory. Alternatively, it can be downloaded from the CDC website. <http://www.cdc.gov/brfss/annual_data/2013/files/LLCP2013ASC.ZIP>. The preprocessing and analysis code can be found in the R subdirectory. The vignette directory contains the analysis in the form of an R Markdown document. To reproduce this analysis, you can install chronic from github with:

``` r
# install.packages("devtools")
devtools::install_github("DataScienceSalon/chronic", build_vignettes = TRUE)
```

You may then read the text and figures by executing the following at the R prompt:

``` r
browseVignettes("chronic")
```

The package depends on the following packages:

R Session Information
---------------------

``` r
sessionInfo()
#> R version 3.4.1 (2017-06-30)
#> Platform: x86_64-w64-mingw32/x64 (64-bit)
#> Running under: Windows 10 x64 (build 14393)
#> 
#> Matrix products: default
#> 
#> locale:
#> [1] LC_COLLATE=English_United States.1252 
#> [2] LC_CTYPE=English_United States.1252   
#> [3] LC_MONETARY=English_United States.1252
#> [4] LC_NUMERIC=C                          
#> [5] LC_TIME=English_United States.1252    
#> 
#> attached base packages:
#> [1] stats     graphics  grDevices utils     datasets  methods   base     
#> 
#> loaded via a namespace (and not attached):
#>  [1] compiler_3.4.1  backports_1.1.0 magrittr_1.5    rprojroot_1.2  
#>  [5] tools_3.4.1     htmltools_0.3.6 yaml_2.1.14     Rcpp_0.12.12   
#>  [9] stringi_1.1.5   rmarkdown_1.6   knitr_1.16      stringr_1.2.0  
#> [13] digest_0.6.12   evaluate_0.10.1
```

License
-------

MIT License Copyright (c) 2017 John James <https://opensource.org/licenses/MIT>
