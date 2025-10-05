---
permalink: /
title: ""
excerpt: ""
author_profile: true
redirect_from: 
  - /about/
  - /about.html
---

{% if site.google_scholar_stats_use_cdn %}
{% assign gsDataBaseUrl = "https://cdn.jsdelivr.net/gh/" | append: site.repository | append: "@" %}
{% else %}
{% assign gsDataBaseUrl = "https://raw.githubusercontent.com/" | append: site.repository | append: "/" %}
{% endif %}
{% assign url = gsDataBaseUrl | append: "google-scholar-stats/gs_data_shieldsio.json" %}

<span class='anchor' id='about-me'></span>

👋 Hi there! My name is Zeqing Wang (王则清).

I am currently pursuing a Master of Science in Computer Engineering at the National University of Singapore. Previously, I obtained my bachelor degree in computer science from Xidian University. 

Currently, my research interests include:

- Efficient AI: model compression, model acceleration, distributed computing.

- Diffusion Models: Video Diffusion Models, Diffusion Language Models.

- Continual Learning and Transfer Learning.


# 🔥 News
- 2025.08: ⛵ Start my Msc. journey in NUS!
- 2025.06: 🎉 Got my Bachelor degree from Xidian University! Thanks to my supervisor and all my friends in XDU!

# 📝 Publications 

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">Preprint</div><img src='https://github.com/INV-WZQ/SparseD/blob/main/assets/demo.gif?raw=true' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[**SparseD: Sparse Attention for Diffusion Language Models**](https://arxiv.org/abs/2509.24014) <img src='https://img.shields.io/github/stars/INV-WZQ/SparseD.svg?style=social&label=Star' alt="sym" height="100%">

**Zeqing Wang**, Gongfan Fang, Xinyin Ma, Xingyi Yang, Xinchao Wang

<div style="display: inline">
    <a href="https://arxiv.org/abs/2509.24014"> <strong>[paper]</strong></a>
    <a href="https://github.com/INV-WZQ/SparseD"> <strong>[code]</strong></a>
    <a class="fakelink" onclick="$(this).siblings('.abstract').slideToggle()" ><strong>[abstract]</strong></a>
    <div class="abstract"  style="overflow: hidden; display: none;">  
        <p> While diffusion language models (DLMs) offer a promising alternative to autoregressive models (ARs), existing open-source DLMs suffer from high inference latency. This bottleneck is mainly due to the attention's quadratic complexity with respect to context length in computing all query-key pairs. Intuitively, to reduce this complexity, a natural strategy is to restrict attention to sparse patterns that retain only the most relevant connections. Such approaches are well-established in ARs, where attention follows fixed and clearly defined sparse patterns. However, in DLMs, we observe distinct sparsity behaviors: (1) attention patterns vary across heads, (2) attention patterns in each head remain highly similar across denoising steps, and (3) early denoising steps are critical for generation. These findings render sparse attention methods designed for ARs largely incompatible with DLMs, as they fail to capture head-specific structures and risk degrading generation when applied in early denoising steps. To address these challenges, we propose SparseD, a novel sparse attention method for DLMs. Leveraging the observations, SparseD only requires pre-computing head-specific sparse patterns one time, and reuses them across all steps. This prevents recomputing sparse patterns at each denoising step. Meanwhile, SparseD uses full attention in the early steps, then switches to sparse attention later to maintain generation quality. Together, these establish SparseD as a practical and efficient solution for deploying DLMs in long-context applications. Experimental results demonstrate that SparseD achieves lossless acceleration, delivering up to 1.50x speedup over FlashAttention at a 64k context length with 1,024 denoising steps. </p>
    </div>
</div>

</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">Preprint</div><img src='https://github.com/DualParal-Project/DualParal/blob/main/assets/gif1.gif?raw=true' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[**Minute-Long Videos with Dual Parallelisms**](https://arxiv.org/abs/2505.21070) <img src='https://img.shields.io/github/stars/DualParal-Project/DualParal.svg?style=social&label=Star' alt="sym" height="100%">

**Zeqing Wang**, Bowen Zheng, Xingyi Yang, Zhenxiong Tan, Yuecong Xu, Xinchao Wang

