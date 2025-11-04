---
cover-image: https://upload.wikimedia.org/wikipedia/commons/c/c6/Tajikistan_wikivoyage_banner.jpg
date: 2025-01-01
theme: theme_name
tags: glaciers,climate,third-pole

---

# Glacier monitoring under global warming trends through remote sensing – An example from The Third Pole  <!--{ as="img" mode="hero" src="https://upload.wikimedia.org/wikipedia/commons/c/c6/Tajikistan_wikivoyage_banner.jpg" }-->
### Authors: Sheharyar Ahmad, Federico Scoto, Ginevra Chelli, Arslaan Akhtar (Ca' Foscari University of Venice) <!--{ style="font-size:1.5rem;opacity:0.7;margin-top:1rem;" }-->

# 
*This story is based on results from the Science Hub Challenges organised and hosted by ESA's ESRIN Science Hub in September 2025. The challenge focused on monitoring properties of snow, glaciers and sea ice using the DeepESDL platform. It was developed by a team from University of Leeds.*

## Challenge
The Third Pole region, encompassing the Hindu Kush-Karakoram-Himalaya mountain ranges, contains the largest concentration of glaciers outside the polar regions. These glaciers are critical water sources for over two billion people in Asia. However, understanding glacier dynamics in this region is complicated by the **"Karakoram anomaly"**, a phenomenon where some glaciers show *stability or even slight growth* despite global warming trends. Monitoring glacier properties such as surface temperature, mass balance, and supraglacial lake formation is essential for water resource management, understanding climate impacts, and predicting flood risks. Traditional field measurements are challenging in these remote, high-altitude environments, making satellite remote sensing the primary tool for comprehensive glacier monitoring.

<div style="text-align: center;"> <img src="https://github.com/eurodatacube/eodash-assets/blob/main/stories/ScienceHub-Challenge-September-2025/Team-5/figure1_team5.png?raw=true" /> <p><b>Figure 1.</b> Conceptual diagram showing the key components of glacier monitoring: surface temperature variations, mass balance changes, and the formation of supraglacial lakes in response to climate forcing.</p> 

</div>

The challenge addresses a specific scientific question: **How can cooler summers coincide with higher water availability in the western Pamir region?** This paradox requires integrating multiple remote sensing datasets to understand the complex interaction between seasonal temperature patterns, glacier mass balance, and water storage dynamics.

## Objective

The objective of this study was to investigate the Kekesayi Glacier in the Pamir Mountains to understand its anomalous behavior under climate change. Specifically, the study aimed to:

- Analyze seasonal and annual Land Surface Temperature (LST) trends over the glacier from 2002 to 2018
- Detect and quantify changes in supraglacial lake area as a proxy for water availability
- Map moisture extent across the glacier surface to assess mass balance changes
- Integrate multi-sensor observations to explain the apparent paradox of warming winters, cooling summers, and increased water availability

This integrated approach enables a comprehensive understanding of glacier dynamics that goes beyond simple temperature or area change assessments.

## Use case <!--{ as="eox-map" mode="tour" }-->

### <!--{ layers='[{"type":"Group","properties":{"id":"OverlayGroup","title":"Overlay Layers"},"layers":[{"type":"Tile","properties":{"id":"overlay_bright;:;EPSG:3857","title":"Overlay labels"},"source":{"type":"XYZ","url":"//s2maps-tiles.eu/wmts/1.0.0/overlay_base_bright_3857/default/g/{z}/{y}/{x}.png","projection":"EPSG:3857"}}]},{"type":"Group","properties":{"id":"AnalysisGroup","title":"Data Layers"},"layers":[{"type":"Tile","properties":{"id":"MODIS_LST_Pamir;:;2d96aa0d-5170-4979-b00e-e9e3eb1d3308;:;MODIS_LST_Pamir;:;EPSG:3857","title":"MODIS Land Surface Temperature"},"source":{"type":"TileWMS","url":"https://services.sentinel-hub.com/ogc/wms/0635c213-17a1-48ee-aef7-9d1731695a54","projection":"EPSG:4326","tileGrid":{"tileSize":[512,512]},"params":{"LAYERS":["MODIS_LST"],"TILED":true,"TIME":"2015-09-01T00:00:00Z/2015-09-30T23:59:59Z"}}}]},{"type":"Group","properties":{"id":"BaseLayersGroup","title":"Base Layers"},"layers":[{"type":"Tile","properties":{"id":"cloudless-2024;:;EPSG:3857","title":"EOxCloudless 2024"},"source":{"type":"XYZ","url":"//s2maps-tiles.eu/wmts/1.0.0/s2cloudless-2024_3857/default/g/{z}/{y}/{x}.jpeg","projection":"EPSG:3857"}},{"type":"Tile","properties":{"id":"OSM;:;EPSG:3857","title":"OSM Background"},"source":{"type":"XYZ","url":"//s2maps-tiles.eu/wmts/1.0.0/osm_3857/default/g/{z}/{y}/{x}.jpeg","projection":"EPSG:3857"}},{"type":"Tile","properties":{"id":"terrain-light;:;EPSG:3857","title":"Terrain Light"},"source":{"type":"XYZ","url":"//s2maps-tiles.eu/wmts/1.0.0/terrain-light_3857/default/g/{z}/{y}/{x}.jpeg","projection":"EPSG:3857"}}]}]' zoom="10.5" center=[75.1,38.3] projection="" animationOptions={duration:500}}-->
#### Kekesayi Glacier, Pamir Mountains
The Kekesayi Glacier is the largest glacier in the Muztagh Ata area of the Pamir Mountains, located at the junction of several major Asian mountain systems. This heavily debris-covered glacier shows no significant frontal change despite regional climate warming, making it an ideal case study for understanding the Karakoram anomaly.

