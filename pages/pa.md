# Codebook 相关论文汇总 (2023-2025)

本文档汇总了近几年(2023-2025)关于codebook的重要论文,包括PDF链接和代码仓库地址。
```c
# include 
```
---
- ## 1. VAEVQ: Enhancing Discrete Visual Tokenization through Variational Modeling
  
  **会议/期刊**: AAAI 2026 (Oral)
  
  **发表时间**: 2025年11月
  
  **简介**: 提出变分潜在量化(VLQ)方法,利用VAE的结构化平滑潜在空间促进更有效的码字激活,解决VQ-VAE中的码本崩溃问题。
  
  **PDF链接**:
- ![VAEVQ.pdf](../assets/VAEVQ_1770951505755_0.pdf)
- arXiv: https://arxiv.org/abs/2511.06863
- arXiv PDF: https://arxiv.org/pdf/2511.06863
  
  **代码仓库**:
- GitHub: https://github.com/script-Yang/VAEVQ
  
  **关键创新**:
- Variational Latent Quantization (VLQ)
- Representation Coherence Strategy (RCS)
- Distribution Consistency Regularization (DC）
- ---
- ## 2. Scaling the Codebook Size of VQGAN to 100,000 with a Utilization Rate of 99%
  
  **会议/期刊**: NeurIPS 2024
  
  **发表时间**: 2024年6月
  
  **简介**: 提出VQGAN-LC方法,将codebook大小扩展到10万,利用率达99%,远超传统VQGAN的16,384上限和12%利用率。
  
  **PDF链接**:
- arXiv: https://arxiv.org/abs/2406.11837
- arXiv PDF: https://arxiv.org/pdf/2406.11837
- NeurIPS Proceedings: https://proceedings.neurips.cc/paper_files/paper/2024/file/1716d022edeac750e57a2986a7135e13-Paper-Conference.pdf
  
  **代码仓库**:
- GitHub: https://github.com/zh460045050/VQGAN-LC
  
  **关键创新**:
- 使用预训练视觉编码器初始化码本
- 训练投影器对齐整个码本与编码器特征分布
- 避免传统方法中逐个优化码本条目的问题
  
  ---
- ## 3. MGVQ: Could VQ-VAE Beat VAE? A Generalizable Tokenizer
  
  **会议/期刊**: arXiv 2025
  
  **发表时间**: 2025年7月
  
  **简介**: 通过多组量化方法大幅增强离散码本的表示能力,在ImageNet上达到PSNR 24.70,显著超越其他方法。
  
  **PDF链接**:
- arXiv: https://arxiv.org/abs/2507.07997
- arXiv PDF: https://arxiv.org/pdf/2507.07997
  
  **代码仓库**:
- GitHub: https://github.com/MKJia/MGVQ
- Hugging Face: https://huggingface.co/mkjia/MGVQ
  
  **关键创新**:
- 保留潜在维度以减少信息损失
- 使用多个子码本进行量化
- 嵌套掩码训练策略
- 表示容量扩展超过10亿倍
  
  ---
- ## 4. Vector Quantization using Gaussian Variational Autoencoder (GQ)
  
  **会议/期刊**: arXiv 2025
  
  **发表时间**: 2024-2025年12月
  
  **简介**: 提出使用高斯变分自编码器进行向量量化的新方法,在UNet和ViT架构上都优于VQGAN、FSQ、LFQ等方法。
  
  **PDF链接**:
- arXiv: https://arxiv.org/abs/2512.06609
- arXiv PDF: https://arxiv.org/pdf/2512.06609
  
  **代码仓库**:
- GitHub: https://github.com/tongdaxu/VQ-VAE-from-Gaussian-VAE
  
  **关键特点**:
- 训练高斯VAE后转换为VQ-VAE
- 接近100%的码本使用率
- 保持重建性能
- 灵活设置码本大小、维度和数量
  
  ---
- ## 5. QINCo: Residual Quantization with Implicit Neural Codebooks
  
  **会议/期刊**: ICML 2024
  
  **发表时间**: 2024年1月
  
  **arXiv编号**: 2401.14732
  
  **简介**: 提出使用隐式神经码本的残差量化方法,构建依赖于先前步骤的专用码本,在BigANN1M和Deep1M数据集上表现优异。
  
  **PDF链接**:
- arXiv: https://arxiv.org/abs/2401.14732
- arXiv PDF: https://arxiv.org/pdf/2401.14732
  
  **代码仓库**:
- GitHub: https://github.com/facebookresearch/Qinco
  
  **后续工作**:
- **QINCo2** (ICLR 2025): https://arxiv.org/abs/2501.03078
  
  **关键创新**:
- 神经网络预测下一量化步骤的码本
- 码本依赖于之前选择的Voronoi单元
- 动态速率量化器
- 集成束搜索和近似解码
  
  ---
- ## 6. Soft Convex Quantization (SCQ)
  
  **会议/期刊**: ICML 2024
  
  **发表时间**: 2024年
  
  **简介**: 通过可微凸优化解决VQ-VAE中的codebook collapse问题,实现更好的梯度反向传播。
  
  **PDF链接**: 需要进一步搜索ICML 2024论文集
  
  **代码仓库**: 待确认
  
  ---
- ## 7. SGC-VQGAN: Semantic Guided Clustering Codebook
  
  **会议/期刊**: arXiv 2024
  
  **发表时间**: 2024年
  
  **简介**: 利用语义引导聚类构建temporospatially一致的语义codebook,解决codebook collapse和token语义不平衡问题。
  
  **PDF链接**: 需要进一步搜索
  
  **代码仓库**: 待确认
  
  ---
- ## 8. DiVeQ: Differentiable Vector Quantization
  
  **会议/期刊**: arXiv 2025
  
  **发表时间**: 2025年
  
  **arXiv编号**: 2509.26469
  
  **简介**: 使用重参数化技巧实现可微的向量量化。
  
  **PDF链接**: https://arxiv.org/abs/2509.26469 (需验证)
  
  **代码仓库**: 待确认
  
  ---
- ## 9. Topic-VQ-VAE: Leveraging Latent Codebooks for Topic Modeling
  
  **会议/期刊**: arXiv 2024
  
  **发表时间**: 2024年
  
  **简介**: 将VQ-VAE的潜在codebook应用于主题建模,支持文档生成和图像生成。
  
  **PDF链接**: 需要进一步搜索
  
  **代码仓库**: 待确认
  
  ---
- ## 10. Scaling Transformers for Low-Bitrate High-Quality Speech Coding
  
  **会议/期刊**: arXiv 2024
  
  **发表时间**: 2024年11月
  
  **arXiv编号**: 2411.19842
  
  **简介**: 将codebook应用于语音编码领域。
  
  **PDF链接**: https://arxiv.org/abs/2411.19842
  
  **代码仓库**: 待确认
  
  ---
- ## 11. Vector Quantization with Self-Attention for Quality-Independent Recognition
  
  **会议/期刊**: CVPR 2023 (Highlight)
  
  **发表时间**: 2023年
  
  **简介**: 用于低质量图像识别,结合自注意力机制。
  
  **PDF链接**: 需要在CVPR 2023论文集中查找
  
  **代码仓库**: 待确认
  
  ---
- ## 12. Resizing Codebook Without Retraining
  
  **会议/期刊**: Multimedia Systems 2023
  
  **发表时间**: 2023年
  
  **简介**: 提出无需重新训练即可调整codebook大小的方法,利用hyperbolic embeddings和Hilbert curve。
  
  **PDF链接**: 需要在Multimedia Systems期刊查找
  
  **代码仓库**: 待确认
  
  ---
- ## 13. Factorized Visual Tokenization and Generation (FQGAN)
  
  **会议/期刊**: arXiv 2024
  
  **发表时间**: 2024年11月
  
  **简介**: 提出因子化量化设计,将codebook分解为多个独立的子码本,实现更高效和可扩展的视觉tokenization。
  
  **PDF链接**:
- arXiv: https://arxiv.org/abs/2411.16681
- arXiv PDF: https://arxiv.org/pdf/2411.16681
- arXiv HTML: https://arxiv.org/html/2411.16681v1
  
  **代码仓库**: 待确认(论文中提到代码将公开)
  
  **关键创新**:
- 因子化码本设计
- 解耦正则化(disentanglement regularization)
- 表示学习目标
- 在离散图像重建上达到SOTA性能
  
  ---
- ## 14. SimVQ: Addressing Representation Collapse with One Linear Layer
  
  **会议/期刊**: arXiv 2024
  
  **发表时间**: 2024年11月
  
  **简介**: 通过一个线性层解决表示崩溃问题,实现接近100%的码本利用率。
  
  **PDF链接**:
- arXiv: https://arxiv.org/abs/2411.02038
- arXiv HTML: https://arxiv.org/html/2411.02038
  
  **代码仓库**: 待确认
  
  **关键特点**:
- 无论码本大小如何都能保持高利用率
- 在扩大码本时持续提供性能改进
- 在图像和音频任务上建立新的SOTA
  
  ---
- ## 15. OneVAE: Joint Discrete and Continuous Optimization
  
  **会议/期刊**: arXiv 2025
  
  **发表时间**: 2025年8月
  
  **简介**: 联合离散和连续表示优化,使用FSQ保留预训练连续VAE先验。
  
  **PDF链接**:
- arXiv: https://arxiv.org/abs/2508.09857
- arXiv PDF: https://arxiv.org/pdf/2508.09857
  
  **代码仓库**: 待确认
  
  **关键创新**:
- 多token量化机制
- 第一帧增强(用于因果VAE)
- 双路径优化
  
  ---
- ## 相关资源
- ### 综述与教程
- **VQ-VAE综述**: https://www.emergentmind.com/topics/vector-quantization-variational-autoencoder-vq-vae
- ### 相关工具库
- **Faiss**: Facebook AI的向量检索库 - https://github.com/facebookresearch/faiss
- ### 数据集
  
  常用的评估数据集:
- ImageNet
- BigANN1M
- Deep1M
- SIFT1M
- AudioCaps (音频)
- WavCaps (音频)
  
  ---
- ## 论文分类
- ### 按研究方向分类:
  
  **1. 提高码本利用率**
- VQGAN-LC (99%利用率)
- MGVQ (接近100%利用率)
- GQ (接近100%利用率)
- SimVQ
  
  **2. 扩展码本容量**
- VQGAN-LC (10万码字)
- MGVQ (十亿倍表示容量)
- FQGAN (因子化码本)
  
  **3. 改进量化策略**
- VAEVQ (变分建模)
- QINCo/QINCo2 (隐式神经码本)
- SCQ (软凸量化)
  
  **4. 应用领域**
- 图像: VQGAN-LC, MGVQ, FQGAN, VAEVQ
- 音频/语音: Scaling Transformers for Speech Coding
- 主题建模: Topic-VQ-VAE
- 图像识别: Vector Quantization with Self-Attention
  
  ---
- ## 搜索建议
  
  如果您需要查找特定论文的完整信息,可以:
- **在arXiv搜索**: https://arxiv.org/
- **在Google Scholar搜索**: https://scholar.google.com/
- **在Papers with Code搜索**: https://paperswithcode.com/
- **在Hugging Face Papers搜索**: https://huggingface.co/papers
  
  **搜索关键词组合**:
- "codebook vector quantization"
- "VQ-VAE 2024"
- "VQGAN codebook"
- "discrete visual tokenization"
- "neural codebook"
  
  ---
- ## 更新日志
- **2025年2月**: 初始版本创建
- 包含15篇主要论文
- 已验证的PDF和代码链接: 5篇
- 待补充详细信息: 10篇