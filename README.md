# Boozin' in the Finger Lakes

## About the Project

This project was completed as a final project for MAP-674 (Spatial Analysis) as part of the New Maps Plus MSc in Digital Mapping. Included are a Jupyter Notebook and dynamic web map of breweries and distilleries within a half mile of a winery in the Finger Lakes region of upstate New York.

## Run the Project
1. Clone repository into local directory
2. Navigate to new repository in terminal
3. Recreate Conda virtual environment
    - `conda env create -f environment.yml`
4. Activate virtual environment
    - `conda activate fingerlakes`
5. Install local server (I use `http-server` and npm as my package manager, generally)
    1. In terminal, run `http-server --cors=*` from repository
6. You should now be able to view the map through your local server (check terminal output for server)
    1. Navigate to `maps/` in terminal OR localhost
7. To run the notebook, run `jupyter notebook` and navigate to `notebooks/ny_beer_wine.ipynb`
    1. OR navigate to `notebooks/` and run `jupyter notebook ny_beer_wine.ipynb` directly