The Pamir Mountains, often called the "Roof of the World," are situated in Central Asia at the intersection of the Himalayas, Tian Shan, Karakoram, Kunlun, and Hindu Kush ranges. The region experiences marked interannual variability in temperature and precipitation, creating complex glacier dynamics.

<div style="display: flex; flex-direction: column; align-items: center; margin: 40px 0;">
    <img 
        src="https://github.com/eurodatacube/eodash-assets/blob/main/stories/ScienceHub-Challenge-September-2025/Team-5/Globe5_Pamir.png?raw=true" 
        style="max-width: 100%; width: 800px; height: auto;"
        alt="Kekesayi Glacier location"
    />
    <p style="text-align: center; font-size: 1.2em; margin-top: 10px;">
        <b>Figure 2.</b> Location of Kekesayi Glacier in the Pamir Mountains, Central Asia.
    </p>
</div>

## Data and Methods
#### Dataset
The study integrated three primary satellite datasets:

- **MODIS AQUA L3C Daily LST Data Cube (CCI)**: 1km spatial resolution, 2002–2018 time range, providing daytime Land Surface Temperature measurements
- **Sentinel-2 (S2L2A)**: 10m spatial resolution, three time points (2015, 2017, 2020), used for supraglacial lake detection as a proxy for water availability
- **Sentinel-1 GRD**: 10m spatial resolution, three time points (2015, 2017, 2020), used for moisture extent and mass balance assessment

Temperature trend analysis was supplemented with ECMWF ERA5 reanalysis data to provide climatic context, showing marked interannual variability with higher temperature anomalies in winter since the 1980s and slightly positive Surface Mass Balance (SMB).

#### Methodology workflow

**1. Land Surface Temperature Analysis (MODIS L3C)**
<div style="text-align: center;"> <img src="https://github.com/eurodatacube/eodash-assets/blob/main/stories/ScienceHub-Challenge-September-2025/Team-5/team5_method1.png?raw=true" /> <p><b>Figure 3.</b> Annual & Seasonal Mean LST ove Kekesayi Glacier.</p> </div>


**2. Supraglacial Lake Detection (Sentinel-2)**
<div style="text-align: center;"> <img src="https://github.com/eurodatacube/eodash-assets/blob/main/stories/ScienceHub-Challenge-September-2025/Team-5/team5_method2.png?raw=true" /> <p><b>Figure 4.</b> Glacier lake area change detection.</p> </div>


**3. Moisture Extent Mapping (Sentinel-1)**
<div style="text-align: center;"> <img src="https://github.com/eurodatacube/eodash-assets/blob/main/stories/ScienceHub-Challenge-September-2025/Team-5/team5_method3.png?raw=true" /> <p><b>Figure 5.</b> Moisture extent over the Kekesayi glacier.</p> </div>


## Results <!--{ as="eox-map" mode="tour" }-->

