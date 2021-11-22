# iMAAPssmry

```iMAAPs``` is a powerful tool to estimate multiple-wave population admixed time, which is currently designed to infer the two-way, multiple-wave admixture based on admixture induced LD. This software can deal with genotype data, haplotype data and the data re-coded according to admixture ancestries.

For more details of iMAAPs, see https://github.com/Shuhua-Group/iMAAPs.

**iMAAPssmry V0.2**

```iMAAPssmry``` is an R package providing the function to summary spectrum and admixture time interval of the output files of iMAAPs.

## Install and load the package
To install the package, please use ```devtools```
```
devtools::install_github("Chen-SHuangHui/iMAAPssmry0.2");
library(iMAAPssmry0.2);
```

## Summary spectrum and admixture time interval
```
data(ad_inp);
data(rawld_inp);

x <- iMAAPssmry(ad_inp = ad_inp,rawld_inp = rawld_inp, denoise_cut = 0.99, num_chr = 10);
#summary spectrum
> x$sum_spectrum
      gen          mag
 [1,]   0 0.0017808938
 [2,]  47 0.0078082779
 [3,]  48 0.0166346230
 [4,]  49 0.0213023051
 [5,]  50 0.0241563812
 [6,]  51 0.0281666768
 [7,]  52 0.0283945524
 [8,]  53 0.0246115749
 [9,]  54 0.0195652641
[10,]  55 0.0140609798
[11,]  56 0.0093997124
[12,]  57 0.0003601793

#estimated admixture time
> x$time
       median       SD       pvalue         mag       mag_sd      prop
[1,]  0.00000 0.000000 1.152493e-08 0.001780894 0.0003210443 0.1919001
[2,] 51.48246 2.394118 2.834765e-08 0.028394552 0.0063921496 0.8080999
```

# Citation
If you use ```iMAAPs``` in your research, please cite

Zhou Y, Yuan K, Yu Y, Ni X, Xie P, Xing EP, Xu S. Inference of multiple-wave population admixture by modeling decay of linkage disequilibrium with polynomial functions. Heredity (Edinb). 2017 May;118(5):503-510. doi: 10.1038/hdy.2017.5. Epub 2017 Feb 15. PMID: 28198814; PMCID: PMC5564381.

(Link:https://www.nature.com/articles/hdy20175)




