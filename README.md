# Visualising Australia's Climate

FIT2179 Data Visualisation 2 — Monash University, May 2026
Author: Ting-Han Wu

Live page: https://hans940324.github.io/australia-climate-viz/

## What is this

Ten Vega-Lite charts built from 20 years of daily weather observations across eight Australian capital cities (Sydney, Melbourne, Brisbane, Perth, Adelaide, Hobart, Darwin, Canberra), covering 2005-01-01 to 2025-04-30.

The page is organised into three parts:

1. **Temperature across Australia** — Charts 1 to 4
2. **Where the rain falls** — Charts 5 and 6
3. **Zooming into Melbourne** — Charts 7 to 10

## Folder structure

```
climate-viz/
├── index.html                          The full web page (all data inlined)
├── README.md                           This file
├── vega/                               10 Vega-Lite JSON specs (human-readable)
│   ├── chart_01_city_temp_compare.vl.json
│   ├── chart_02_slope.vl.json
│   ├── chart_03_choropleth.vl.json
│   ├── chart_04_city_boxplot.vl.json
│   ├── chart_05_rainfall_ranking.vl.json
│   ├── chart_06_rainfall_seasonal.vl.json
│   ├── chart_07_melb_summer.vl.json
│   ├── chart_08_melb_hot_days.vl.json
│   ├── chart_09_melb_calendar.vl.json
│   └── chart_10_melb_weather_donut.vl.json
├── data/                               All data referenced by the specs
│   ├── states_real.geojson             High-res Australian state boundaries
│   ├── state_temps_2024.csv            2024 annual mean temp per capital
│   ├── state_rainfall_season.csv       Summer-half vs winter-half rainfall per state
│   ├── city_tmean_compare.csv          2024 vs 20-yr-mean temp per city
│   ├── city_slope.csv                  2005-09 vs 2020-24 mean per city
│   ├── city_annual_rain.csv            Mean annual rainfall per city
│   ├── city_monthly_tmax.csv           Per-city monthly mean Tmax (20 yr × 12 mo)
│   ├── city_climate_summary.csv        One-row-per-city headline metrics
│   ├── melb_summer_max.csv             Melbourne DJF mean Tmax per year
│   ├── melb_hot_days.csv               Melbourne days ≥35°C and ≥40°C per year
│   ├── melb_2024_daily.csv             Melbourne daily Tmax for 2024
│   ├── melb_weather_types.csv          Melbourne 20-yr weather classification
│   ├── melbourne_daily.csv             Raw Open-Meteo daily for Melbourne
│   ├── sydney_daily.csv                Raw Open-Meteo daily for Sydney
│   ├── brisbane_daily.csv              etc.
│   ├── perth_daily.csv
│   ├── adelaide_daily.csv
│   ├── hobart_daily.csv
│   ├── darwin_daily.csv
│   └── canberra_daily.csv
└── png/                                Static PNG renders of each chart (preview)
    └── chart_01_…  through  chart_10_…
```

(An `_archive/` folder also exists with earlier-iteration files that were superseded; not used by the page.)

## Data sources

- **Daily weather**: [Open-Meteo Historical Weather API](https://open-meteo.com/en/docs/historical-weather-api) (ERA5 reanalysis at ~9 km grid). One CSV per capital city.
- **State boundaries**: [rowanhogan/australian-states](https://github.com/rowanhogan/australian-states) (GeoJSON).

## How to view

Open `index.html` directly in a browser. All data is inlined so no local server is needed.

## AI use

Vega-Lite specs, page styling, and caption drafting were assisted by Claude (Anthropic). Data sourcing, chart selection, narrative framing, and final wording were the author's.
