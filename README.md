# Electric Vehicle (EV) Adoption Dashboard

This project develops an interactive Dash application using Plotly and Python to visualize and analyze Electric Vehicle (EV) adoption trends across various U.S. states. The dashboard provides insights into EV registrations, charging infrastructure, and the relationship between EV adoption and socioeconomic factors.

## Project Overview

The primary goal of this application is to provide a user-friendly interface for exploring data related to EV adoption. The application is built to be deployment-ready and includes all necessary materials to run it in a local environment.

## Features

* **Interactive Data Exploration**: Select multiple states, a year, and several metrics to compare EV registration trends.
* **Key Metrics Visualization**: View average EV share by state, and explore the relationship between EV registrations and charging outlets, as well as gasoline prices.
* **Detailed State-Level Analysis**: Drill down into specific states and years to see the breakdown of charging outlet types (Level 1, Level 2, DC Fast) and key socioeconomic indicators.
* **Beliefs Comparison**: Compare public beliefs regarding climate change and environmental impact across selected states.

## Data Sources

The data used in this application is primarily sourced from:

* [EV Adoption in USA (2016-2023) on Kaggle](https://www.kaggle.com/datasets/surajshivakumar/ev-adoption-usa/data) by Suraj Shivakumar.

The data is consolidated into a single `EV_Data.csv` file. The emphasis of this project is on the visualizations and communication of insights rather than the data ingestion process itself. The `EV_Data.csv` file is included for redundancy and ease of use.

### Variable Descriptions

The variables we use from the `EV_Data.csv` file are:

**Vehicle & Infrastructure Data:**

* **state**: U.S. State
* **year**: Year of data collection
* **EV Registrations**: Number of electric vehicle registrations
* **Total Vehicles**: Total number of vehicles registered in the state
* **EV Share (%)**: Percentage of electric vehicles out of total vehicles
* **Total Charging Outlets**: Total number of charging outlets available across stations
* **Level 1**: Number of Level 1 charging outlets
* **Level 2**: Number of Level 2 charging outlets
* **DC Fast**: Number of DC Fast charging outlets
* **price\_cents\_per\_kwh**: Electricity price in cents per kilowatt-hour
* **gasoline\_price\_per\_gallon**: Gasoline price per gallon

**Public Opinion & Beliefs (Survey-based data, percentages of people who agree):**

* **affectweather**: Belief that global warming is affecting weather
* **devharm**: Belief that developing countries should do more to reduce global warming
* **discuss**: Frequency of discussing global warming
* **exp**: Personal experience with global warming impacts
* **localofficials**: Belief that local officials should do more to address global warming
* **personal**: Belief that global warming will harm them personally
* **reducetax**: Support for a carbon tax to reduce global warming
* **regulate**: Support for government regulation of greenhouse gas emissions
* **worried**: Level of worry about global warming

## Installation and Setup

To run this application locally, follow these steps:

1. **Clone the repository:**

   ```bash
   git clone https://github.com/niku4657/EV_Adoption_Dashboard.git
   cd EV_Adoption_Dashboard
   ```
2. **Create and activate a virtual environment (recommended):**

   ```bash
   python -m venv venv
   # On Windows
   .\venv\Scripts\activate
   # On macOS/Linux
   source venv/bin/activate
   ```
3. **Install the required packages:**

   ```bash
   pip install -r requirements.txt
   ```
4. **Run the Dash application:**

   ```bash
   jupyter notebook dashboard.ipynb
   ```

   Then, within the notebook, run all cells. The last cell `app.run(debug=True)` will start the server.
5. **Access the application:**
   Open your web browser and navigate to `http://127.0.0.1:8050/`.

## Application Structure

* `dashboard.ipynb`: The main Dash application file containing all the relevant code.
* `EV_Data.csv`: The dataset used for the dashboard.
* `requirements.txt`: Lists all Python dependencies required to run the application.
* `README.md`: This file, providing an overview and instructions.