### <!--{ layers='[{"type":"Group","properties":{"id":"OverlayGroup","title":"Overlay Layers"},"layers":[{"type":"Tile","properties":{"id":"overlay_bright;:;EPSG:3857","title":"Overlay labels"},"source":{"type":"XYZ","url":"//s2maps-tiles.eu/wmts/1.0.0/overlay_base_bright_3857/default/g/{z}/{y}/{x}.png","projection":"EPSG:3857"}}]},{"type":"Group","properties":{"id":"AnalysisGroup","title":"Data Layers"},"layers":[{"type":"Tile","properties":{"id":"MODIS_LST_Pamir;:;2d96aa0d-5170-4979-b00e-e9e3eb1d3308;:;MODIS_LST_Pamir;:;EPSG:3857","title":"MODIS Land Surface Temperature"},"source":{"type":"TileWMS","url":"https://services.sentinel-hub.com/ogc/wms/0635c213-17a1-48ee-aef7-9d1731695a54","projection":"EPSG:4326","tileGrid":{"tileSize":[512,512]},"params":{"LAYERS":["MODIS_LST"],"TILED":true,"TIME":"2015-09-01T00:00:00Z/2015-09-30T23:59:59Z"}}}]},{"type":"Group","properties":{"id":"BaseLayersGroup","title":"Base Layers"},"layers":[{"type":"Tile","properties":{"id":"cloudless-2024;:;EPSG:3857","title":"EOxCloudless 2024"},"source":{"type":"XYZ","url":"//s2maps-tiles.eu/wmts/1.0.0/s2cloudless-2024_3857/default/g/{z}/{y}/{x}.jpeg","projection":"EPSG:3857"}},{"type":"Tile","properties":{"id":"OSM;:;EPSG:3857","title":"OSM Background"},"source":{"type":"XYZ","url":"//s2maps-tiles.eu/wmts/1.0.0/osm_3857/default/g/{z}/{y}/{x}.jpeg","projection":"EPSG:3857"}},{"type":"Tile","properties":{"id":"terrain-light;:;EPSG:3857","title":"Terrain Light"},"source":{"type":"XYZ","url":"//s2maps-tiles.eu/wmts/1.0.0/terrain-light_3857/default/g/{z}/{y}/{x}.jpeg","projection":"EPSG:3857"}}]}]' zoom="10.5" center=[75.1,38.3] projection="" animationOptions={duration:500}}-->
#### Seasonal Land Surface Temperature Patterns (MODIS L3C)
Maps of seasonal LST averaged over 2002-2018 reveal marked spatial variability between different areas of the Kekesayi Glacier, particularly between accumulation and ablation zones. As expected, during autumn and spring seasons, LST is higher in the ablation zone compared to the accumulation zone. 

**The most striking finding is the summer temperature pattern**: while warming would be expected, summer mean LST actually shows cooling in the ablation part of the glacier. This counterintuitive result is key to understanding the glacier's anomalous behavior.

<div style="display: flex; flex-direction: column; align-items: center; margin: 40px 0;">
    <img 
        src="https://github.com/eurodatacube/eodash-assets/blob/main/stories/ScienceHub-Challenge-September-2025/Team-5/results_team5.png?raw=true" 
        style="max-width: 100%; width: 800px; height: auto;"
        alt="Kekesayi Glacier location"
    />
    <p style="text-align: center; font-size: 1.2em; margin-top: 10px;">
        <b>Figure 6.</b> Seasonal Surface Temperature Averages.
    </p>
</div>

