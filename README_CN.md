<h1 align="center">Open Satellite Imagery Datasets</h1>

<p align="center">
一个持续整理和维护开源卫星遥感数据集的项目，汇集数据集简介、应用方向及相关链接。
</p>

<p align="center">
  <a href="./README.md"><img src="https://img.shields.io/badge/English-555555?style=for-the-badge" alt="Switch to English" height="28"></a>
  <img src="https://img.shields.io/badge/简体中文-0969da?style=for-the-badge" alt="简体中文（当前语言）" height="28">
</p>

<p align="center"><strong>31 个数据集与数据系列</strong> &nbsp;·&nbsp; <strong>9 个主题方向</strong></p>

<details>
<summary><strong>目录</strong></summary>

- [快速索引](#快速索引)
- [基础模型与大规模预训练](#基础模型与大规模预训练) · 4
- [场景分类与土地覆盖](#场景分类与土地覆盖) · 6
- [目标检测与实例分割](#目标检测与实例分割) · 5
- [语义分割与地物制图](#语义分割与地物制图) · 4
- [变化检测与灾害评估](#变化检测与灾害评估) · 4
- [农业与卫星时间序列](#农业与卫星时间序列) · 3
- [云检测与云去除](#云检测与云去除) · 2
- [遥感视觉语言](#遥感视觉语言) · 2
- [开放原始卫星影像](#开放原始卫星影像) · 1

</details>

## 快速索引

**[基础模型与预训练](#基础模型与大规模预训练) · 4**

| 数据集 | 任务 | 规模 |
| :--- | :--- | ---: |
| [**MajorTOM-Core**](#majortom-core) | 大规模预训练 | 数百万切片 |
| [**SSL4EO-S12**](#ssl4eo-s12) | 自监督学习 | 251,079 个地点 |
| [**SatlasPretrain**](#satlaspretrain) | 多任务学习 | 3.02 亿标签 |
| [**M3LEO**](#m3leo) | 多模态学习 | 多模态配准数据 |

**[场景分类](#场景分类与土地覆盖) · 6**

| 数据集 | 任务 | 规模 |
| :--- | :--- | ---: |
| [**BigEarthNet v2.0**](#bigearthnet-v20) | 多标签土地覆盖 | 549,488 对切片 |
| [**EuroSAT**](#eurosat) | 土地利用与覆盖 | 27,000 张 · 10 类 |
| [**NWPU-RESISC45**](#nwpu-resisc45) | 场景分类 | 31,500 张 · 45 类 |
| [**SEN12MS**](#sen12ms) | SAR 与光学融合 | 180,662 组样本 |
| [**So2Sat LCZ42**](#so2sat-lcz42) | 局地气候区 | 400,673 个切片 |
| [**fMoW**](#fmow) | 功能地点识别 | 62 类 |

**[目标检测](#目标检测与实例分割) · 5**

| 数据集 | 任务 | 规模 |
| :--- | :--- | ---: |
| [**xView**](#xview) | 小目标检测 | 超过 100 万目标 |
| [**DOTA v2.0**](#dota-v20) | 旋转目标检测 | 11,268 张 · 18 类 |
| [**RSOD**](#rsod) | 光学目标检测 | 976 张 · 4 类 |
| [**HRSID**](#hrsid) | SAR 舰船与实例掩膜 | 16,951 个实例 |
| [**xView3-SAR**](#xview3-sar) | SAR 舰船检测 | 近 1,000 景 |

**[语义分割与制图](#语义分割与地物制图) · 4**

| 数据集 | 任务 | 规模 |
| :--- | :--- | ---: |
| [**SpaceNet**](#spacenet) | 建筑与道路提取 | 多项挑战 |
| [**OpenEarthMap**](#openearthmap) | 全球土地覆盖 | 5,000 张 · 44 国 |
| [**LoveDA**](#loveda) | 城乡域适应 | 5,987 张 · 7 类 |
| [**Sen1Floods11**](#sen1floods11) | 洪水范围提取 | 11 次事件 |

**[变化检测与灾害](#变化检测与灾害评估) · 4**

| 数据集 | 任务 | 规模 |
| :--- | :--- | ---: |
| [**xBD / xView2**](#xbd--xview2) | 建筑损毁评估 | 4 级损毁标签 |
| [**LEVIR-CD**](#levir-cd) | 建筑变化检测 | 637 对 |
| [**S2Looking**](#s2looking) | 侧视变化检测 | 5,000 对 |
| [**DynamicEarthNet**](#dynamicearthnet) | 语义时序变化 | 75 个区域 · 每日影像 |

**[农业与时间序列](#农业与卫星时间序列) · 3**

| 数据集 | 任务 | 规模 |
| :--- | :--- | ---: |
| [**PASTIS-R**](#pastis-r) | 作物与地块分割 | 2,433 个序列 |
| [**Sen4AgriNet**](#sen4agrinet) | 作物时间序列 | 多国家、多年份 |
| [**Fields of the World**](#fields-of-the-world) | 农田边界提取 | 24 个以上国家 |

**[云检测与去除](#云检测与云去除) · 2**

| 数据集 | 任务 | 规模 |
| :--- | :--- | ---: |
| [**AllClear**](#allclear) | 云去除 | 23,742 个区域 |
| [**CloudSEN12**](#cloudsen12) | 云与云影分割 | 49,400 个切片 |

**[视觉语言](#遥感视觉语言) · 2**

| 数据集 | 任务 | 规模 |
| :--- | :--- | ---: |
| [**ChatEarthNet**](#chatearthnet) | 描述与图文检索 | 163,488 + 10,000 对 |
| [**RS5M**](#rs5m) | 图文预训练 | 约 500 万对 |

**[原始影像](#开放原始卫星影像) · 1**

| 数据集 | 任务 | 覆盖 |
| :--- | :--- | ---: |
| [**Maxar Open Data**](#maxar-open-data) | 灾害响应 | 按事件组织 |

## 基础模型与大规模预训练

### MajorTOM-Core

基于 ESA Phi-Lab 的 Major TOM 网格与数据组织框架构建的大规模卫星影像数据集。统一的空间索引和元数据结构便于按区域、传感器或处理级别提取子集，主要用于地球观测基础模型预训练、表征学习和影像检索。

- **影像与数据**：Sentinel-2 L1C / L2A、Sentinel-1 RTC，配套 Copernicus DEM 高程数据。
- **规模与覆盖**：近全球覆盖，数百万影像切片，总量达数十 TB。
- **数据特点**：按模态组织数据，支持结合统一网格进行跨数据源匹配。

**资源**：[GitHub](https://github.com/ESA-PhiLab/Major-TOM) · [数据集集合](https://huggingface.co/Major-TOM)

### SSL4EO-S12

面向自监督学习的多模态、多季节卫星影像数据集。同一地点提供 SAR 与两种处理级别的光学观测，可用于学习跨传感器、跨季节的稳定表征，无需依赖人工任务标签。

- **影像与数据**：Sentinel-1 双极化 SAR、Sentinel-2 L1C 和 L2A，包含四季时间点。
- **规模与覆盖**：全球 251,079 个地点，原始数据约 1.5 TB。
- **补充说明**：官方同时提供预训练权重；数据与权重采用 CC BY 4.0。

**资源**：[GitHub](https://github.com/zhu-xlab/SSL4EO-S12) · [数据下载](https://mediatum.ub.tum.de/1660427)

### SatlasPretrain

Allen Institute for AI 发布的多任务遥感预训练数据集，将卫星与航空影像同多种地理要素标签关联。覆盖检测、分割、分类和回归任务，并提供可供下游任务微调的预训练模型。

- **影像与标注**：Sentinel-1/2、Landsat 8/9 和 NAIP 航空影像等；标签包含点、线、面及栅格等形式。
- **规模与覆盖**：约 3.02 亿标签、137 个类别、7 种标签类型；标签数量不等于影像数量。
- **补充说明**：影像与标签来自不同来源，许可按各组成部分分别适用。

**资源**：[GitHub](https://github.com/allenai/satlas) · [数据下载](https://huggingface.co/allenai/satlas-pretrain) · [预训练模型](https://github.com/allenai/satlaspretrain_models)

### M3LEO

面向多模态地球观测学习的数据集，将光学、雷达和地球物理数据在地理位置上对齐。可用于跨模态表征学习、数据融合，以及土地覆盖分类、生物量或高程相关的回归任务。

- **影像与数据**：Sentinel-1、Sentinel-2、InSAR 产品，以及土地覆盖、生物量和高程等辅助数据。
- **数据特点**：不同模态以地理配准方式组织，便于构建输入与预测目标的多种组合。

**资源**：[GitHub](https://github.com/spaceml-org/M3LEO) · [数据集集合](https://huggingface.co/M3LEO)

[返回索引](#快速索引)

## 场景分类与土地覆盖

### BigEarthNet v2.0

大规模多标签土地覆盖基准，同一区域配对提供 SAR 与光学影像。一个样本可同时包含多种土地覆盖类型，适合多标签分类、跨模态融合和遥感预训练评测。

- **影像与标注**：Sentinel-1 与 Sentinel-2 L2A；多标签和像素级参考图来自 CORINE Land Cover 2018。
- **规模与覆盖**：549,488 对影像切片，覆盖欧洲 10 个国家。
- **补充说明**：此处统计对应 v2.0；土地覆盖参考图由现有制图产品生成，并非逐像素人工重标。

**资源**：[官网与数据](https://bigearth.net/) · [社区文档](https://github.com/kai-tub/ben-docs)

### EuroSAT

基于 Sentinel-2 的土地利用与土地覆盖场景分类数据集，每张影像对应一个类别。提供 RGB 与完整多光谱版本，体量较小，适合分类基线、教学实验和训练流程验证。

- **影像与标注**：Sentinel-2，提供 RGB 和 13 波段多光谱影像，以及图像级分类标签。
- **规模与覆盖**：27,000 张 64 × 64 像素影像，10 个类别。

**资源**：[GitHub](https://github.com/phelber/EuroSAT) · [数据下载](https://doi.org/10.5281/zenodo.7711810)

### NWPU-RESISC45

西北工业大学发布的大规模遥感场景分类基准，覆盖机场、港口、工业区、住宅区、农田、森林和河流等多种自然与人工场景。类别数量较多、类内差异明显，适合场景分类、迁移学习和跨区域泛化评估。

- **影像与标注**：从 Google Earth 获取的 RGB 影像，每张影像具有一个场景类别标签。
- **规模与覆盖**：31,500 张 256 × 256 像素影像，45 个类别，每类 700 张；影像来自 100 多个国家。
- **分辨率**：不同类别和区域差异较大，主要约为 0.2–30 m / 像素。
- **来源说明**：原始资料以 Google Earth 标示影像来源，未逐景披露具体卫星或航空平台。

**资源**：[论文](https://arxiv.org/abs/1703.00121) · [TensorFlow Datasets 说明](https://www.tensorflow.org/datasets/catalog/resisc45) · [Hugging Face 镜像](https://huggingface.co/datasets/timm/resisc45)

### SEN12MS

全球多季节的 SAR、光学影像与土地覆盖参考数据集，每个样本由三部分地理配准数据组成。主要用于土地覆盖识别、跨模态数据融合和多模态表征学习。

- **影像与标注**：Sentinel-1 SAR、Sentinel-2 多光谱影像，以及 MODIS 土地覆盖参考图。
- **规模与覆盖**：180,662 组配准样本，切片大小为 256 × 256 像素。
- **补充说明**：MODIS 参考图的原始空间分辨率较低，不等同于精细人工分割标注。

**资源**：[GitHub](https://github.com/schmitt-muc/SEN12MS) · [数据下载](https://mediatum.ub.tum.de/1474000)

### So2Sat LCZ42

用于局地气候区（Local Climate Zone，LCZ）分类的多模态卫星影像数据集。类别反映建筑形态与自然地表特征，提供不同空间和城市划分，支持城市环境识别及跨区域泛化评估。

- **影像与标注**：Sentinel-1 与 Sentinel-2 配对切片，配有图像级 LCZ 标签。
- **规模与覆盖**：400,673 个 32 × 32 像素切片，17 个类别。
- **版本说明**：官方 v4.2 提供修正后的地理定位文件；2026 年 3 月公告说明了 EPSG 等字段的修正。

**资源**：[GitHub](https://github.com/zhu-xlab/So2Sat-LCZ42) · [数据下载](https://huggingface.co/datasets/zhu-xlab/So2Sat-LCZ42)

### fMoW

Functional Map of the World 关注地点的功能用途，例如机场、港口、医院和电站，而不只是地表外观。数据包含目标区域、多时相卫星观测及元数据，适合功能地点分类与时序建模。

- **影像与标注**：商业卫星 RGB / 多光谱影像，配有目标边界框、功能类别和采集元数据。
- **规模与覆盖**：62 个类别；RGB 版本约 200 GB，完整版本约 3.5 TB。
- **补充说明**：这里指原始 fMoW 数据集，不是以 Sentinel-2 构建的 fMoW-Sentinel 衍生版本。

**资源**：[GitHub 与下载说明](https://github.com/fMoW/dataset) · [AWS 数据目录](https://registry.opendata.aws/spacenet/)

[返回索引](#快速索引)

## 目标检测与实例分割

### xView

高分辨率卫星影像目标检测数据集，覆盖车辆、船舶、建筑和基础设施等细粒度类别。大量小目标、复杂背景和类别不均衡使其适合评估密集场景中的检测能力。

- **影像与标注**：WorldView-3 光学影像，约 0.3 m 分辨率，提供目标边界框和类别标签。
- **规模与覆盖**：超过 100 万个目标、60 个类别，影像覆盖超过 1,400 km²。

**资源**：[数据集官网](http://xviewdataset.org/) · [GitHub 组织](https://github.com/DIUx-xView)

### DOTA v2.0

面向任意方向目标检测的遥感基准，使用旋转框描述飞机、舰船、车辆和桥梁等目标。大幅影像中包含多尺度、密集排列及方向变化明显的实例，适合旋转检测与大图切片推理研究。

- **影像与标注**：卫星与航空影像混合，来源包括 Google Earth、GF-2、JL-1 及航空摄影；提供定向四边形标注。
- **规模与覆盖**：11,268 张大幅影像、18 个类别，约 180 万个目标实例。
- **补充说明**：统计对应 DOTA v2.0；仅限学术用途，禁止商业使用。

**资源**：[GitHub 工具集](https://github.com/CAPTAIN-WHU/DOTA_devkit) · [数据下载](https://captain-whu.github.io/DOTA/dataset.html)

### RSOD

武汉大学发布的小型光学遥感目标检测数据集，面向飞机、油罐、立交桥和操场四类典型目标。数据规模较小但飞机目标密集，适合目标检测入门实验、轻量模型验证和小目标检测研究。

- **影像与标注**：光学遥感影像，采用 PASCAL VOC 格式的水平边界框标注。
- **规模与覆盖**：976 张影像，共 6,950 个目标实例。
- **类别分布**：4,993 架飞机、1,586 个油罐、180 座立交桥和 191 个操场。
- **来源说明**：官方仓库未逐景披露具体卫星或航空平台，并通过百度网盘链接提供分类别下载。

**资源**：[GitHub 与下载说明](https://github.com/RSIA-LIESMARS-WHU/RSOD-Dataset-) · [论文](https://ieeexplore.ieee.org/document/7827088)

### HRSID

高分辨率 SAR 舰船检测与实例分割数据集，同时提供舰船位置和轮廓标注。影像覆盖港口、近岸与海面等场景，可用于研究复杂背景及不同成像条件下的舰船识别。

- **影像与标注**：TerraSAR-X、Sentinel-1B 等 SAR 卫星影像，提供舰船边界框和实例掩膜。
- **规模与覆盖**：5,604 张影像、16,951 个舰船实例；分辨率包括 0.5 m、1 m 和 3 m。

**资源**：[GitHub 与下载说明](https://github.com/chaozhong2010/HRSID)

### xView3-SAR

以海上非法、未报告和无管制捕捞监测为背景的 SAR 检测基准。围绕舰船定位、船舶属性和长度估计设置任务，侧重大范围海域中的目标发现。

- **影像与标注**：Sentinel-1 SAR，配有舰船相关标注，以及水深、风场等辅助栅格。
- **规模与覆盖**：近 1,000 景大型 SAR 影像。
- **访问说明**：数据下载需要在 xView3 网站注册并登录。

**资源**：[GitHub 基线](https://github.com/DIUx-xView/xview3-reference) · [数据入口](https://iuu.xview.us/)

[返回索引](#快速索引)

## 语义分割与地物制图

### SpaceNet

由多项挑战组成的高分辨率卫星影像数据集系列，而非单一固定数据集。任务从建筑轮廓、道路网络提取延伸到路网旅行时间估计、多时相城市变化和洪灾基础设施识别。

- **影像与标注**：WorldView、Planet 和商业 SAR 等影像；按挑战提供建筑多边形、道路网络或灾害相关标签。
- **数据特点**：各挑战配套数据说明、评测指标与基线方案，可按具体任务选择。
- **补充说明**：不同挑战的影像分辨率、数据规模与许可分别定义。

**资源**：[GitHub 组织](https://github.com/SpaceNetChallenge) · [AWS 数据目录](https://registry.opendata.aws/spacenet/)

### OpenEarthMap

面向全球高分辨率土地覆盖制图的语义分割基准。将不同地区的卫星与航空影像统一到 8 类标注体系，支持土地覆盖分割、域适应和跨国家泛化评估。

- **影像与标注**：卫星与航空 RGB 影像，0.25–0.5 m 分辨率，提供人工像素级土地覆盖标签。
- **规模与覆盖**：5,000 张影像、约 220 万个分割区域，覆盖 44 个国家的 97 个区域。
- **访问说明**：下载包不含 xBD 部分的原始 RGB 影像；构建完整数据集需另行获取 xBD 并按官方说明合并。
- **许可说明**：不同来源的影像和标签适用不同许可，部分区域有非商业限制。

**资源**：[GitHub](https://github.com/bao18/open_earth_map) · [数据下载](https://doi.org/10.5281/zenodo.7223446) · [项目主页](https://open-earth-map.org/)

### LoveDA

面向城乡差异的土地覆盖语义分割数据集，覆盖武汉、南京和常州的城市与乡村区域。城乡场景在目标尺度、类别比例及背景外观上存在差异，可用于监督分割与无监督域适应。

- **影像与标注**：Google Earth 高分辨率影像，提供 7 类像素级土地覆盖标签。
- **规模与覆盖**：5,987 张影像，覆盖中国 3 个城市的城乡区域。
- **来源与许可**：官方以 Google Earth 标示影像来源，不能仅据此判定卫星与航空影像的比例；仅限学术用途，禁止商业使用。

**资源**：[GitHub](https://github.com/JunJue-Wang/LoveDA) · [数据下载](https://doi.org/10.5281/zenodo.5706578)

### Sen1Floods11

面向洪水范围提取的地理配准卫星影像数据集，围绕不同地区的洪水事件组织观测与水体标签。可用于 SAR 洪水分割、弱监督学习和跨事件评估。

- **影像与标注**：Sentinel-1 SAR 与 Sentinel-2 多光谱影像，包含人工水体标注和弱标签数据。
- **规模与覆盖**：11 次洪水事件，全量约 14 GB；切片为 512 × 512 像素，统一到 10 m 网格。
- **数据特点**：提供地理参考影像、事件元数据及训练 / 测试划分；不同标签来源需分别区分。

**资源**：[GitHub 与下载说明](https://github.com/cloudtostreet/Sen1Floods11)

[返回索引](#快速索引)

## 变化检测与灾害评估

### xBD / xView2

xBD 是 xView2 灾害损毁评估挑战使用的数据集，提供同一区域的灾前、灾后高分辨率卫星影像。任务同时涉及建筑定位与损毁分级，而非仅判断是否发生变化。

- **影像与标注**：灾前 / 灾后影像对、建筑多边形，以及无损、轻微损毁、严重损毁和完全损毁 4 级标签。
- **规模与覆盖**：涵盖多个地区和多种自然灾害事件。
- **访问说明**：下载页面可能要求注册或登录。

**资源**：[GitHub 基线](https://github.com/DIUx-xView/xView2_baseline) · [数据入口](https://xview2.org/dataset)

### LEVIR-CD

双时相建筑变化检测基准，主要标注建筑新增与消失。影像间隔为 5–14 年，适合研究长期城市建设变化及二值变化区域分割。

- **影像与标注**：Google Earth 约 0.5 m 分辨率影像，提供建筑变化二值掩膜。
- **规模与覆盖**：637 对 1024 × 1024 像素影像，共 31,333 个建筑变化实例。
- **来源与许可**：官方以 Google Earth 标示影像来源，不能仅据此判定卫星与航空影像的比例；仅限学术用途，禁止商业使用。

**资源**：[GitHub](https://github.com/justchenhao/LEVIR) · [项目主页与下载](https://justchenhao.github.io/LEVIR/)

### S2Looking

面向侧视卫星影像的建筑变化检测数据集，侧重视角变化与复杂乡村背景带来的挑战。不同离轴角度会造成建筑外观和投影位置差异，可用于评估变化检测模型的视角鲁棒性。

- **影像与标注**：高分辨率侧视卫星影像对，配有建筑变化标注；名称中的 S2 不代表 Sentinel-2。
- **规模与覆盖**：5,000 对 1024 × 1024 像素影像，超过 65,920 个变化实例；分辨率约 0.5–0.8 m。

**资源**：[GitHub 与下载说明](https://github.com/S2Looking/Dataset)

### DynamicEarthNet

将高频卫星观测与土地覆盖语义变化结合的时间序列数据集。每日影像记录地表演变，按月标签提供监督信号，适合时序语义分割、变化检测及稀疏标签下的时空建模。

- **影像与标注**：PlanetScope 多光谱时间序列，按月提供 7 类土地覆盖像素级标注。
- **规模与覆盖**：全球 75 个研究区域，提供每日影像观测。
- **补充说明**：影像与标注的时间频率不同，并非每张日观测影像都有人工标签。

**资源**：[GitHub](https://github.com/aysim/dynnet) · [数据下载](https://mediatum.ub.tum.de/1650201)

[返回索引](#快速索引)

## 农业与卫星时间序列

### PASTIS-R

融合雷达与光学时间序列的农业地块分割基准，是 PASTIS 的多模态扩展。语义类别与地块实例编号同时提供，可支持作物分类、语义分割、实例分割和全景分割。

- **影像与标注**：Sentinel-2 多光谱序列与 Sentinel-1 升降轨序列，配有作物类别和地块实例标签。
- **规模与覆盖**：2,433 个时间序列样本、124,422 个农业地块、18 种作物。

**资源**：[GitHub](https://github.com/VSainteuf/pastis-benchmark) · [数据下载](https://doi.org/10.5281/zenodo.5735646)

### Sen4AgriNet

多国家、多年份的农业遥感时间序列数据集，以农户申报及土地地块识别系统数据构建标签。可用于作物类型识别、农田分割，以及跨年份和跨地区的模型迁移评估。

- **影像与标注**：Sentinel-2 多光谱序列，配有作物标签与农业地块信息。
- **规模与覆盖**：包含法国和西班牙加泰罗尼亚等区域的多年观测。
- **数据特点**：提供面向对象与影像切片的数据组织方式；基础地块档案规模不等于可直接训练的影像样本数量。

**资源**：[GitHub](https://github.com/Orion-AI-Lab/S4A) · [数据下载](https://huggingface.co/datasets/orion-ai-lab/S4A) · [基线模型](https://github.com/Orion-AI-Lab/S4A-Models)

### Fields of the World

面向跨区域农田边界提取的全球基准，将多个开放地块数据源统一为一致格式，并与双时相卫星影像配对。重点支持农田范围识别、地块实例分割和跨国家泛化。

- **影像与标注**：两个季节的 Sentinel-2 RGB 与近红外影像，配有地块边界和掩膜。
- **规模与覆盖**：覆盖欧洲、非洲、亚洲和南美洲的 24 个以上国家。
- **数据特点**：提供标准化数据、来源清单和基线代码，便于追溯不同地区的标注来源。

**资源**：[GitHub 基线](https://github.com/fieldsoftheworld/ftw-baselines) · [数据下载](https://source.coop/ftw/benchmark-data) · [数据来源清单](https://github.com/fieldsoftheworld/ftw-datasets-list)

[返回索引](#快速索引)

## 云检测与云去除

### AllClear

面向光学卫星影像云去除的多传感器时间序列基准，结合雷达、光学和多时相观测，为被云遮挡的地表恢复提供互补信息。可用于多时相影像重建与多传感器融合。

- **影像与数据**：Sentinel-1、Sentinel-2、Landsat 8/9，覆盖 2022 年的观测。
- **规模与覆盖**：全球 23,742 个研究区域，约 400 万张影像。
- **访问说明**：官方仓库提供 `download.py`，用于获取数据及元数据。

**资源**：[GitHub 与下载说明](https://github.com/Zhou-Hangyu/allclear) · [项目主页](https://allclear.cs.cornell.edu/)

### CloudSEN12

面向 Sentinel-2 云与云影识别的数据集，提供不同精细程度的人工标注，以及可用于对比的云检测结果。适合云掩膜生成、云影分割与卫星影像质量评估。

- **影像与标注**：Sentinel-2 光学影像，配套 Sentinel-1、DEM、水体和土地覆盖等辅助数据。
- **规模与覆盖**：原始版本包含 49,400 个影像切片，覆盖除南极洲外的各大陆。
- **补充说明**：不同子集的标注精细程度与覆盖情况不同，不能将全部切片视为同等质量的稠密人工标注。

**资源**：[GitHub](https://github.com/cloudsen12/dataset) · [项目主页与数据](https://cloudsen12.github.io/)

[返回索引](#快速索引)

## 遥感视觉语言

### ChatEarthNet

基于 Sentinel-2 的图文配对数据集，利用 ESA WorldCover 土地覆盖信息辅助生成自然语言描述，并引入人工核验流程。可用于遥感图像描述、图文检索和视觉语言模型训练。

- **影像与标注**：Sentinel-2 影像与大语言模型生成的文本描述。
- **规模与覆盖**：163,488 个 GPT-3.5 描述图文对，另有 10,000 个 GPT-4V 描述图文对；这些数字按图文配对统计，不表示独立地理位置数量。
- **补充说明**：文本主要由模型生成，不等同于逐条人工撰写的描述；数据与模型权重采用 CC BY 4.0。

**资源**：[GitHub](https://github.com/zhu-xlab/ChatEarthNet) · [数据下载](https://doi.org/10.5281/zenodo.11003436)

### RS5M

大规模遥感图文预训练数据集，由公开图文数据中的遥感相关样本与已有遥感数据集的自动描述构成。可用于视觉语言对齐、零样本分类和跨模态检索。

- **影像与标注**：包括从 LAION、COYO 等筛选的图文数据，以及 fMoW、BigEarthNet、MillionAID 等遥感数据的图文配对。
- **规模与覆盖**：约 500 万个图文对，数据体量约 500 GB。
- **来源与许可**：属于多来源汇编，网络子集不能统一确认到具体卫星或航空传感器；许可与使用限制按组成来源分别适用。

**资源**：[GitHub](https://github.com/om-ai-lab/RS5M) · [数据下载](https://huggingface.co/datasets/omlab/RS5M)

[返回索引](#快速索引)

## 开放原始卫星影像

### Maxar Open Data

Maxar Open Data Program 按重大自然灾害和人道主义事件开放高分辨率卫星影像。它是事件影像资源集合，不是统一标注的机器学习基准，可作为灾害制图、变化分析与自定义标注的数据来源。

- **影像与数据**：Maxar 高分辨率商业卫星影像，按事件提供灾前、灾中或灾后观测。
- **数据组织**：提供云优化 GeoTIFF（COG）影像，可通过数据目录和 STAC 浏览器检索。
- **补充说明**：下方 GitHub 链接为社区维护的影像目录；具体事件、影像覆盖和许可以发布方数据说明为准。

**资源**：[AWS 数据目录](https://registry.opendata.aws/maxar-open-data/) · [STAC 浏览器](https://radiantearth.github.io/stac-browser/#/external/maxar-opendata.s3.dualstack.us-west-2.amazonaws.com/events/catalog.json) · [GitHub 社区目录](https://github.com/opengeos/maxar-open-data)

[返回索引](#快速索引)

---

最近整理：**2026-09-10**
