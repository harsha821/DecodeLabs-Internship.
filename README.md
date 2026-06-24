URBAN HEAT MITIGATION DECISION SUPPORT SYSTEM (ISRO)

┌─────────────────────────────────────────────────────────────────────┐
│      URBAN HEAT MITIGATION DECISION SUPPORT SYSTEM (ISRO)          │
├─────────────────────────────────────────────────────────────────────┤
│                                                                     │
│   ┌─────────────────┐              ┌──────────────────────┐         │
│   │   User Portal   │              │   Admin Dashboard    │         │
│   │   (React Web)   │              │   (React Web)        │         │
│   └────────┬────────┘              └──────────┬───────────┘         │
│            │                                  │                     │
│   ┌────────▼──────────────────────────────────▼────────────┐        │
│   │              FastAPI Backend Server                    │        │
│   │ Auth · JWT · GIS APIs · AOI APIs · Forecast APIs      │        │
│   └──────┬──────────┬──────────┬──────────┬───────────────┘        │
│          │          │          │          │                        │
│   ┌──────▼──┐ ┌─────▼────┐ ┌──▼──────┐ ┌─▼────────────┐           │
│   │ AOI     │ │ Heat Map │ │Forecast │ │ Scenario     │           │
│   │ Service │ │ Service  │ │ Service │ │ Simulator    │           │
│   └────┬────┘ └────┬─────┘ └──┬──────┘ └─────┬────────┘           │
│        │           │          │              │                    │
│        └───────────┴──────────┴──────────────┘                    │
│                            │                                      │
│               ┌────────────▼─────────────┐                        │
│               │ PostgreSQL + PostGIS     │                        │
│               │ AOI · Heat Maps          │                        │
│               │ Forecasts · Suitability  │                        │
│               │ Scenario Results         │                        │
│               └──────────────────────────┘                        │
│                                                                     │
│   ┌───────────────────────────────────────────────────────────┐     │
│   │               AI/ML Service (FastAPI)                    │     │
│   │ Current Heat Prediction  → XGBoost                       │     │
│   │ Future Heat Forecasting → LSTM                           │     │
│   │ Heat Driver Analysis   → SHAP                            │     │
│   │ Physics-Informed Validation                              │     │
│   └───────────────────────────────────────────────────────────┘     │
│                                                                     │
│   ┌───────────────────────────────────────────────────────────┐     │
│   │ Optimization & Recommendation Engine                     │     │
│   │ Cooling Suitability Analysis                             │     │
│   │ Multi-Objective Optimization                             │     │
│   │ Recommendation Engine                                    │     │
│   │ Scenario Simulator Service                               │     │
│   └───────────────────────────────────────────────────────────┘     │
└─────────────────────────────────────────────────────────────────────┘

EXTERNAL INTEGRATIONS
─────────────────────────────────────────────────────────────────────

Satellite Data
Landsat 8/9                 ──► Data Collection Service
Sentinel-2                  ──► Data Collection Service

Weather Data
IMD Weather API             ──► Weather Service
Temperature                 ──► Weather Service
Humidity                    ──► Weather Service
Wind Speed                  ──► Weather Service

Geospatial Data
DEM Elevation Data          ──► Terrain Service
LULC Data                   ──► Land Cover Service

Feature Extraction
NDVI                        ──► Feature Extraction Service
NDBI                        ──► Feature Extraction Service
NDWI                        ──► Feature Extraction Service
LST                         ──► Feature Extraction Service

AI/ML PROCESSING
─────────────────────────────────────────────────────────────────────

XGBoost
├── Current City Heat Map
├── Current Area Heat Map
└── Area Heat Hotspots

LSTM
├── Day 1–7 City Forecast
└── Day 1–7 Area Forecast

SHAP
└── Heat Driver Analysis

OPTIMIZATION ENGINE OUTPUTS
─────────────────────────────────────────────────────────────────────

Cooling Suitability Analysis
└── Cooling Suitability Maps

Multi-Objective Optimization
└── Priority Intervention Areas

Recommendation Engine
└── Recommended Cooling Intervention Plan

Scenario Simulator Service
├── Post-Mitigation Forecasts
├── Cooling Strategy Impact Analysis
└── Before vs After Comparison