<div style="display: inline">
    <a href="https://dualparal-project.github.io/dualparal.github.io/"> <strong>[project page]</strong></a>
    <a href="https://arxiv.org/abs/2505.21070"> <strong>[paper]</strong></a>
    <a href="https://github.com/DualParal-Project/DualParal"> <strong>[code]</strong></a>
    <a class="fakelink" onclick="$(this).siblings('.abstract').slideToggle()" ><strong>[abstract]</strong></a>
    <div class="abstract"  style="overflow: hidden; display: none;">  
        <p> Diffusion Transformer (DiT)-based video diffusion models generate high-quality videos at scale but incur prohibitive processing latency and memory costs for long videos. To address this, we propose a novel distributed inference strategy, termed DualParal. The core idea is that, instead of generating an entire video on a single GPU, we parallelize both temporal frames and model layers across GPUs. However, a naive implementation of this division faces a key limitation: since diffusion models require synchronized noise levels across frames, this implementation leads to the serialization of original parallelisms. We leverage a block-wise denoising scheme to handle this. Namely, we process a sequence of frame blocks through the pipeline with progressively decreasing noise levels. Each GPU handles a specific block and layer subset while passing previous results to the next GPU, enabling asynchronous computation and communication. To further optimize performance, we incorporate two key enhancements. Firstly, a feature cache is implemented on each GPU to store and reuse features from the prior block as context, minimizing inter-GPU communication and redundant computation. Secondly, we employ a coordinated noise initialization strategy, ensuring globally consistent temporal dynamics by sharing initial noise patterns across GPUs without extra resource costs. Together, these enable fast, artifact-free, and infinitely long video generation. Applied to the latest diffusion transformer video generator, our method efficiently produces 1,025-frame videos with up to 6.54x lower latency and 1.48x lower memory cost on 8xRTX 4090 GPUs.  </p>
    </div>
</div>


</div>
</div>

<div class='paper-box'><div class='paper-box-image'><div><div class="badge">ASP-DAC 2025</div><img src='https://github.com/INV-WZQ/LightCL/blob/main/image/method.png?raw=true' alt="sym" width="100%"></div></div>
<div class='paper-box-text' markdown="1">

[**LightCL: Compact Continual Learning with Low Memory Footprint For Edge Device**](https://arxiv.org/abs/2407.10545) <img src='https://img.shields.io/github/stars/INV-WZQ/LightCL.svg?style=social&label=Star' alt="sym" height="100%">

**Zeqing Wang**, Fei Cheng, Kangye Ji, Bohu Huang

<div style="display: inline">
    <a href="https://arxiv.org/abs/2407.10545"> <strong>[paper]</strong></a>
    <a href="https://github.com/INV-WZQ/LightCL"> <strong>[code]</strong></a>
    <a class="fakelink" onclick="$(this).siblings('.abstract').slideToggle()" ><strong>[abstract]</strong></a>
    <div class="abstract"  style="overflow: hidden; display: none;">  
        <p> Continual learning (CL) is a technique that enables neural networks to constantly adapt to their dynamic surroundings. Despite being overlooked for a long time, this technology can considerably address the customized needs of users in edge devices. Actually, most CL methods require huge resource consumption by the training behavior to acquire generalizability among all tasks for delaying forgetting regardless of edge scenarios. Therefore, this paper proposes a compact algorithm called LightCL, which evaluates and compresses the redundancy of already generalized components in structures of the neural network. Specifically, we consider two factors of generalizability, learning plasticity and memory stability, and design metrics of both to quantitatively assess generalizability of neural networks during CL. This evaluation shows that generalizability of different layers in a neural network exhibits a significant variation. Thus, we Maintain Generalizability by freezing generalized parts without the resource-intensive training process and  Memorize Feature Patterns by stabilizing feature extracting of previous tasks to enhance generalizability for less-generalized parts with a little extra memory, which is far less than the reduction by freezing. Experiments illustrate that LightCL outperforms other state-of-the-art methods and reduces at most 6.16x memory footprint. We also verify the effectiveness of LightCL on the edge device.  </p>
    </div>
</div>

</div>
</div>


# 🎖 Honors and Awards
- 2021-2025(B.Eng.): National Scholarship of 2021-2022, National Scholarship of 2022-2023, 2025 CCF Elite Collegiate Award, Duan Baoyan Innovation Fund (Only 4 undergraduate students at Xidian University)


# 📖 Educations
- *2025.08 - (now)*, Msc. Student in College of Design and Engineering, National University of Singapore
- *2021.09 - 2025.06*, B.Eng. in Computer Science and Technology, Xidian University


