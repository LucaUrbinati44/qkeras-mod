# qkeras-mod
This is an extension of the original [QKeras](https://github.com/google/qkeras) repository (commit hash number 4d61681d71c27a872dce96926a3f20908e0c7854).

The main novelty of this extension is the added support to affine uniform quantization [1][2][3] for activation layers by introducing a new layer called _quantized_bits_featuremaps_.

It also provides some modifications to AutoQKeras, such as the support to Batch Normalization fusion.

The explanation of all the modifications is in [4]. 

## How to start
Create a new conda environment using the provided _qkeras-env.yml_ environment, replace the original files of QKeras with the following ones, and then follow [_qkeras-mod-explained.ipynb_](https://github.com/LucaUrbinati44/qkeras-mod/blob/main/qkeras-mod-explained.ipynb):
- _autoqkeras/autoqkeras_internal.py_ -->

  _<your_qkeras-env_installation_path>/autoqkeras/autoqkeras_internal.py_
- _autoqkeras/forgiving_metrics/forgiving_bits.py_ -->

  _<your_qkeras-env_installation_path>/autoqkeras/forgiving_metrics/forgiving_bits.py_ 
- _qkeras/quantizers.py_ ->

  _<your_qkeras-env_installation_path>/qkeras/quantizers.py_
- _qkeras/utils.py_ -->

  _<your_qkeras-env_installation_path>/qkeras/utils.py_

## If using this code, please cite our work
```
@ARTICLE{urbinati2024access,
author={Urbinati, Luca and Casu, Mario R.},
journal={IEEE Access}, 
title={High-Level Design of Precision-Scalable DNN Accelerators Based on Sum-Together Multipliers}, 
year={2024},
volume={12},
number={},
pages={44163-44189},
doi={10.1109/ACCESS.2024.3380472}}
```


## References
[1] B. Jacob et al., "Quantization and Training of Neural Networks for Efficient Integer-Arithmetic-Only Inference," arXiv:1712.05877 [cs, stat], Dec. 2017. Available: http://arxiv.org/abs/1712.05877

[2] Mao, Lei. "Quantization for Neural Networks". Lei Mao’s Log Book, May 17, 2020, https://leimao.github.io/article/Neural-Networks-Quantization/

[3] H. Wu, P. Judd, X. Zhang, M. Isaev, and P. Micikevicius, “Integer Quantization for Deep Learning Inference: Principles and Empirical Evaluation,” arXiv:2004.09602 [cs, stat], Apr. 2020, Accessed: Dec. 22, 2021. [Online]. Available: http://arxiv.org/abs/2004.09602.

[4] Terlizzi, M. Alessio, "Mixed-precision Quantization and Inference of MLPerf Tiny DNNs on Precision-Scalable Hardware Accelerators", 2023, Politecnico di Torino. Accessed: Dec. 7, 2023. [Online]. Available: https://webthesis.biblio.polito.it/26664/.

