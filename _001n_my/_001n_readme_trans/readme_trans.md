> 本文件是 [`show_and_tell/README.md`](../../README.md) 的中文翻译。论文英文标题、作者、链接、代码与引用格式保持原样。

## 最新动态

* 预训练模型与演示（demos）现已发布！
* 完整代码——即将发布！

# Show and Tell：基于空间感知概念瓶颈模型的视觉可解释深度神经网络 [CVPR'25]

<div>
  <img src="../../docs/salf-cbm-gif-v2.gif" style="width:100%">
</div>
<br>

<a href="https://itaybenou.github.io/show-and-tell/"><img src="https://img.shields.io/static/v1?label=Project&message=Website&color=red" height=20.5></a>
<a href="https://arxiv.org/abs/2502.20134"><img src="https://img.shields.io/badge/arXiv-2502.20134-b31b1b.svg" height=20.5></a>

> **Show and Tell: Visually Explainable Deep Neural Nets via Spatially-Aware Concept Bottleneck Models**
>
> Itay Benou, Tammy Riklin-Raviv
>
> 摘要：现代深度神经网络已在多种任务上达到人类水平。然而，与人类不同，它们无法通过指出“在哪里”、说出是哪些概念引导了判断，来解释自身的决策。在这项工作中，我们提出了一个统一的框架，可将任意视觉神经网络转变为在空间与概念两个层面都可解释的模型。我们引入了一种空间感知的概念瓶颈层（spatially-aware concept bottleneck layer），该层无需人工标注，就能把预训练骨干网络的“黑盒”特征投影为可解释的概念图（concept maps）。在该瓶颈之上训练一个分类层，我们便得到一个自解释模型：它能阐明哪些概念对预测影响最大，并给出热力图，在输入图像中标出这些概念的位置。据此，我们将该方法命名为“Spatially-Aware and Label-Free Concept Bottleneck Model”（SALF-CBM，空间感知且无需标签的概念瓶颈模型）。结果表明，所提出的 SALF-CBM：(1) 在多种分类任务上优于非空间（non-spatial）的 CBM 方法，也优于原始骨干网络；(2) 能生成高质量的空间解释，在零样本分割任务上优于广泛使用的基于热力图的方法；(3) 便于模型探索与调试，用户可以查询特定的图像区域，并通过局部编辑概念图来改进模型的决策。

## 安装

1. 克隆仓库。
2. 安装 Python（3.9）与 PyTorch（1.13）。
3. 运行 `pip install -r requirements.txt`。
4. 运行 `bash download_model.sh` 下载预训练模型。
5. 下载 [ViT-B SAM 模型 checkpoint](https://dl.fbaipublicfiles.com/segment_anything/sam_vit_b_01ec64.pth)，并将其放在 `segment_anything/checkpoint` 文件夹下。

## 运行演示

按照以下 notebook 中的说明操作：

1. 解释模型预测：`demos/model_explainability.ipynb`。
2. Explain Anything 功能：`demos/explain_anything.ipynb`。
3. 模型调试功能：`demos/model_debugging.ipynb`。

## 引用本文

Itay Benou and Tammy Riklin Raviv, [*Show and Tell: Visually Explainable Deep Neural Nets via Spatially-Aware Concept Bottleneck Models*](https://openaccess.thecvf.com/content/CVPR2025/papers/Benou_Show_and_Tell_Visually_Explainable_Deep_Neural_Nets_via_Spatially-Aware_CVPR_2025_paper.pdf), CVPR 2025.

```
@inproceedings{benou2025show,
  title={Show and Tell: Visually Explainable Deep Neural Nets via Spatially-Aware Concept Bottleneck Models},
  author={Benou, Itay and Raviv, Tammy Riklin},
  booktitle={Proceedings of the Computer Vision and Pattern Recognition Conference},
  pages={30063--30072},
  year={2025}
}
```
