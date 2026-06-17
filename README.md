# Robust Clustering via Trimming

A Python implementation of robust clustering algorithms based on the trimming principle, evaluated on simulated datasets and real-world Berlin crime data.

---

## Overview

Standard clustering methods like k-means are highly sensitive to outliers. This project implements and compares **five trimming-based robust clustering methods** that automatically detect and exclude a fraction of the most atypical observations during clustering:

| Method | Paradigm |
|---|---|
| Trimmed K-Means | Centroid-based |
| Trimmed K-Medoids | Medoid-based |
| TCLUST | Model-based (Gaussian mixture) |
| Robust Linear Grouping (RLG) | Subspace / PCA-based |
| Robust Clusterwise Linear Regression (RCLR) | Regression-based |

---

## Dataset

Berlin Crime Dataset (2012–2019), shared by the Berlin Police Department via Kaggle:
https://www.kaggle.com/datasets/danilzyryanov/crime-in-berlin-2012-2019

---

## Results Summary

- All methods achieved **ARI > 0.95** on simulated datasets with known ground truth.
- On the Berlin crime data, **Robust Linear Grouping** achieved the best silhouette score (0.704) at `k=2`, `alpha=0.05`.
- Trimmed points in the crime dataset consistently corresponded to subregions with extreme crime rates, validating the trimming approach.

---

## References

