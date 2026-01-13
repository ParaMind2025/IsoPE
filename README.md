

<div align="center">

# RiemannFormer: A Framework for Attention in Curved Spaces

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Github](https://img.shields.io/badge/Github-RiemannFormer-black?logo=github)](https://github.com)
[![Framework](https://img.shields.io/badge/PyTorch-2.0%2B-ee4c2c.svg)](https://pytorch.org/)
[![arXiv](https://img.shields.io/badge/arXiv-2506.07405-b31b1b.svg)](https://arxiv.org/abs/2506.07405)
[![Math](https://img.shields.io/badge/Geometry-Riemannian)](https://en.wikipedia.org/wiki/Riemannian_geometry)

“Spacetime tells matter how to move;
matter tells spacetime how to curve.”

— John Archibald Wheeler

</div>

Official implementation of the paper **"RiemannFormer: A Framework for Attention in Curved Spaces"**.

We introduce **RiemannFormer**, a paradigm shift that reimagines the Transformer through the lens of differential geometry. By rejecting the implicit flat Euclidean assumption of standard Self-Attention, we posit that token embeddings reside on a **Curved Riemannian Manifold**.

Our framework introduces **PaTESO (Parallel Transport of Embeddings via Subspace Orientation)**, a geometrically principled position encoding derived from the isomorphism $\mathfrak{so}(4) \cong \mathfrak{su}(2)_L \oplus \mathfrak{su}(2)_R$. This allows us to decouple **Flat Translation** from **Intrinsic Curvature**, enabling a dynamic geometry where *"Matter determines the Metric"*.

## 🚀 News & Updates

*   **[2025-06-10]** 🏆 **SOTA Efficiency:** Our metric-gated architecture outperforms standard ViT and RoPE variants on CIFAR benchmarks with high parameter efficiency.


## 🏗️ Methodology

### 0.

<div align="center">

[![New paradigm]](./figs/figure-1.pdf)

</div>

### 1. The Attention Manifold
We model the interaction between tokens $n$ and $m$ as **Parallel Transport** $\mathcal{P}_{n \to m}$ along a geodesic. The transport operator is factorized into a flat component and a curvature component:

$$
\mathcal{P}_{n \to m} = \underbrace{\exp\left( \Delta \mathbf{p}_{nm} \cdot \mathbf{J}_L \right)}_{\text{Flat Translation}} \cdot \underbrace{\exp\left( \lambda \cdot \Omega_{nm} \cdot \mathbf{J}_R \right)}_{\text{Symplectic Curvature}}
$$

### 2. Matter Determines Geometry (Metric Gating)
Unlike standard attention where the metric is fixed ($\mathbf{I}$), we learn a **Dynamic Riemannian Metric** $\mathbf{g}_{ij} = s_i s_j$. The scaling factor $s_i$ is derived directly from the semantic content (Matter):

$$
s_i = \sigma(\text{Proj}(\mathbf{x}_i))
$$

This allows the model to spatially expand salient regions (foreground) and compress noise (background), effectively acting as a **"Gravitational Lens"** for information flow.


## 💻 Usage



## 📂 Project Structure



## 🖊️ Citation

If you find this work helpful or inspiring, please cite us:

```bibtex
@article{2025riemannformer,
  title={RiemannFormer: A Framework for Attention in Curved Spaces},
  author={Zhongping Ji},
  journal={arXiv preprint arXiv:2506.07405},
  year={2025}
}
```

## 🙏 Acknowledgement
We stand on the shoulders of giants. This work draws inspiration from **Riemannian geometry**，**General Relativity**, **Gauge Theory**.
