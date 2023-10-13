---
layout: page
title: Dilated Unet
description: medical image segmentation by introducing DilatedUNet
img: assets/img/project_2.jpg
importance: 2
category: work
giscus_comments: true
---

This paper introduces DilatedUNet, a novel approach that combines a Dilated Transformer block with the U-Net architecture to enhance medical image segmentation by effectively addressing global context and spatial relationship challenges, achieving fast and accurate results that outperform existing methods on challenging benchmarks like Synapse and ISIC.

Explore our innovative network architecture, DilatedUNet, at the forefront of medical image segmentation, combining the power of Dilated Transformers with the U-Net structure for superior results on complex tasks:


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/Dilated.svg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The architecture of Dilated-Unet, which is composed of encoder, bottleneck, decoder and skip connections. Encoder, bottleneck
    and decoder are all constructed based on Dilated transformer block.
</div>



The DiNA (Dilated Neighborhood Attention) block deviates from conventional multi-head self-attention modules and operates as a sparse yet potent global operation when coupled with the local-only Neighborhood Attention (NA) module. Illustrated in Figure below, a pair of consecutive DiNA transformer blocks features LayerNorm (LN), Neighborhood Attention (NA), Dilated Neighborhood Attention (DiNA), a residual connection, and a 2-layer MLP with GELU nonlinearity. These transformer blocks employ both sliding-window Neighborhood Attention (NA) and Dilated Neighborhood Attention (DiNA) modules, providing a versatile and efficient attention mechanism that can be sequentially applied for enhanced performance.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/Dilated-block.svg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The overview of Dilated Transformer block, which is composed of NA, MLP, DiNa and Layer Norms.
</div>


The visualization of our organ body segmentation model showcases its remarkable performance, surpassing prior research in segmenting numerous organs, notably excelling in liver, spleen, left kidney, stomach, and gallbladder segmentation where it achieves the top results. Even for the remaining organs, our model secures the second-best results. Furthermore, a compelling qualitative example depicted in Figure 3 illustrates the method's outstanding performance. It closely mirrors ground truth data, faithfully representing the actual organ structures, making it a visually convincing demonstration of the model's excellence.


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/body-organ.svg" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Comparative segmentation results on the Synapse dataset.
</div>
