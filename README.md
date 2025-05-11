# Tabrifics Stockist Map
Shopify Liquid Element snippet to display an interactive map of Tabrifics stockist locations. The map fetches stockist data from a publicly shared Google Sheet, allowing for easy updating of stockist locations.

<img width="1453" alt="Screenshot 2025-04-14 at 21 39 08" src="https://github.com/user-attachments/assets/e000591a-5e81-4afd-a8ed-389acf956b39" />

## Features
- Interactive map with markers for each stockist location
- Real-time data fetched from a Google Sheet
- Easy integration into Shopify with Liquid
- Can use custom map tiles.

## Setup
Follow these steps to setup the stockist map on your Shopify store.

### 1. Prepare Google Sheet
Create a Google Sheet with the following columns:
- name
- address
- lat
- lng
- url

Then publish the sheet to the web by going to File > Share > Publish to web

Choose Sheet1 instead of entire document, and choose Comma Separated Values (.csv) as the format.

Copy the link given to you after publishing.

### 2. Setup Liquid
Copy contents of `example.html` into a new liquid element in Shopify. 

Replace YOURURLHERE in the `publicSpreadseetUrl` variable with the URL copied from your published Google Sheet.

### 3. Custom Map Tiles
`stockists.html` uses MapTiler tiles, if you want to use this then you just need to replace YOURKEYHERE with your MapTiler API key in the `maptilerAPIkey` variable.

[Read more about using custom map tiles with MapTiler](https://docs.maptiler.com/leaflet/examples/raster-tiles-in-leaflet-js/)

## Data Fetching

The stockist data is fetched from the Google Sheet using the [PapaParse library](https://github.com/mholt/PapaParse). The method to fetch the Google Sheets data was used from this [Tabletop.js](https://github.com/jsoma/tabletop) page.

## Maintaining Stockist Data

To update stockist data, simply update the Google Sheet. The map will automatically update with the new data without any need for manual updates in Shopify.
