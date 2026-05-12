# CAC-by-channel
*Project Overview*

This project demonstrates an end-to-end data processing workflow for marketing performance analysis. The primary challenge lies in handling cumulative raw data exported from multiple ad platforms (TikTok, Meta, and Google).
Since the source data contains multiple daily snapshots per advertisement, the project focuses on data cleaning, state-of-the-day extraction using window functions, and calculating core performance marketing KPIs.

*Dataset Structure*

The core dataset marketing_ads_raw.csv contains the following fields:
| Field | Type | Description |
| :--- | :--- | :--- |
| **source** | STRING | Advertising channel: tiktok, meta, google |
| **campaign_id** | STRING | Unique ID of the marketing campaign |
| **adset_id** | STRING | Unique ID of the ad set |
| **ad_id** | STRING | Unique ID of the specific advertisement |
| **date** | DATE | Reporting date |
| **spend** | FLOAT | Cumulative spend in USD at the time of snapshot |
| **impressions** | INTEGER | Cumulative number of ad impressions |
| **clicks** | INTEGER | Cumulative number of clicks |
| **installs** | INTEGER | Cumulative number of app installs |
| **registrations**| INTEGER | Cumulative number of registrations |
| **timestamp** | TIMESTAMP | Exact time when the ETL loaded the data (UTC) |
