# Lab 4: Interactive Web Mapping

## Project Description
This project contains two interactive choropleth web maps built using Mapbox GL JS:

1. **US Population Density Map** (`pop_density.html`) - A tutorial example showing state-level population densities across the United States
2. **Washington COVID-19 Map** (`index.html`) - An interactive map displaying COVID-19 case rates per 10,000 people across Washington State counties

## Maps

### 1. US Population Density Map
**File:** `pop_density.html`  
**Data Source:** `assets/stateData.geojson`  
**Description:** Displays population density (people per square mile) for all US states using a yellow-orange-red color scheme.

**Features:**
- 8 classification categories (0-9 to 1000+ people/sq.mi.)
- Hover interaction shows state name and density value
- Centered on continental United States

**Live Map:** [https://tinnam11.github.io/geog_328_web_mapping/pop_density.html]

### 2. Washington COVID-19 Case Rates Map
**File:** `index.html`  
**Data Source:** `assets/wa-covid-data-102521.geojson`  
**Description:** Visualizes cumulative COVID-19 case rates per 10,000 people across Washington State counties as of October 25, 2021.

**Features:**
- 8 classification categories (0-499 to 3500+ cases per 10k people)
- Orange sequential color scheme
- Hover interaction displays county name and case rate
- Focused on Washington State geography

**Live Map:** [https://tinnam11.github.io/geog_328_web_mapping/index.html]

## Data Sources

### US Population Density Data
- **File:** `stateData.geojson`
- **Attributes:** 
  - `name` - State name
  - `density` - Population density (people per square mile)

### Washington COVID-19 Data
- **File:** `wa-covid-data-102521.geojson`
- **Date:** October 25, 2021
- **Attributes:**
  - `name` - County name
  - `casePer10k` - Cumulative COVID-19 cases per 10,000 people
  - `deathPer10k` - Cumulative COVID-19 deaths per 10,000 people
  - `fullyVaxPer10k` - Fully vaccinated people per 10,000 people

**Original Data Sources:**
- COVID-19 case and death data: [The New York Times](https://github.com/nytimes/covid-19-data)
- COVID-19 vaccination data: [Washington State Department of Health](https://www.doh.wa.gov/Emergencies/COVID19/DataDashboard)
- Population estimates: [Washington State Office of Financial Management](https://ofm.wa.gov/)
- Cartographic boundaries: [U.S. Census Bureau](https://www.census.gov/geographies/mapping-files/time-series/geo/carto-boundary-file.html)

## Technologies Used
- **Mapbox GL JS** (v2.5.0) - Interactive web mapping library
- **HTML5** - Structure and content
- **CSS3** - Styling and layout
- **JavaScript (ES6+)** - Interactivity and data handling
- **GeoJSON** - Geographic data format

## Project Structure
```
lab04/
├── index.html                      # Washington COVID-19 map
├── pop_density.html                # US population density map
├── readme.md                       # Project documentation
└── assets/
    ├── stateData.geojson          # US state population data
    └── wa-covid-data-102521.geojson  # Washington COVID-19 data
```

## Features Implementation

### Choropleth Mapping
Both maps use the Mapbox GL JS `step` expression to create discrete color classifications based on data values. Colors are assigned using threshold values to create visually distinct categories.

### Interactive Hover
Maps implement event listeners that detect mouse movement over geographic features and dynamically update an information panel with:
- Feature name (state/county)
- Specific data value for that feature

### Legend
Dynamically generated legends use JavaScript to create color-coded entries that match the map's classification scheme, helping users interpret the data visualization.

## Acknowledgments
- Lab tutorial created by **Prof. Bo Zhao** (zhaobo@uw.edu)
- University of Washington Geography Department
- Mapbox for mapping platform and basemaps

## License
This project is created for part of GEOG 328 coursework.

---