### <!--{ layers='[{"type":"Group","properties":{"id":"OverlayGroup","title":"Overlay Layers"},"layers":[{"type":"Tile","properties":{"id":"overlay_bright;:;EPSG:3857","title":"Overlay labels"},"source":{"type":"XYZ","url":"//s2maps-tiles.eu/wmts/1.0.0/overlay_base_bright_3857/default/g/{z}/{y}/{x}.png","projection":"EPSG:3857"}}]},{"type":"Group","properties":{"id":"AnalysisGroup","title":"Data Layers"},"layers":[{"type":"Tile","properties":{"id":"MODIS_LST_Pamir;:;2d96aa0d-5170-4979-b00e-e9e3eb1d3308;:;MODIS_LST_Pamir;:;EPSG:3857","title":"MODIS Land Surface Temperature"},"source":{"type":"TileWMS","url":"https://services.sentinel-hub.com/ogc/wms/0635c213-17a1-48ee-aef7-9d1731695a54","projection":"EPSG:4326","tileGrid":{"tileSize":[512,512]},"params":{"LAYERS":["MODIS_LST"],"TILED":true,"TIME":"2015-09-01T00:00:00Z/2015-09-30T23:59:59Z"}}}]},{"type":"Group","properties":{"id":"BaseLayersGroup","title":"Base Layers"},"layers":[{"type":"Tile","properties":{"id":"cloudless-2024;:;EPSG:3857","title":"EOxCloudless 2024"},"source":{"type":"XYZ","url":"//s2maps-tiles.eu/wmts/1.0.0/s2cloudless-2024_3857/default/g/{z}/{y}/{x}.jpeg","projection":"EPSG:3857"}},{"type":"Tile","properties":{"id":"OSM;:;EPSG:3857","title":"OSM Background"},"source":{"type":"XYZ","url":"//s2maps-tiles.eu/wmts/1.0.0/osm_3857/default/g/{z}/{y}/{x}.jpeg","projection":"EPSG:3857"}},{"type":"Tile","properties":{"id":"terrain-light;:;EPSG:3857","title":"Terrain Light"},"source":{"type":"XYZ","url":"//s2maps-tiles.eu/wmts/1.0.0/terrain-light_3857/default/g/{z}/{y}/{x}.jpeg","projection":"EPSG:3857"}}]}]' zoom="10.5" center=[75.1,38.3] projection="" animationOptions={duration:500}}-->
#### Temperature Trend Analysis
We analysed LST time series trend by quantifying pixels inside the ablation zone of glacier for linear trend estimation. A significant warming trend (R²= 0.56) is observed in winter, while autumn and spring show a cooling trend (R² 0.34 and 0.43, respectively). Notably during Summer a non significant cooling trend (R² = 0.05) can be also observed.

<div style="display: flex; flex-direction: column; align-items: center; margin: 40px 0;">
    <img 
        src="https://github.com/eurodatacube/eodash-assets/blob/main/stories/ScienceHub-Challenge-September-2025/Team-5/results2_team5.png?raw=true" 
        style="max-width: 100%; width: 800px; height: auto;"
        alt="Kekesayi Glacier location"
    />
    <p style="text-align: center; font-size: 1.2em; margin-top: 10px;">
        <b>Figure 7.</b> Seasonal Trend of Time Series.
    </p>
</div>



<!--no-nav=true -->  
## Supraglacial Lake Expansion (Sentinel-2)
Sentinel-2 analysis using NDWI (threshold ≥ 0.11) to detect water pixels revealed substantial growth in supraglacial lake area:

- **September 2015**: 0.16 km²
- **September 2020**: 0.406 km²

This represents a **154% increase** in lake area over five years, indicating enhanced water availability despite cooler summer temperatures. The expansion is linked to increased winter melting from warmer temperatures, with meltwater pooling in surface depressions.

<div style="display: flex; flex-direction: column; align-items: center; margin: 40px 0;">
    <img 
        src="https://github.com/eurodatacube/eodash-assets/blob/main/stories/ScienceHub-Challenge-September-2025/Team-5/results3_team5.png?raw=true" 
        style="max-width: 100%; width: 800px; height: auto;"
        alt="Supraglacial lake comparison"
    />
    <p style="text-align: center; font-size: 1.2em; margin-top: 10px;">
        <b>Figure 8.</b> Comparison of supraglacial lakes between September 2015 (left) and September 2020 (right), showing significant expansion in lake area.
    </p>
</div>

## Moisture Extent Evolution (Sentinel-1)
Sentinel-1 moisture mapping at the end of summer season shows a dramatic increase in surface moisture extent:

- **September 2015**: 2.54 km²
- **September 2017**: 3.34 km²
- **September 2020**: 8.2 km²

The moisture extent maps generally coincide with supraglacial lake locations but cover a larger area, indicating subsurface water storage and saturated debris cover. The **223% increase** from 2015 to 2020 demonstrates substantial changes in glacier hydrology.

<div style="display: flex; flex-direction: column; align-items: center; margin: 40px 0;">
    <img 
        src="https://github.com/eurodatacube/eodash-assets/blob/main/stories/ScienceHub-Challenge-September-2025/Team-5/results4_team5.png?raw=true" 
        style="max-width: 100%; width: 800px; height: auto;"
        alt="Moisture extent evolution"
    />
    <p style="text-align: center; font-size: 1.2em; margin-top: 10px;">
        <b>Figure 9.</b> Evolution of moisture extent across Kekesayi Glacier from 2015 to 2020, showing progressive increase in wet areas.
    </p>
</div>


## Conclusions

The study shows that some of the glaciers in the third pole do not respond uniformly to climate change, and shows slightly positive mass balance for the last decades.

