# A 理论课综述初稿

## 3.1-1 病灶检测框

病灶检测框将候选区域标在原始影像上，使阅片者能够逐处核对模型定位。Wang 等提出 EL-DETR，在四个真实数据集上评估病灶检测，并用注意力图展示解码器中内容查询与位置查询的权重（R19）。同样以病灶检测为题，Nayak 等对颊黏膜照片执行正常与异常二分类，其敏感度和特异度衡量的是图像级筛查表现（U397）。因此，评价空间定位时应说明预测框如何与参考框匹配，以及框内区域是否进入后续分类。结合 Teng 等对医学影像可解释性的讨论（U409），若要判断分类器是否依赖框内信息，还需观察改变该区域后预测如何变化。

原文位置：[R19 公开摘要](https://research.polyu.edu.hk/en/publications/an-explainable-lesion-detection-transformer-model-for-medical-ima/) · [U397 Evaluation metrics、Table 2](https://pmc.ncbi.nlm.nih.gov/articles/PMC13127626/) · [U409 综述](https://qims.amegroups.org/article/view/131785/html)

## 3.1-2 语义分割掩膜

语义分割以像素或体素级掩膜描绘目标边界，使阅片者能够核对目标的形状和范围。Dense-Ynet 联合输出胸片肺部掩膜与 ARDS 分类结果，并按肺野象限呈现分类结果（R20）。MedSAM 根据框提示生成目标掩膜，在外部验证中以 Dice 衡量预测掩膜和参考标注的重合程度（R21）。掩膜也可以由分类模型的归因热图经阈值化和后处理得到。Nikulins 等将这种掩膜与参考标注逐像素比较（U399），而 ExShall-CNN 通过移除特定模块后 Dice 的变化评估模块贡献（U400）。这些研究分别说明了掩膜边界如何验证，以及如何检验分割模型对特定模块的依赖。

原文位置：[R20 方法与 Table 1](https://pmc.ncbi.nlm.nih.gov/articles/PMC10581023/) · [R21 Fig. 4](https://www.nature.com/articles/s41467-024-44824-z.pdf) · [U399 Fig. 2–3](https://pmc.ncbi.nlm.nih.gov/articles/PMC11856553/) · [U400 §4.2、Tables 3–4](https://www.mdpi.com/2504-4990/7/1/19)

## 表 3-1 与图 3-0

表 3-1 按方法类别、实际输入、输出、参考标注与指标、医生可核对的内容和原文位置组织。B 提供逐病灶分割和 MedSAM 条目，C 提供联合分割与分类案例。[U401](https://doi.org/10.1109/ictest64710.2025.11042801) 放在体积分割与解释的补充行，实验结果和图表位置待核。R19 全文的框标注和检测指标也待核。

为 C 统筹的图 3-0 提供一组自绘腰椎轴位 MRI 示意。左侧用定位框标出椎间孔，右侧用半透明掩膜描绘硬膜囊边界。绘图可参考[腰椎 MRI 研究 Fig. 2](https://pmc.ncbi.nlm.nih.gov/articles/PMC10566647/)。

合稿时将 R、U 编号替换为全文统一的参考文献编号。
