# qkeras-mod
This is an extension of the original QKeras repository: [github.com/google/qkeras](https://github.com/google/qkeras).

The main novelty of this extension is the added support to affine uniform quantization [1][2][3] for activation layers by introducing a new layer called _quantized_bits_featuremaps_, to be used when _alpha=auto_.

It also provides some modifications to AutoQKeras, such as the support to Batch Normalization fusion.

The explanation of all the modifications is in: Terlizzi, M. Alessio, "Mixed-precision Quantization and Inference of MLPerf Tiny DNNs on Precision-Scalable Hardware Accelerators", 2023, Politecnico di Torino. Accessed: Dec. 7, 2023. [Online]. Available: https://webthesis.biblio.polito.it/26664/.

## New files
Create a new conda environment using _qkeras-env.yml_, replace the original files of QKeras with the following ones, and then follow _QKeras_Unveiled-final.ipynb_:
- autoqkeras/autoqkeras_internal.py
- autoqkeras/forgiving_metrics/forgiving_bits.py
- qkeras/quantizers.py
- qkeras/utils.py

## Publications using this code

- Luca Urbinati and Mario R. Casu, "High-Level Design of Precision-Scalable DNN Accelerators Based on Sum-Together Multiplier", in the review process.

## References

[1] B. Jacob et al., "Quantization and Training of Neural Networks for Efficient Integer-Arithmetic-Only Inference," arXiv:1712.05877 [cs, stat], Dec. 2017. Available: http://arxiv.org/abs/1712.05877

[2] Mao, Lei. "Quantization for Neural Networks". Lei Mao’s Log Book, May 17, 2020, https://leimao.github.io/article/Neural-Networks-Quantization/

[3] H. Wu, P. Judd, X. Zhang, M. Isaev, and P. Micikevicius, “Integer Quantization for Deep Learning Inference: Principles and Empirical Evaluation,” arXiv:2004.09602 [cs, stat], Apr. 2020, Accessed: Dec. 22, 2021. [Online]. Available: http://arxiv.org/abs/2004.09602.


