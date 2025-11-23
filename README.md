# Bike Patterns in Boston - Lab 7

An interactive geospatial visualization of bike traffic patterns in the Boston area using Mapbox and D3.js.

## Setup Instructions

### 1. Get Your Mapbox Access Token

1. Go to [Mapbox](https://www.mapbox.com/) and create an account using your UCSD email
2. After signing up and verifying your email, go to your [Account Dashboard](https://account.mapbox.com/)
3. Copy your default public access token (it starts with `pk.`)
4. Open `map.js` and replace `YOUR_ACCESS_TOKEN_HERE` on line 7 with your actual token:

```javascript
mapboxgl.accessToken = 'pk.your_actual_mapbox_access_token_here';
```

### 2. Test Locally

You can test the project locally by opening `index.html` in a web browser. However, for best results, use a local server:

```bash
# Using Python 3
python -m http.server 8000

# Using Python 2
python -m SimpleHTTPServer 8000

# Using Node.js (if you have http-server installed)
npx http-server
```

Then open `http://localhost:8000` in your browser.

### 3. Deploy to GitHub Pages

1. Create a new repository on GitHub (e.g., `bikewatching`)
2. Push your code to the repository
3. Go to Settings > Pages in your GitHub repository
4. Select the branch (usually `main`) and folder (`/root`)
5. Your site will be available at `https://yourusername.github.io/repository-name/`

## Features

- **Interactive Map**: Pan and zoom around Boston area
- **Bike Lanes**: Visualized green lines showing bike lanes in Boston and Cambridge
- **Station Markers**: Circles representing BlueBike stations
- **Traffic Visualization**: 
  - Circle size represents total traffic volume
  - Circle color represents traffic flow (more departures = blue, balanced = orange-blue mix, more arrivals = orange)
- **Time Filter**: Slider to filter traffic by time of day
- **Tooltips**: Hover over stations to see exact traffic numbers

## Files Structure

- `index.html` - Main HTML file
- `map.js` - Main JavaScript file with Mapbox and D3 logic
- `global.css` - Global styles
- `map.css` - Map-specific styles
- `assets/favicon.svg` - Bike emoji favicon

## Data Sources

- Bike lanes: Boston Open Data and Cambridge GIS
- Station data: BlueBikes (via DSC 106 lab data)
- Traffic data: BlueBikes March 2024 (via DSC 106 lab data)