The focused “ Kekesayi Glacier” is found to be experiencing warming winters with increasing meltwater which contributes in expanding supraglacial lakes, whereas the glacier experiences slightly cooler summer. These mixed signals highlight the importance of combining climatic analysis with morphometric proxies to capture
the full story.

The integration of multiple sensors (MODIS, Sentinel-1 & 2) and reanalysis products (ECMWF ERA5) can help in better understanding of evolving water balance of glaciers, and by extension, their role in regional hydrology and global climate change.

#### Future work
**Future perspectives** foresees to use newer remote sensing products such as Crystal/Sentinel 3 to measure snow depth, quantifying moisture content, differentiating debris from snow etc.

## <!--{ as="div" }--> Open Science

| **Name**                                                                                                                                       | **Type**            | **Agency / Provider**                     | **Description / Usage**                                                                                                                                                                                                                 |
| ---------------------------------------------------------------------------------------------------------------------------------------------- | ------------------- | ----------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **[MODIS Land Surface Temperature (LST)](https://lpdaac.usgs.gov/products/mod11a1v061/)**                                        | Dataset             | NASA/USGS               | MODIS AQUA L3C daily daytime LST at 1km resolution (2002-2018) from ESA CCI Cube. Used for analyzing seasonal and annual temperature trends over the glacier.                            |
| **[Sentinel-2 MSI](https://sentinel.esa.int/web/sentinel/missions/sentinel-2)**                                                                                       | Dataset | ESA (European Space Agency)                        | Multispectral optical imagery at 10m resolution for 2015, 2017, and 2020. Green and NIR bands used to calculate NDWI for supraglacial lake detection.                                     |
| **[Sentinel-1 SAR](https://sentinel.esa.int/web/sentinel/missions/sentinel-1)**                                          | Dataset     | ESA (European Space Agency)               | C-band radar Ground Range Detected (GRD) data at 10m resolution for 2015, 2017, and 2020. Used for moisture extent mapping and mass balance assessment.                                                     |
| **[ECMWF ERA5 Reanalysis](https://www.ecmwf.int/en/forecasts/datasets/reanalysis-datasets/era5)**                          | Dataset | ECMWF (European Centre for Medium-Range Weather Forecasts) | Climate reanalysis data providing temperature anomalies and precipitation context for interpreting glacier behavior.                                               |
| **[ESA CCI Data Cube](https://climate.esa.int/en/)**                          | Platform | ESA Climate Change Initiative | Earth System Data Lab (ESDL) infrastructure providing harmonized access to multiple climate data records including MODIS LST.                                               |

#### Code Repository
Access the processing scripts and analysis notebooks to reproduce the study workflow.
<iframe width="100%" height="600" src="https://github.com/science-hub-challenges/glacier-monitoring-pamir" frameborder="0"></iframe>

#### References
- Shean, D. E., Bhushan, S., Montesano, P., Rounce, D. R., Arendt, A., & Osmanoglu, B. (2020). A systematic, regional assessment of high mountain Asia glacier mass balance. *Frontiers in Earth Science*, 7, 363.

- Salerno, F., Guyennon, N., Yang, K. et al. (2023). Local cooling and drying induced by Himalayan glaciers under global warming. *Nature Geoscience*, 16, 1120–1127. [https://doi.org/10.1038/s41561-023-01331-y](https://doi.org/10.1038/s41561-023-01331-y)

- Hugonnet, R., McNabb, R., Berthier, E. et al. (2021). Accelerated global glacier mass loss in the early twenty-first century. *Nature*, 592, 726–731. [https://doi.org/10.1038/s41586-021-03436-z](https://doi.org/10.1038/s41586-021-03436-z)

- Wangchuk, S., and Bolch, T. (2020). Mapping of glacial lakes using Sentinel-1 and Sentinel-2 data and a random forest classifier: Strengths and challenges. *Science of Remote Sensing*, 2, 100008.

- Holzer, N., Vijay, S., Yao, T., Xu, B., Buchroithner, M., and Bolch, T. (2015). Four decades of glacier variations at Muztagh Ata (eastern Pamir): a multi-sensor study including Hexagon KH-9 and Pléiades data. *The Cryosphere*, 9, 2071–2088. [https://doi.org/10.5194/tc-9-2071-2015](https://doi.org/10.5194/tc-9-2071-2015)

## Contributors
**Students**: Sheharyar Ahmad, Federico Scoto, Ginevra Chelli, Arslaan Akhtar
