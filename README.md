# Lithium Supply Chain Plausibility Assessment

A geospatial research pipeline for assessing the transparency and reliability of the global lithium supply chain using real open data, spatial analysis, remote sensing, and deep learning.

**Department of Geoinformatics — Z_GIS**
**Paris Lodron University of Salzburg**

---

## What this project does

This case study traces 5 verified lithium supply chain paths from mine to battery manufacturer and runs three plausibility checks on each path using real publicly available data.

The three plausibility rules are:
- Rule 1 — Geological consistency: Does the geology at the declared mine location actually support lithium extraction?
- Rule 2 — Geographic feasibility: Is the declared trade route between nodes physically and logistically realistic?
- Rule 3 — Network structure completeness: Is every tier of the supply chain present from mine to end user?

---

## Research question

When a company declares a lithium supply chain path — can we verify it is geologically consistent, geographically feasible, and structurally complete using geospatial data, remote sensing, and deep learning?

---

## Supply chain paths studied

| Path | Mine | Country | Processing | Country | Manufacturer | Country |
|---|---|---|---|---|---|---|
| 1 | Greenbushes | Australia | Kwinana Plant | Australia | CATL | China |
| 2 | Salar de Atacama | Chile | La Negra Refinery | Chile | LG Chem | Korea |
| 3 | Wodgina | Australia | Kemerton Plant | Australia | Panasonic | Japan |
| 4 | Qinghai Lake Brine | China | Ganfeng Refinery | China | BYD | China |
| 5 | Pilgangoora | Australia | Chinese Refineries | China | Samsung SDI | Korea |

---

## Data sources

All links below are confirmed working and were used to collect the actual data for this project.

| # | Dataset | Source | Format | Confirmed Link |
|---|---|---|---|---|
| 1 | USGS MRDS geological records | USGS | CSV + Shapefile | https://mrdata.usgs.gov/mrds/find-mrds-graded.php |
| 2 | Mineral Commodity Summaries 2026 | USGS | PDF | https://pubs.usgs.gov/periodicals/mcs2026/mcs2026-lithium.pdf |
| 3 | Australian Critical Minerals Map 2025 | Geoscience Australia | PDF | https://d28rz98at9flks.cloudfront.net/150802/150802_00_0.pdf |
| 4 | Australia Identified Mineral Resources 2024 | Geoscience Australia | PDF | https://minexcrc.com.au/wp-content/uploads/2025/03/2024-AIMR-100325.pdf |
| 5 | CATL ESG Report 2025 | CATL | PDF | https://www.catl.com/en/uploads/1/file/public/202603/20260331135628_dciihbv1qr.pdf |
| 6 | Ganfeng Annual Report 2024 | Ganfeng Lithium | PDF | https://www.ganfenglithium.com/ir1_en.html |
| 7 | LG Chem Sustainability Report 2024 | LG Chem | PDF | https://www.lgchem.com/upload/file/sustainability/2024_LGChem_Sustainability_Report_ENG.pdf |
| 8 | Samsung SDI Sustainability Report 2025 | Samsung SDI | PDF | https://www.samsungsdi.com/upload/download/sustainable-management/Samsung_SDI_Sustainability_Report_2025_EN.pdf |
| 9 | IGO Annual Report 2024 | IGO Limited | PDF | https://www.igo.com.au/site/pdf/db560842-6410-48a5-a911-3e45093eb372/2024-Annual-Report.pdf |
| 10 | SQM Annual Report 2024 | SQM | PDF | https://ir.sqm.com/system/files-encrypted/nasdaq_kms/assets/2025/06/12/2-37-42/MEMORIA%20SQM%202024_eng.pdf |
| 11 | Albemarle Annual Report 2025 | Albemarle | PDF | https://investors.albemarle.com/financial-information/annual-reports |
| 12 | Pilbara Minerals Annual Report 2024 | Pilbara Minerals | PDF | https://minedocs.com/27/Pilbara-Minerals-AR-06302024.pdf |
| 13 | UN Comtrade lithium trade flows | United Nations | CSV | https://comtradeplus.un.org |
| 14 | Sentinel-2 satellite imagery | Copernicus via Google Earth Engine | API | https://earthengine.google.com |
| 15 | Open Supply Hub facility data | Open Supply Hub | CSV | https://opensupplyhub.org |

---

## Important note on Open Supply Hub

A search of Open Supply Hub across all mining and material production sectors returned no results for Tianqi Lithium, CATL, Ganfeng, or any other lithium supply chain company. This is itself a key finding of this study — upstream lithium supply chains remain entirely absent from global facility transparency platforms that cover apparel and textile supply chains extensively.

---

## Accounts required

The following platforms require a free account before downloading data:

| Platform | Purpose | Registration |
|---|---|---|
| UN Comtrade | Trade flow data | https://comtradeplus.un.org |
| Open Supply Hub | Facility data | https://opensupplyhub.org |
| Google Earth Engine | Satellite imagery | https://earthengine.google.com |

---

## Technology stack

| Tool | Purpose |
|---|---|
| Python 3.10 | Primary programming language |
| Google Colab | Development and execution environment |
| Google Earth Engine API | Sentinel-2 satellite imagery access |
| pandas | Data loading and cleaning |
| geopandas | Spatial data processing |
| shapely | Geometric operations |
| folium | Interactive map visualization |
| rasterio | Satellite imagery processing |
| networkx | Knowledge graph construction |
| pyvis | Interactive graph visualization |
| PyTorch | Deep learning framework |
| torchvision | Pre-trained CNN models |
| torch-geometric | Graph Neural Network |
| scikit-learn | Traditional ML and preprocessing |

---

## Notebook structure

The entire pipeline runs in one single Google Colab notebook divided into 8 sections:

| Section | What it does |
|---|---|
| 1 | Setup and library installation |
| 2 | Google Drive connection and data loading |
| 3 | Data exploration and cleaning |
| 4 | Knowledge graph construction and Graph Neural Network |
| 5 | Spatial analysis and trade route mapping |
| 6 | Remote sensing and CNN land cover classification |
| 7 | Autoencoder anomaly detection |
| 8 | Final plausibility report and results |

---

## How to run this project

Step 1 — Create free accounts at the three platforms listed above

Step 2 — Download all data files from the confirmed links in the data sources table

Step 3 — Create a folder in your Google Drive named: lithium-supply-chain-plausibility

Step 4 — Inside that folder create these subfolders:
01_geological
02_supply_chain
03_trade_flows
04_remote_sensing

Step 5 — Save each downloaded file into the correct subfolder

Step 6 — Open the notebook in Google Colab using the link below

Step 7 — Run all cells from top to bottom

---

## References
- IEA (2025). World Energy Outlook 2025. International Energy Agency.
- UNCTAD (2026). Critical Minerals, Critical Decisions. United Nations.
- USGS (2026). Mineral Commodity Summaries 2026. U.S. Geological Survey.
- Cerai, A.P. (2024). Geography of Control: Lithium Supply Chain. Mineral Economics.
- IGO Limited (2024). Annual Report 2024.
- SQM (2024). Annual Report 2024.
- Albemarle Corporation (2025). Annual Report 2025.
- Pilbara Minerals (2024). Annual Report 2024.
- CATL (2025). ESG Report 2025.
- Ganfeng Lithium (2024). Annual Report 2024.
- LG Chem (2024). Sustainability Report 2024.
- Samsung SDI (2025). Sustainability Report 2025.
