# Table 8: Mean Absolute Errors for MODNet Models on OQMD Halogen-Containing Materials

This folder contains the data corresponding to **Table 8** from the paper, which presents the mean absolute errors (MAE) for MODNet models on the tasks of prediction of convex hull distance and band gap on the subset of halogen-containing materials from OQMD. The table compares the inclusion of all GNN featurizers over the original MatMiner features. In parentheses, the percentage MAE deviation from the default MatMiner featurizer in MODNet on the given task is shown.

### Features Compared:
- **Default MatMiner (MM)**: The default featurizer used in MODNet.
- **MM + MEGNet ℓ-OFM**: Combines the default MatMiner features with latent OFM features generated by MEGNet.
- **MM + MEGNet ℓ-OFM + MEGNetPreL32**: Combines the default MatMiner features with latent OFM features and features from a pre-trained MEGNet model with 32 layers.
- **OMEGA**: Combines the default MatMiner features with latent OFM features by MEGNet proxy, features from a pre-trained MEGNet model with 32 layers, and adjacent MEGNet model features.

### Results:
| Features                              | MAE (eV) OQMD halogen Ehull (N=31,271) | MAE (eV) OQMD halogen Eg (N=8,518) |
|---------------------------------------|----------------------------------------|--------------------------------------|
| **Default MatMiner (MM)**             | 0.0556                                | 0.4557                               |
| **MM + MEGNet ℓ-OFM**                 | 0.0561 (+0.8%)                        | 0.4501 (-1.2%)                       |
| **MM + MEGNet ℓ-OFM + MEGNetPreL32**  | 0.0538 (-3.2%)                        | 0.3835 (-15.8%)                      |
| **OMEGA**                             | 0.0519 (-6.7%)                        | 0.3784 (-17.0%)                      |

### Citation:
If you use these results in your work, please cite the original paper:

- Rogério Almeida Gouvêa, Pierre-Paul De Breuck, Tatiane Pretto, Gian-Marco Rignanese, Marcos José Leite dos Santos, *Boosting feature-based machine learning models for materials science: encoding electronic descriptors and graph-based features for enhanced accuracy and faster featurization*.