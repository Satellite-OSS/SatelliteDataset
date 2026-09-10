<p align="right">
  <strong>English</strong> | <a href="./README_CN.md">简体中文</a>
</p>

# Open Satellite Imagery Datasets

A curated and continuously maintained list of open satellite remote-sensing datasets, with concise descriptions, applications, and access links.

**31 datasets and dataset series** · **9 research areas**

## Contents

- [Quick index](#quick-index)
- [Foundation models and large-scale pretraining](#foundation-models-and-large-scale-pretraining) · 4
- [Scene classification and land cover](#scene-classification-and-land-cover) · 6
- [Object detection and instance segmentation](#object-detection-and-instance-segmentation) · 5
- [Semantic segmentation and mapping](#semantic-segmentation-and-mapping) · 4
- [Change detection and disaster assessment](#change-detection-and-disaster-assessment) · 4
- [Agriculture and satellite time series](#agriculture-and-satellite-time-series) · 3
- [Cloud detection and removal](#cloud-detection-and-removal) · 2
- [Remote-sensing vision-language data](#remote-sensing-vision-language-data) · 2
- [Open raw satellite imagery](#open-raw-satellite-imagery) · 1

## Quick index

| Dataset | Primary tasks | Imagery source | Scale / coverage |
| --- | --- | --- | --- |
| [MajorTOM-Core](#majortom-core) | Large-scale pretraining | Sentinel-1/2 | Millions of image patches |
| [SSL4EO-S12](#ssl4eo-s12) | Self-supervised pretraining | Sentinel-1/2 | 251,079 locations, four seasons |
| [SatlasPretrain](#satlaspretrain) | Multitask pretraining | Satellite + NAIP aerial imagery | 302M labels, 137 categories |
| [M3LEO](#m3leo) | Multimodal learning | Sentinel-1/2 and more | Georegistered multimodal data |
| [BigEarthNet v2.0](#bigearthnet-v20) | Multilabel classification | Sentinel-1/2 | 549,488 patch pairs |
| [EuroSAT](#eurosat) | Scene classification | Sentinel-2 | 27,000 images, 10 classes |
| [NWPU-RESISC45](#nwpu-resisc45) | Scene classification | Google Earth | 31,500 images, 45 classes |
| [SEN12MS](#sen12ms) | Land cover and data fusion | Sentinel-1/2 | 180,662 aligned samples |
| [So2Sat LCZ42](#so2sat-lcz42) | Local climate zone classification | Sentinel-1/2 | 400,673 patches, 17 classes |
| [fMoW](#fmow) | Functional site classification | Commercial satellite imagery | 62 classes, multitemporal |
| [xView](#xview) | Small-object detection | WorldView-3 | Over 1M objects, 60 classes |
| [DOTA v2.0](#dota-v20) | Oriented object detection | Satellite + aerial imagery | 11,268 large images, 18 classes |
| [RSOD](#rsod) | Object detection | Optical remote-sensing imagery | 976 images, 6,950 objects |
| [HRSID](#hrsid) | SAR ship detection and segmentation | TerraSAR-X, Sentinel-1B, and more | 5,604 images, 16,951 instances |
| [xView3-SAR](#xview3-sar) | SAR ship detection | Sentinel-1 | Nearly 1,000 SAR scenes |
| [SpaceNet](#spacenet) | Building and road extraction | WorldView, Planet, SAR, and more | Multiple challenge datasets |
| [OpenEarthMap](#openearthmap) | Land-cover segmentation | Satellite + aerial imagery | 5,000 images, 44 countries, 8 classes |
| [LoveDA](#loveda) | Urban-rural segmentation and adaptation | Google Earth | 5,987 images, 7 classes |
| [Sen1Floods11](#sen1floods11) | Flood segmentation | Sentinel-1/2 | 11 flood events |
| [xBD / xView2](#xbd--xview2) | Building damage assessment | Pre/post-disaster satellite imagery | Multiple disasters, 4 damage levels |
| [LEVIR-CD](#levir-cd) | Building change detection | Google Earth | 637 pairs, 31,333 change instances |
| [S2Looking](#s2looking) | Off-nadir building change detection | High-resolution satellite imagery | 5,000 bitemporal pairs |
| [DynamicEarthNet](#dynamicearthnet) | Semantic change segmentation | PlanetScope | 75 sites, daily imagery |
| [PASTIS-R](#pastis-r) | Crop classification and parcel segmentation | Sentinel-1/2 | 2,433 sequences, 18 crop classes |
| [Sen4AgriNet](#sen4agrinet) | Crop classification and field segmentation | Sentinel-2 | Multicountry, multiyear series |
| [Fields of the World](#fields-of-the-world) | Field-boundary extraction | Bitemporal Sentinel-2 | More than 24 countries |
| [AllClear](#allclear) | Cloud removal and reconstruction | Sentinel-1/2, Landsat 8/9 | 23,742 regions |
| [CloudSEN12](#cloudsen12) | Cloud and cloud-shadow segmentation | Sentinel-2 with Sentinel-1 context | 49,400 patches |
| [ChatEarthNet](#chatearthnet) | Captioning and image-text retrieval | Sentinel-2 | 163,488 + 10,000 image-text pairs |
| [RS5M](#rs5m) | Vision-language pretraining | Multisource remote-sensing and web imagery | About 5M image-text pairs |
| [Maxar Open Data](#maxar-open-data) | Disaster response and change analysis | Maxar commercial satellite imagery | Organized by disaster event |

## Foundation models and large-scale pretraining

### MajorTOM-Core

A large-scale satellite imagery collection built around ESA Phi-Lab's Major TOM grid and data organization framework. Its common spatial index and metadata structure support regional, sensor-specific, and processing-level subsets for foundation-model pretraining, representation learning, and retrieval.

- **Imagery and data**: Sentinel-2 L1C/L2A and Sentinel-1 RTC, with Copernicus DEM elevation data.
- **Scale and coverage**: Near-global coverage, millions of image patches, and tens of terabytes.
- **Key feature**: Modality-specific storage aligned through a shared spatial grid.

**Resources**: [GitHub](https://github.com/ESA-PhiLab/Major-TOM) · [Dataset collection](https://huggingface.co/Major-TOM)

### SSL4EO-S12

A multimodal, multiseason satellite dataset for self-supervised learning. Each location contains SAR and optical observations at two processing levels, enabling cross-sensor and cross-season representation learning without task-specific manual labels.

- **Imagery and data**: Dual-polarization Sentinel-1 SAR plus Sentinel-2 L1C and L2A at four seasonal timestamps.
- **Scale and coverage**: 251,079 global locations and about 1.5 TB of raw data.
- **Additional information**: Pretrained weights are available; the data and weights use CC BY 4.0.

**Resources**: [GitHub](https://github.com/zhu-xlab/SSL4EO-S12) · [Data](https://mediatum.ub.tum.de/1660427)

### SatlasPretrain

A multitask remote-sensing pretraining dataset released by the Allen Institute for AI. It connects satellite and aerial imagery with several forms of geospatial labels and supports detection, segmentation, classification, regression, and downstream model fine-tuning.

- **Imagery and labels**: Sentinel-1/2, Landsat 8/9, NAIP aerial imagery, and more; labels include points, lines, polygons, and raster targets.
- **Scale and coverage**: About 302M labels, 137 categories, and 7 label types. Label count is not image count.
- **Additional information**: Imagery and labels retain licenses from their respective sources.

**Resources**: [GitHub](https://github.com/allenai/satlas) · [Data](https://huggingface.co/allenai/satlas-pretrain) · [Pretrained models](https://github.com/allenai/satlaspretrain_models)

### M3LEO

A dataset for multimodal Earth-observation learning that aligns optical, radar, and geophysical data geographically. It supports cross-modal representation learning, data fusion, land-cover classification, and regression of variables such as biomass or elevation.

- **Imagery and data**: Sentinel-1, Sentinel-2, InSAR products, land cover, biomass, elevation, and other auxiliary layers.
- **Key feature**: Georegistered modalities can be combined into different model inputs and prediction targets.

**Resources**: [GitHub](https://github.com/spaceml-org/M3LEO) · [Dataset collection](https://huggingface.co/M3LEO)

[Back to index](#quick-index)

## Scene classification and land cover

### BigEarthNet v2.0

A large-scale multilabel land-cover benchmark with paired SAR and optical imagery for each location. Samples may contain several land-cover types and support multilabel classification, cross-modal fusion, and pretraining evaluation.

- **Imagery and labels**: Sentinel-1 and Sentinel-2 L2A, with multilabel and pixel-level reference maps derived from CORINE Land Cover 2018.
- **Scale and coverage**: 549,488 paired patches across 10 European countries.
- **Additional information**: These figures refer to v2.0; the reference maps are derived from an existing land-cover product rather than newly annotated pixel by pixel.

**Resources**: [Website and data](https://bigearth.net/) · [Community documentation](https://github.com/kai-tub/ben-docs)

### EuroSAT

A Sentinel-2 land-use and land-cover scene-classification dataset with one category per image. Its RGB and full multispectral versions are compact enough for classification baselines, teaching, and training-pipeline validation.

- **Imagery and labels**: Sentinel-2 RGB and 13-band multispectral images with image-level class labels.
- **Scale and coverage**: 27,000 images at 64 × 64 pixels across 10 classes.

**Resources**: [GitHub](https://github.com/phelber/EuroSAT) · [Data](https://doi.org/10.5281/zenodo.7711810)

### NWPU-RESISC45

A large remote-sensing scene-classification benchmark released by Northwestern Polytechnical University. It covers natural and human-made scenes such as airports, harbors, industrial areas, residential areas, farmland, forests, and rivers.

- **Imagery and labels**: RGB images collected from Google Earth, each with one scene label.
- **Scale and coverage**: 31,500 images at 256 × 256 pixels, 45 classes, and 700 images per class, covering more than 100 countries.
- **Resolution**: Approximately 0.2–30 m per pixel, varying by class and region.
- **Source note**: The original material identifies Google Earth as the source but does not disclose the satellite or aerial platform for each image.

**Resources**: [Paper](https://arxiv.org/abs/1703.00121) · [TensorFlow Datasets](https://www.tensorflow.org/datasets/catalog/resisc45) · [Hugging Face mirror](https://huggingface.co/datasets/timm/resisc45)

### SEN12MS

A global, multiseason dataset of aligned SAR, optical, and land-cover reference data. Each sample contains three georegistered components for land-cover understanding, multimodal fusion, and cross-modal representation learning.

- **Imagery and labels**: Sentinel-1 SAR, Sentinel-2 multispectral imagery, and MODIS land-cover reference maps.
- **Scale and coverage**: 180,662 aligned samples at 256 × 256 pixels.
- **Additional information**: The MODIS reference has a coarser native resolution and should not be treated as precise manually drawn segmentation.

**Resources**: [GitHub](https://github.com/schmitt-muc/SEN12MS) · [Data](https://mediatum.ub.tum.de/1474000)

### So2Sat LCZ42

A multimodal satellite dataset for Local Climate Zone classification. Its classes describe built form and natural surface characteristics, while spatial and city-based splits support evaluation of geographic generalization.

- **Imagery and labels**: Paired Sentinel-1 and Sentinel-2 patches with image-level LCZ labels.
- **Scale and coverage**: 400,673 patches at 32 × 32 pixels across 17 classes.
- **Version note**: The official v4.2 release provides corrected geolocation files; a March 2026 notice describes fixes to EPSG and related fields.

**Resources**: [GitHub](https://github.com/zhu-xlab/So2Sat-LCZ42) · [Data](https://huggingface.co/datasets/zhu-xlab/So2Sat-LCZ42)

### fMoW

Functional Map of the World classifies the function of a location, such as an airport, harbor, hospital, or power plant, rather than only its visual land-cover type. It combines target regions, multitemporal satellite observations, and acquisition metadata.

- **Imagery and labels**: Commercial satellite RGB or multispectral imagery with bounding boxes, functional classes, and acquisition metadata.
- **Scale and coverage**: 62 classes; about 200 GB for RGB and about 3.5 TB for the full multispectral release.
- **Additional information**: This entry describes the original fMoW dataset, not the Sentinel-2-based fMoW-Sentinel derivative.

**Resources**: [GitHub and download instructions](https://github.com/fMoW/dataset) · [AWS data catalog](https://registry.opendata.aws/spacenet/)

[Back to index](#quick-index)

## Object detection and instance segmentation

### xView

A high-resolution satellite object-detection dataset covering fine-grained vehicles, vessels, buildings, and infrastructure. Dense small objects, complex backgrounds, and class imbalance make it useful for evaluating detectors in difficult overhead scenes.

- **Imagery and labels**: WorldView-3 optical imagery at about 0.3 m resolution with bounding boxes and class labels.
- **Scale and coverage**: More than 1M objects across 60 classes and over 1,400 km².

**Resources**: [Dataset website](http://xviewdataset.org/) · [GitHub organization](https://github.com/DIUx-xView)

### DOTA v2.0

A benchmark for oriented object detection in remote-sensing imagery. Rotated quadrilaterals describe aircraft, ships, vehicles, bridges, and other objects in large images with diverse scales, orientations, and densities.

- **Imagery and labels**: Mixed satellite and aerial imagery from Google Earth, GF-2, JL-1, and aerial platforms, with oriented quadrilateral annotations.
- **Scale and coverage**: 11,268 large images, 18 classes, and about 1.8M object instances.
- **Additional information**: Figures refer to DOTA v2.0; use is restricted to academic purposes.

**Resources**: [GitHub toolkit](https://github.com/CAPTAIN-WHU/DOTA_devkit) · [Data](https://captain-whu.github.io/DOTA/dataset.html)

### RSOD

A compact optical remote-sensing object-detection dataset released by Wuhan University. It contains four common target categories and is useful for introductory detection experiments, lightweight model validation, and small-object detection.

- **Imagery and labels**: Optical remote-sensing images with horizontal bounding boxes in PASCAL VOC format.
- **Scale and coverage**: 976 images and 6,950 object instances.
- **Class distribution**: 4,993 aircraft, 1,586 oil tanks, 180 overpasses, and 191 playgrounds.
- **Source note**: The official repository does not disclose the satellite or aerial platform for each image and provides category-specific downloads through Baidu Netdisk.

**Resources**: [GitHub and download instructions](https://github.com/RSIA-LIESMARS-WHU/RSOD-Dataset-) · [Paper](https://ieeexplore.ieee.org/document/7827088)

### HRSID

A high-resolution SAR dataset for ship detection and instance segmentation, with both ship locations and object masks. It covers harbors, coastal waters, and open-sea conditions under varying imaging settings.

- **Imagery and labels**: TerraSAR-X, Sentinel-1B, and other SAR satellite imagery with bounding boxes and instance masks.
- **Scale and coverage**: 5,604 images and 16,951 ship instances at 0.5 m, 1 m, and 3 m resolutions.

**Resources**: [GitHub and download instructions](https://github.com/chaozhong2010/HRSID)

### xView3-SAR

A SAR benchmark motivated by the detection of illegal, unreported, and unregulated fishing. Tasks include vessel localization, attribute classification, and length estimation over large maritime scenes.

- **Imagery and labels**: Sentinel-1 SAR with vessel annotations and auxiliary rasters such as bathymetry and wind fields.
- **Scale and coverage**: Nearly 1,000 large SAR scenes.
- **Access note**: Downloading the data requires registration and sign-in on the xView3 website.

**Resources**: [GitHub baseline](https://github.com/DIUx-xView/xview3-reference) · [Data](https://iuu.xview.us/)

[Back to index](#quick-index)

## Semantic segmentation and mapping

### SpaceNet

A series of high-resolution satellite-imagery challenges rather than one fixed dataset. Tasks span building footprints, road networks, travel-time estimation, multitemporal urban change, and flood-related infrastructure mapping.

- **Imagery and labels**: WorldView, Planet, commercial SAR, and other imagery with challenge-specific building, road, or disaster labels.
- **Key feature**: Individual challenges provide task definitions, metrics, baselines, and data documentation.
- **Additional information**: Resolution, scale, access method, and license vary by challenge.

**Resources**: [GitHub organization](https://github.com/SpaceNetChallenge) · [AWS data catalog](https://registry.opendata.aws/spacenet/)

### OpenEarthMap

A global high-resolution land-cover segmentation benchmark that unifies satellite and aerial imagery under an eight-class label system. It supports semantic segmentation, domain adaptation, and cross-country generalization.

- **Imagery and labels**: Satellite and aerial RGB imagery at 0.25–0.5 m resolution with manual pixel-level labels.
- **Scale and coverage**: 5,000 images and about 2.2M segments across 97 regions in 44 countries.
- **Access note**: The release does not bundle the xBD RGB images; the full dataset requires downloading xBD separately and following the compilation instructions.
- **License note**: Licenses vary by source, and some regions have noncommercial restrictions.

**Resources**: [GitHub](https://github.com/bao18/open_earth_map) · [Data](https://doi.org/10.5281/zenodo.7223446) · [Project website](https://open-earth-map.org/)

### LoveDA

A land-cover segmentation dataset designed around urban-rural domain differences in Wuhan, Nanjing, and Changzhou. Variation in object scale, class balance, and appearance supports supervised segmentation and unsupervised domain-adaptation studies.

- **Imagery and labels**: High-resolution Google Earth imagery with seven pixel-level land-cover classes.
- **Scale and coverage**: 5,987 images covering urban and rural areas in three Chinese cities.
- **Source and license**: Google Earth is listed as the source, which alone does not identify the satellite-to-aerial ratio. Academic use only.

**Resources**: [GitHub](https://github.com/JunJue-Wang/LoveDA) · [Data](https://doi.org/10.5281/zenodo.5706578)

### Sen1Floods11

A georegistered satellite dataset for flood-extent mapping, organized around flood events from multiple regions. It supports SAR flood segmentation, weak supervision, and cross-event evaluation.

- **Imagery and labels**: Sentinel-1 SAR, Sentinel-2 multispectral imagery, hand-labeled water masks, and weak labels.
- **Scale and coverage**: 11 flood events and about 14 GB; 512 × 512 pixel patches on a 10 m grid.
- **Key feature**: Includes georeferenced imagery, event metadata, and train/test splits; label sources should be distinguished during use.

**Resources**: [GitHub and download instructions](https://github.com/cloudtostreet/Sen1Floods11)

[Back to index](#quick-index)

## Change detection and disaster assessment

### xBD / xView2

xBD is the dataset used by the xView2 disaster-damage assessment challenge. It pairs pre- and post-disaster high-resolution satellite imagery and combines building localization with damage grading rather than only binary change detection.

- **Imagery and labels**: Pre/post-disaster pairs, building polygons, and four damage levels: no damage, minor damage, major damage, and destroyed.
- **Scale and coverage**: Multiple regions and natural-disaster types.
- **Access note**: The download page may require registration or sign-in.

**Resources**: [GitHub baseline](https://github.com/DIUx-xView/xView2_baseline) · [Data](https://xview2.org/dataset)

### LEVIR-CD

A bitemporal building change-detection benchmark focused on building construction and removal. Image pairs are separated by 5–14 years and support binary change segmentation over long-term urban development.

- **Imagery and labels**: Google Earth imagery at about 0.5 m resolution with binary building-change masks.
- **Scale and coverage**: 637 pairs at 1024 × 1024 pixels and 31,333 building-change instances.
- **Source and license**: Google Earth is listed as the source, which alone does not identify the satellite-to-aerial ratio. Academic use only.

**Resources**: [GitHub](https://github.com/justchenhao/LEVIR) · [Project website and data](https://justchenhao.github.io/LEVIR/)

### S2Looking

A building change-detection dataset built from off-nadir satellite imagery. It emphasizes viewpoint variation and complex rural scenes, where changing look angles alter building appearance and projected position.

- **Imagery and labels**: Bitemporal high-resolution off-nadir satellite imagery with building-change annotations. “S2” in the name does not mean Sentinel-2.
- **Scale and coverage**: 5,000 pairs at 1024 × 1024 pixels, more than 65,920 change instances, and about 0.5–0.8 m resolution.

**Resources**: [GitHub and download instructions](https://github.com/S2Looking/Dataset)

### DynamicEarthNet

A satellite time-series dataset combining frequent imagery with semantic land-cover change labels. Daily observations record surface dynamics while monthly annotations provide supervision for temporal segmentation and change modeling.

- **Imagery and labels**: PlanetScope multispectral time series with monthly pixel-level labels across seven land-cover classes.
- **Scale and coverage**: 75 sites worldwide with daily image observations.
- **Additional information**: Imagery and labels have different temporal frequencies; not every daily image has a manual annotation.

**Resources**: [GitHub](https://github.com/aysim/dynnet) · [Data](https://mediatum.ub.tum.de/1650201)

[Back to index](#quick-index)

## Agriculture and satellite time series

### PASTIS-R

A radar-optical agricultural parcel benchmark and multimodal extension of PASTIS. Semantic crop classes and parcel instance IDs support classification, semantic segmentation, instance segmentation, and panoptic segmentation.

- **Imagery and labels**: Sentinel-2 multispectral series and ascending/descending Sentinel-1 series with crop classes and parcel instances.
- **Scale and coverage**: 2,433 time-series samples, 124,422 agricultural parcels, and 18 crop classes.

**Resources**: [GitHub](https://github.com/VSainteuf/pastis-benchmark) · [Data](https://doi.org/10.5281/zenodo.5735646)

### Sen4AgriNet

A multicountry, multiyear agricultural time-series dataset whose labels come from farmer declarations and land-parcel identification systems. It supports crop classification, field segmentation, and generalization across regions and years.

- **Imagery and labels**: Sentinel-2 multispectral time series with crop and parcel information.
- **Scale and coverage**: Multiyear observations from regions including France and Catalonia, Spain.
- **Key feature**: Includes object-based and patch-based organization; the size of the underlying parcel archive is not the number of directly trainable image samples.

**Resources**: [GitHub](https://github.com/Orion-AI-Lab/S4A) · [Data](https://huggingface.co/datasets/orion-ai-lab/S4A) · [Baseline models](https://github.com/Orion-AI-Lab/S4A-Models)

### Fields of the World

A global benchmark for cross-region field-boundary extraction. It standardizes multiple open parcel-label sources and pairs them with bitemporal satellite imagery for field mapping, instance segmentation, and cross-country generalization.

- **Imagery and labels**: Sentinel-2 RGB and near-infrared imagery from two seasons with field boundaries and masks.
- **Scale and coverage**: More than 24 countries across Europe, Africa, Asia, and South America.
- **Key feature**: Standardized data, source inventories, and baseline code help preserve label provenance across regions.

**Resources**: [GitHub baselines](https://github.com/fieldsoftheworld/ftw-baselines) · [Data](https://source.coop/ftw/benchmark-data) · [Source inventory](https://github.com/fieldsoftheworld/ftw-datasets-list)

[Back to index](#quick-index)

## Cloud detection and removal

### AllClear

A multisensor time-series benchmark for cloud removal in optical satellite imagery. Radar, optical, and multitemporal observations provide complementary information for reconstructing cloud-obscured surfaces.

- **Imagery and data**: Sentinel-1, Sentinel-2, and Landsat 8/9 observations from 2022.
- **Scale and coverage**: 23,742 regions worldwide and about 4M images.
- **Access note**: The official repository provides `download.py` for retrieving data and metadata.

**Resources**: [GitHub and download instructions](https://github.com/Zhou-Hangyu/allclear) · [Project website](https://allclear.cs.cornell.edu/)

### CloudSEN12

A dataset for cloud and cloud-shadow understanding in Sentinel-2 imagery. It includes human annotations at different levels of detail and outputs from existing cloud detectors for cloud masking, shadow segmentation, and quality assessment.

- **Imagery and labels**: Sentinel-2 optical imagery with Sentinel-1, DEM, water, land-cover, and other auxiliary data.
- **Scale and coverage**: The original version contains 49,400 image patches across every continent except Antarctica.
- **Additional information**: Annotation detail and coverage vary across subsets; not every patch has an equally detailed dense manual label.

**Resources**: [GitHub](https://github.com/cloudsen12/dataset) · [Project website and data](https://cloudsen12.github.io/)

[Back to index](#quick-index)

## Remote-sensing vision-language data

### ChatEarthNet

A Sentinel-2 image-text dataset that uses ESA WorldCover semantics to help generate detailed natural-language descriptions and includes a manual verification stage. It supports captioning, retrieval, and vision-language model training.

- **Imagery and labels**: Sentinel-2 imagery with descriptions generated by large language and vision-language models.
- **Scale and coverage**: 163,488 GPT-3.5-captioned pairs plus 10,000 GPT-4V-captioned pairs. These are pair counts, not counts of unique locations.
- **Additional information**: Most captions are model-generated rather than written individually by humans; data and model weights use CC BY 4.0.

**Resources**: [GitHub](https://github.com/zhu-xlab/ChatEarthNet) · [Data](https://doi.org/10.5281/zenodo.11003436)

### RS5M

A large remote-sensing image-text pretraining dataset assembled from filtered public web data and automatically captioned remote-sensing datasets. It supports vision-language alignment, zero-shot classification, and cross-modal retrieval.

- **Imagery and labels**: Filtered LAION, COYO, and related web data, plus image-text pairs from fMoW, BigEarthNet, MillionAID, and other remote-sensing datasets.
- **Scale and coverage**: About 5M image-text pairs and roughly 500 GB.
- **Source and license**: This is a multisource collection. The original satellite or aerial sensor cannot be uniformly verified for its web subset, and licenses follow the component sources.

**Resources**: [GitHub](https://github.com/om-ai-lab/RS5M) · [Data](https://huggingface.co/datasets/omlab/RS5M)

[Back to index](#quick-index)

## Open raw satellite imagery

### Maxar Open Data

The Maxar Open Data Program releases high-resolution satellite imagery for major natural disasters and humanitarian events. It is an event-based imagery collection rather than a uniformly labeled machine-learning benchmark and can support disaster mapping, change analysis, and custom annotation.

- **Imagery and data**: Maxar commercial satellite imagery captured before, during, or after individual events.
- **Data organization**: Cloud Optimized GeoTIFF imagery discoverable through data catalogs and a STAC browser.
- **Additional information**: The GitHub link below is a community-maintained catalog. Event coverage, imagery, and license terms follow the publisher's documentation.

**Resources**: [AWS data catalog](https://registry.opendata.aws/maxar-open-data/) · [STAC browser](https://radiantearth.github.io/stac-browser/#/external/maxar-opendata.s3.dualstack.us-west-2.amazonaws.com/events/catalog.json) · [Community GitHub catalog](https://github.com/opengeos/maxar-open-data)

[Back to index](#quick-index)

---

Last reviewed: **2026-09-10**
