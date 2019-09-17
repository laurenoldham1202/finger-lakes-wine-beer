# Boozin' in the Finger Lakes

## About the Project

This project was completed as a final project for MAP-674 (Spatial Analysis) as part of the New Maps Plus MSc in Digital Mapping. Included are a Jupyter Notebook and dynamic web map of breweries and distilleries within a half mile of a winery in the Finger Lakes region of upstate New York. Map and notebook authored by Lauren Oldham, September 2019.

### Data
#### New York Breweries and Wineries
Wineries, Breweries, and Distilleries data provided by https://data.ny.gov/.

Based on Liquor Authority Quarterly List of Active Licenses

Liquor Authority quarterly list of all active licensees in NYS filtered by Winery and Brewery specific License Types.

https://data.ny.gov/Economic-Development/Wineries-Breweries-and-Distilleries-Map/c2hv-vmqn

#### Shapefiles
United States state and county shapefiles provided by GADM.

https://gadm.org/download_country_v3.html

## Run the Project
1. Clone repository into local directory
2. Navigate to new repository in terminal
3. Recreate Conda virtual environment
    - `conda env create -f environment.yml`
4. Activate virtual environment
    - `conda activate fingerlakes`
5. Install local server (I use `http-server` and npm as my package manager, generally)
    - In terminal, run `http-server --cors=*` from repository
6. You should now be able to view the map through your local server (check terminal output for server)
    - Navigate to `maps/` in terminal OR localhost
7. To run the notebook, run `jupyter notebook` and navigate to `notebooks/ny_beer_wine.ipynb`
    - OR navigate to `notebooks/` and run `jupyter notebook ny_beer_wine.ipynb` directly
    
    
## Future Considerations and Updates

As is, the current map isn't very visually interesting; a bit more data manipulation, geoprocessing, and styling would improve it. Some future improvement considerations are:

1. Increase buffer range or make dynamic in the map with a slider range
2. Dissolve or group establishments with multiple types (some establishments are both wineries and distilleries and are plotted as separate entities on top of each other, masking whichever is on bottom)
3. Split the winery and brewery/distillery datasets into separate layers and include a layer control to toggle them
4. Add additional datasets (population? alcoholism rates? drunk driving statistics? etc.)
5. Add establishment website data to JSON to include in mouseover label
6. Perform nearest neighbor analysis to include in mouseover label ('X establishment is Ydistance from Z establishment, its closest neighbor')
