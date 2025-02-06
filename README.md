# WANG_NipahMProtein_2025

## Project Description
This repository contains code and data for the research project "Nipah virus matrix protein utilizes cortical actin to stabilize the virus assembly sites and promote budding".

## Repository Structure
- `k_stage_from_rawdata.py`: Main data processing script for analyzing experimental results
- `testdata.csv`: Test dataset for validation
- `Experiment_02_Plot.csv`: Experimental data for plotting and analysis
- `LICENSE`: License information

## Code Description
### k_stage_from_rawdata.py
This script processes and analyzes experimental data related to Nipah virus matrix protein interactions. The script performs the following operations:

#### Data Processing Pipeline
1. **Data Import and Preprocessing**
   - Reads multiple CSV files from specified directory
   - Removes unnamed columns and handles missing data
   - Merges data from multiple experiments into a single dataset

2. **Data Cleaning and Filtering**
   - Fills missing values using forward and backward filling methods
   - Shifts data to align time series
   - Normalizes data using MinMaxScaler

3. **Analysis Functions**
   - Implements cubic polynomial regression for curve fitting
   - Calculates derivatives for slope analysis
   - Identifies dwelling stages using slope thresholds
   - Determines key transition points in protein behavior

4. **Visualization and Output**
   - Generates plots for each analyzed dataset showing:
     * Original data points
     * Cubic fit curve
     * Highlighted dwelling regions
   - Saves results as PNG files
   - Exports analysis results to a tab-separated file

#### Key Parameters
- `k_up`: Upper threshold for slope analysis (default: 1)
- `k_down`: Lower threshold for slope analysis (default: -1)
- Time intervals: 5-unit intervals for measurements

## Usage Instructions
1. Ensure all required Python dependencies are installed:
   ```bash
   pip install pandas numpy scipy scikit-learn matplotlib
   ```

2. Prepare your data files:
   - CSV format
   - Data should contain intensity measurements over time
   - Files should be named consistently for batch processing

3. Run the data processing script:
   ```bash
   python k_stage_from_rawdata.py
   ```

### Input Data Format
The script expects CSV files with:
- Intensity measurements in columns
- Time points in rows
- Headers indicating measurement identifiers
- Data starting from row 4 (3 header rows are skipped)

### Output Files
1. **Merged Data**
   - `all_output.csv`: Combined raw data from all input files
   - `all_output_filtered.csv`: Processed and filtered data

2. **Analysis Results**
   - `results.txt`: Tab-separated file containing:
     * File identifiers
     * Column names
     * K values (slopes)
     * Top region start/end points
   - Individual PNG plots for each analyzed dataset

## Data Analysis Pipeline
The scripts in this repository process experimental data related to Nipah virus matrix protein interactions with cortical actin and their role in viral assembly and budding.

## Citation
If you use this code or data in your research, please cite:
[Citation information will be added upon publication]

## License
This project is licensed under the terms specified in the LICENSE file.

## Contact
For questions or issues, please open an issue in the repository or contact the project maintainers.