1. Becht, E., McInnes, L., Healy, J., Dutertre, C. A., Kwok, I. W. H., Ng, L. G., ... & Newell, E. W. (2019). Dimensionality reduction for visualizing single-cell data using UMAP. *Nature Biotechnology*, 37(1), 38–44. https://doi.org/10.1038/nbt.4314
2. Carlsson, G. (2009). Topology and data. *Bulletin of the American Mathematical Society*, 46(2), 255–308. https://doi.org/10.1090/S0273-0979-09-01249-X
3. Chazal, F., & Michel, B. (2021). An introduction to topological data analysis: fundamental and practical aspects for data scientists. *Frontiers in Artificial Intelligence*, 4, 667963. https://doi.org/10.3389/frai.2021.667963
4. Croux, C., & Haesbroeck, G. (2000). Principal component analysis based on robust estimators of the covariance or correlation matrix: influence functions and efficiencies. *Biometrika*, 87(3), 603–618. https://doi.org/10.1093/biomet/87.3.603
5. Cuesta-Albertos, J. A., Gordaliza, A., & Matrán, C. (1997). Trimmed k-means: An attempt to robustify quantizers. *Computational Statistics & Data Analysis*, 29(1), 43–61.
6. Dempster, A. P., Laird, N. M., & Rubin, D. B. (1977). Maximum likelihood from incomplete data via the EM algorithm. *Journal of the Royal Statistical Society: Series B (Methodological)*, 39(1), 1–38. https://doi.org/10.1111/j.2517-6161.1977.tb01600.x
7. Ester, M., Kriegel, H. P., Sander, J., & Xu, X. (1996). A density-based algorithm for discovering clusters in large spatial databases with noise. In *Proceedings of the Second International Conference on Knowledge Discovery and Data Mining* (pp. 226–231). AAAI Press.
8. Fasy, B. T., Lecci, F., Rinaldo, A., Wasserman, L., Balakrishnan, S., & Singh, A. (2014). Confidence sets for persistence diagrams. *The Annals of Statistics*, 42(6), 2301–2339. https://doi.org/10.1214/14-AOS1252
9. Fraley, C., & Raftery, A. E. (2002). Model-based clustering, discriminant analysis, and density estimation. *Journal of the American Statistical Association*, 97(458), 611–631. https://doi.org/10.1198/016214502760047131
10. Fritz, H., García-Escudero, L. A., & Mayo-Iscar, A. (2013). tclust: An R package for a trimming approach to cluster analysis. *Journal of Statistical Software*, 47(12), 1–26.
11. García-Escudero, L. A., Gordaliza, A., Matrán, C., & Mayo-Iscar, A. (2008). A general trimming approach to robust cluster analysis. *The Annals of Statistics*, 36(3), 1324–1345.
12. García-Escudero, L. A., Gordaliza, A., San Martín, R., Van Aelst, S., & Zamar, R. (2009). Robust Linear Clustering. *Journal of the Royal Statistical Society Series B: Statistical Methodology*, 71(1), 301–318. https://doi.org/10.1111/j.1467-9868.2008.00682.x
13. García-Escudero, L. A., Gordaliza, A., Mayo-Iscar, A., & San Martín, R. (2010). Robust clusterwise linear regression through trimming. *Computational Statistics & Data Analysis*, 54(12), 3057–3069. https://doi.org/10.1016/j.csda.2009.07.002
14. García-Escudero, L. A., Mayo-Iscar, A., & Ortega, J. (2024). Robust clustering based on trimming. *WIREs Computational Statistics*.
15. Hampel, F. R., Ronchetti, E. M., Rousseeuw, P. J., & Stahel, W. A. (1986). *Robust Statistics: The Approach Based on Influence Functions*. Wiley.
16. Hodge, V., & Austin, J. (2004). A survey of outlier detection methodologies. *Artificial Intelligence Review*, 22(2), 85–126. https://doi.org/10.1023/B:AIRE.0000045502.10941.a9
17. Hubert, L., & Arabie, P. (1985). Comparing partitions. *Journal of Classification*, 2, 193–218.
18. Ibáñez, M. V., Viñue, G., Alemany, S., Simó, A., Epifanio, I., Domingo, J., & Ayala, G. (2012). Apparel sizing using trimmed PAM and OWA operators. *Expert Systems with Applications*, 39, 10512–10520.
19. Jolliffe, I. T. (2002). *Principal Component Analysis* (2nd ed.). Springer.
20. Kaufman, L., & Rousseeuw, P. J. (1990). *Finding Groups in Data: An Introduction to Cluster Analysis*. Wiley.
21. Lloyd, S. P. (1982). Least squares quantization in PCM. *IEEE Transactions on Information Theory*, 28(2), 129–137. https://doi.org/10.1109/TIT.1982.1056489
22. Manning, C. D., Raghavan, P., & Schütze, H. (2008). *Introduction to Information Retrieval*. Cambridge University Press.
23. Maronna, R. A., Martin, R. D., Yohai, V. J., & Salibián-Barrera, M. (2019). *Robust Statistics: Theory and Methods (with R)* (2nd ed.). Wiley.
24. McInnes, L., Healy, J., & Melville, J. (2018). UMAP: Uniform Manifold Approximation and Projection for dimension reduction. *arXiv preprint* arXiv:1802.03426.
25. Murtagh, F., & Contreras, P. (2012). Algorithms for hierarchical clustering: an overview. *Wiley Interdisciplinary Reviews: Data Mining and Knowledge Discovery*, 2(1), 86–97. https://doi.org/10.1002/widm.53
26. Rousseeuw, P. J. (1984). Least median of squares regression. *Journal of the American Statistical Association*, 79(388), 871–880. https://doi.org/10.1080/01621459.1984.10477105
27. Rousseeuw, P. J., & Leroy, A. M. (1987). *Robust Regression and Outlier Detection*. Wiley.
28. Rousseeuw, P. J., & Van Driessen, K. (1999). A fast algorithm for the minimum covariance determinant estimator. *Technometrics*, 41(3), 212–223. https://doi.org/10.1080/00401706.1999.10485670
29. Roweis, S. T., & Saul, L. K. (2000). Nonlinear dimensionality reduction by locally linear embedding. *Science*, 290(5500), 2323–2326. https://doi.org/10.1126/science.290.5500.2323
30. Singh, G., Mémoli, F., & Carlsson, G. (2007). Topological methods for the analysis of high dimensional data sets and 3D object recognition. In *SPBG'07: Proceedings of the Eurographics Symposium on Point-Based Graphics* (pp. 91–100). Eurographics Association.
31. Tenenbaum, J. B., de Silva, V., & Langford, J. C. (2000). A global geometric framework for nonlinear dimensionality reduction. *Science*, 290(5500), 2319–2323. https://doi.org/10.1126/science.290.5500.2319
32. van der Maaten, L., & Hinton, G. (2008). Visualizing data using t-SNE. *Journal of Machine Learning Research*, 9, 2579–2605.
33. Wasserman, L. (2018). Topological data analysis. *Annual Review of Statistics and Its Application*, 5, 501–532. https://doi.org/10.1146/annurev-statistics-031017-100045
34. Zomorodian, A., & Carlsson, G. (2005). Computing persistent homology. *Discrete & Computational Geometry*, 33(2), 249–274. https://doi.org/10.1007/s00454-004-1146-y
35. Zyryanov, D. (2019). Crime in Berlin, Germany, 2012–2019 [Dataset]. Kaggle. https://www.kaggle.com/datasets/danilzyryanov/crime-in-berlin-2012-2019
