# ArcGISPro MapSeries PNGExport
This script exports multiple maps based on a spatial map series from an ArcGIS project layout. It iterates through the map series and exports each map as a PNG image.

## 1. Prerequisites

- [ArcGIS Desktop](https://www.esri.com/en-us/arcgis/products/arcgis-desktop/overview)
- [Python](https://www.python.org/) (usually comes with ArcGIS installation)

## 2. Important Notes

- <b>Warning!!!</b> Save your project before running the code.
- This code **do not support bookmark map series**.
- This code assumes that the ArcGIS project is currently open and active in the ArcGIS Desktop application.
- Make sure you have the necessary permissions to access the specified export location.

## 3. Step by Step Guide

Follow these steps to execute the code (Demonstration is provided in this [YouTube Tutorial](https://www.youtube.com/watch?v=IgkXu33A6YI)).

1. Open an ArcGISPro project (containing the data and the layout that needed to be exported).

3. Create a **spatial map series** in the layout that needs to be exported. <br> Check out this [YouTube Tutorial](https://www.youtube.com/watch?v=MNG381rli24) to learn how to create map series.

5. Open a Notebook within ArcGISPro. (Insert --> New Notebook)

6. Copy and paste the [script](ArcGISPro_MapSeries_PNGExport) into a cell in the Notebook.

7. Run the script. The code will prompt you to enter input variables.
   
9. Enter the input variables. Press 'Enter' after entering each input.
   
11. Wait for the code to execute. Then check the output folder.

| Variable name | Description | Example | 
| -------- | -------- | -------- |
| `layout_name` | Name of the Layout (which contain the spatial map series) | Layout 1|
| `Folder_location` | Output folder location for the exported maps | C:\GIS\Test1|
| `File_prefix` | File name prefix for exported maps (Base name) | Map_|
| `File_suffix` | Export with page name (yes/no) | yes for page name <br> no for page number|

## 4. Code Explanation

The script performs the following steps:

1. It imports required modules.

2. It opens the current ArcGIS project using the `ArcGISProject` class.

3. The specified layout name (`layout_name`) is used to obtain a reference to the desired layout within the project.

4. The script checks if the layout contains a spatial map series (`MapSeries`).

5. The map series is retrieved from the layout.

6. The script iterates through each page in the map series and export as PNG images.

## 5. Features

This code is adopted from  [ArcGISPro documentation](https://pro.arcgis.com/en/pro-app/latest/arcpy/mapping/mapseries-class.htm) and has been enhanced with additional capabilities.
- The `layout_name` parameter allows to specify the layout you want to export.
- The `Folder_location` parameter allows to change the export Location.
- Both `File_prefix` and `File_suffix` parameters allows to change the output file name.


## 6. License

This script is provided under the [MIT License](LICENSE).
