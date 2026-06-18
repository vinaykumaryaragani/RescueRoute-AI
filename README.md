# RescueRoute AI – Smart Emergency Response and Navigation System

AI-powered emergency response system that enables real-time disaster monitoring and safe route optimization for efficient rescue operations.

## Overview

RescueRoute AI is a FastAPI + React-based disaster navigation platform that combines real-time disaster feeds, map-based road risk analysis, and safety-aware route optimization to support informed decision-making during emergencies.

## Key Features

* Integrated live disaster data from ReliefWeb, NASA FIRMS, and OpenWeather into a unified backend format exposed through `/disasters` and `/api/disasters`.
* Implemented timeline filtering with URL-synced frontend state and backend `from` / `to` date filtering.
* Visualized disaster events on interactive maps using clustered markers, type-based colors, and detailed information panels.
* Developed a rule-based road status engine to classify roads as `blocked`, `risky`, or `safe` based on nearby disaster impact zones.
* Displayed blocked roads directly on the map using GeoJSON overlays and custom styling.
* Enhanced routing by avoiding blocked roads and assigning penalties to risky roads for safer navigation.
* Enabled route comparison mode to display both the fastest and the safest routes simultaneously.
* Implemented AI-generated disaster summaries with local fallback summaries for improved reliability.
* Added browser geolocation and destination search using Nominatim autocomplete.
* Incorporated confidence indicators and warning banners to provide users with better situational awareness.

## Tech Stack

### Frontend

* React
* Vite
* Zustand
* Mapbox GL

### Backend

* FastAPI

### External APIs and Services

* ReliefWeb
* NASA FIRMS
* OpenWeather
* Overpass
* OSRM
* Nominatim

## Setup

### Backend

```bash
cd backend
pip install -r requirements.txt
python main.py
```

The API runs at `http://localhost:8000`.

### Frontend

```bash
cd frontend
npm install
npm run dev
```

The application runs at `http://localhost:5173`.

## Required Environment Variables

### Backend

* `RELIEFWEB_APPNAME`
* `NASA_API_KEY`
* `OPENWEATHER_API_KEY`

### Frontend

* `VITE_MAPBOX_TOKEN`
* `VITE_API_BASE` (optional)

## Verification

* Backend syntax check: `python -m compileall .`
* Frontend linting: `npm run lint`
* Production build: `npm run build`

## Author

**Yaragani VinayKumar**
