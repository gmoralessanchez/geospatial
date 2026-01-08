# MPCPro GeoCatalog Moon Images Viewer

A simple web application to view Chandrayaan-2 OHRC moon images from any Microsoft Planetary Computer Pro GeoCatalog collection.

## Features

- 🗺️ Interactive moon map using Leaflet with OpenPlanetary Moon basemap
- 🔗 Configurable GeoCatalog URL and Collection ID
- 📷 Browse STAC items from any GeoCatalog collection
- 🔍 View image footprints on the map
- 🖼️ Preview thumbnails in sidebar
- 🎯 Click to select, zoom, and overlay images on the map
- 🔐 Secure authentication with bearer token and automatic SAS token fetching

## Usage

### Running Locally

1. Simply open `index.html` in a web browser
2. Enter your GeoCatalog URL (e.g., `https://your-geocatalog.[region].geocatalog.spatio.azure.com`)
3. Enter the Collection ID (e.g., `chandrayaan2_ohrc_calibrated`)
4. Enter your bearer token
5. Click "Connect" to load the images

## Authentication

The application uses two-step authentication:

1. **Bearer Token** - Required to authenticate with the GeoCatalog STAC API
2. **SAS Token** - Automatically fetched from the `/sas/token/{collection_id}` endpoint to access collection assets (thumbnails, images)

Contact your GeoCatalog administrator to obtain bearer token credentials.

## Technical Details

- Uses projection compatible with OpenPlanetary Moon basemap tiles
- STAC API endpoints:
  - Items: `/stac/collections/{collection_id}/items`
  - SAS Token: `/sas/token/{collection_id}?api-version=2025-04-30-preview`
- Image overlays positioned using item geometry bounds

## Files

- `index.html` - Main web application (single file, no build required)
- `chandrayaan2_ohrc_calibrated.json` - Sample STAC collection metadata
- `items/` - Sample STAC item files
- `README.md` - This documentation

## License

The Chandrayaan-2 OHRC data is provided by ISRO. See the collection metadata for full licensing details. Sample data hosted by CloudFerro.
