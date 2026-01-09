# STAC Sample Files for Microsoft Planetary Computer Pro GeoCatalog

This folder contains sample STAC (SpatioTemporal Asset Catalog) files that can be used as templates for creating collections and items for this project in a [Microsoft Planetary Computer Pro GeoCatalog](https://azure.microsoft.com/en-us/products/planetary-computer-pro).

## Overview

These samples are based on the **Chandrayaan-2 Orbiter High Resolution Camera (OHRC) Calibrated Images** collection from [CloudFerro&#39;s Beyond Earth STAC browser](https://browser.beyondearth.stac.cloudferro.com/collections/chandrayaan2_ohrc_calibrated).

### Source Collection Information

- **Mission**: Chandrayaan-2 (ISRO)
- **Instrument**: Orbiter High Resolution Camera (OHRC)
- **Data Type**: Calibrated panchromatic images of the Moon
- **Resolution**: 0.26m spatial resolution
- **Processing Level**: L2 (Calibrated)

## Files Structure

```
stac_sample/
├── README.md                                    # This file
├── chandrayaan2_ohrc_calibrated.json           # Sample STAC Collection definition
└── items/
    └── ch2_ohr_ncp_20240425t1012478407_d_img_d18.json  # Sample STAC Item
```

### Collection File

`chandrayaan2_ohrc_calibrated.json` - A STAC Collection definition with the required modifications to create the STAC collection in MPC Pro that includes:

- Collection metadata (id, title, description)
- Spatial and temporal extents
- Provider information (ISRO, CloudFerro)
- Keywords and scientific references
- Summary information about the dataset

### Item File

`items/ch2_ohr_ncp_20240425t1012478407_d_img_d18.json` - A STAC Item definition with the required modifications to create an item an ingest data that includes:

- Item metadata (id, geometry, bbox)
- Assets (thumbnail, data files)
- Properties (datetime, platform, instruments)
- Projection information (proj:code, proj:shape)
- Raster band information

## Usage with Microsoft Planetary Computer Pro

These samples can be used as templates when setting up your own geospatial data catalog in Microsoft Planetary Computer Pro GeoCatalog.

### Getting Started

1. **Deploy a GeoCatalog resource** in your Azure subscription
2. **Create a STAC Collection** using the collection JSON as a template
3. **Add STAC Items** to your collection using the item JSON as a template
4. **Configure visualization** settings for your collection

## Microsoft Planetary Computer Pro Documentation

### Key Documentation Links

| Topic                       | Description                                  | Link                                                                                                          |
| --------------------------- | -------------------------------------------- | ------------------------------------------------------------------------------------------------------------- |
| **Overview**          | What is Microsoft Planetary Computer Pro?    | [Overview](https://learn.microsoft.com/en-us/azure/planetary-computer/microsoft-planetary-computer-pro-overview) |
| **Get Started**       | Getting started guide                        | [Get Started](https://learn.microsoft.com/en-us/azure/planetary-computer/get-started-planetary-computer)         |
| **Deploy GeoCatalog** | Deploy a GeoCatalog resource                 | [Deploy Guide](https://learn.microsoft.com/en-us/azure/planetary-computer/deploy-geocatalog-resource)            |
| **STAC Overview**     | Understanding STAC in Planetary Computer Pro | [STAC Overview](https://learn.microsoft.com/en-us/azure/planetary-computer/stac-overview)                        |

### Creating Collections

| Topic                             | Description                                | Link                                                                                                           |
| --------------------------------- | ------------------------------------------ | -------------------------------------------------------------------------------------------------------------- |
| **Create Collection (Web)** | Create a STAC collection via Web Interface | [Web Interface Guide](https://learn.microsoft.com/en-us/azure/planetary-computer/create-collection-web-interface) |
| **Create Collection (API)** | Create a STAC collection via API           | [API Guide](https://learn.microsoft.com/en-us/azure/planetary-computer/create-stac-collection)                    |

### Adding Items and Ingesting Data

| Topic                            | Description                         | Link                                                                                                    |
| -------------------------------- | ----------------------------------- | ------------------------------------------------------------------------------------------------------- |
| **Ingestion Overview**     | Understanding data ingestion        | [Ingestion Overview](https://learn.microsoft.com/en-us/azure/planetary-computer/ingestion-overview)        |
| **Create STAC Item**       | How to create a STAC item           | [Create Item Guide](https://learn.microsoft.com/en-us/azure/planetary-computer/create-stac-item)           |
| **Add Item to Collection** | Add a STAC item to a collection     | [Add Item Guide](https://learn.microsoft.com/en-us/azure/planetary-computer/add-stac-item-to-collection)   |
| **Ingest via Web**         | Ingest data using the Web Interface | [Web Ingestion Guide](https://learn.microsoft.com/en-us/azure/planetary-computer/ingest-via-web-interface) |

### Visualization and Configuration

| Topic                              | Description                             | Link                                                                                                              |
| ---------------------------------- | --------------------------------------- | ----------------------------------------------------------------------------------------------------------------- |
| **Collection Configuration** | Configure collections for visualization | [Configuration Guide](https://learn.microsoft.com/en-us/azure/planetary-computer/configure-collection-web-interface) |
| **Use the Explorer**         | Explore and visualize your data         | [Explorer Guide](https://learn.microsoft.com/en-us/azure/planetary-computer/use-explorer)                            |

### API Reference

| Topic                   | Description                                           | Link                                                                                 |
| ----------------------- | ----------------------------------------------------- | ------------------------------------------------------------------------------------ |
| **API Tutorial**  | Complete API tutorial for ingestion and visualization | [API Tutorial](https://learn.microsoft.com/en-us/azure/planetary-computer/api-tutorial) |
| **API Reference** | Full API reference guide                              | [API Reference](https://learn.microsoft.com/en-us/rest/api/planetarycomputer)           |

## Additional Resources

- [Microsoft Planetary Computer Pro Product Page](https://azure.microsoft.com/en-us/products/planetary-computer-pro)
- [STAC Specification](https://stacspec.org/)
- [CloudFerro Beyond Earth Browser](https://browser.beyondearth.stac.cloudferro.com/)

## Notes

- The sample files use placeholder URLs (`https://avalidgeocatalog.geocatalog.spatio.azure.com`) that should be replaced with your actual GeoCatalog endpoint
- Review the [Supported Data Types](https://learn.microsoft.com/en-us/azure/planetary-computer/supported-data-types) documentation for compatible file formats
