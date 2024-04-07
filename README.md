# Tabrifics Stockist Map
Shopify Liquid Element snippet to display interactive map of Tabrifics stockists

Data is fetched from a Google Sheet published to the web containing the stockist data.

Used [PapaParse and instructions from Tabletop](https://github.com/jsoma/tabletop) to fetch data from Google Sheets.

### Setup
Just copy paste the contents of example.html into a liquid element, and add your Google Sheet public URL to the `publicSpreadsheetUrl` variable.

stockists.html uses MapTiler tiles, if you want to use this then you just need to replace YOURKEYHERE with your MapTiler API key in the `maptilerAPIkey` variable.

### Public Google Sheet
The Google Sheet should have the following columns:
- name
- address
- lat
- lng
- url

Then publish the sheet to the web by going to File > Share > Publish to web

Then choose Sheet1 instead of entire document, and choose Comma Separated Values (.csv) as the format.

Copy this link and paste it between the ""s in the `publicSpreadsheetUrl` variable in the liquid element.

To keep stockist list up to date, just add or remove entries to the linked Google Sheet.