# Automated Swale and Trench Placement Tool

A tool for automating the placement of **swales** and **trenches** (Swench - Just a madeup name) using **UTM coordinates** and **machine learning** to optimize water management and prevent soil erosion. The tool processes UTM data, applies **KMeans clustering** for classification, and generates **contour maps** to visualize terrain elevation.

## Features

- Convert **Easting/Northing (UTM)** data to **Latitude/Longitude**.
- Classify land into **swale** and **trench** regions using **KMeans clustering**.
- Generate and display interactive **swale and trench placement maps**.
- Visualize **elevation contour maps** for terrain analysis.

## Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/your-username/your-repository.git
    cd your-repository
    ```

2. Install the required dependencies:

    ```bash
    pip install -r requirements.txt
    ```

## Usage

1. **Prepare the CSV File**: The CSV file should contain the following columns:
    - **Easting**
    - **Northing**
    - **Elevation**
    - **Distance (m)**
    - *Note: The last column (if any) will be automatically ignored.*

2. **Run the Streamlit App**:

    ```bash
    streamlit run app.py
    ```

3. **Upload the UTM Data**:
    - In the app, upload the CSV file containing **UTM coordinates**.
    - The tool will process the data and display both:
        - A **Swale and Trench Placement Map**.
        - An **Elevation Contour Map**.

## Project Structure

- **model.py**: Contains all the logic for processing the UTM data, converting to lat/lon, and applying machine learning.
- **app.py**: The main frontend file built with **Streamlit** to upload data and display results.
- **README.md**: This file, with project details.
- **requirements.txt**: Lists all the Python dependencies needed to run the project.

## Requirements

- Python 3.x
- Libraries:
    - `pandas`
    - `numpy`
    - `sklearn`
    - `pyproj`
    - `scipy`
    - `matplotlib`
    - `plotly`
    - `streamlit`

## How It Works

1. **Data Processing**: 
   - UTM coordinates (Easting/Northing) are converted to Latitude/Longitude.
   - The terrain is analyzed based on slope and elevation using **KMeans clustering**.

2. **Mapping**:
   - An interactive **map** is generated showing the recommended swale and trench placements.
   - A **contour map** is created to visualize the terrain's elevation.



