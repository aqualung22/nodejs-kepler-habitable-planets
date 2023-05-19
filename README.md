# Identifying possibly habitable Exoplanets from Kepler space telescope CSV data provided by NASA
## _Node.js - csv-parse library_

### Disclaimer
This research has made use of the NASA Exoplanet Archive, which is operated by the California Institute of Technology, under contract with the National Aeronautics and Space Administration under the Exoplanet Exploration Program.

### TL;DR
This README provides an overview of a Node.js project that analyzes publicly available Exoplanets data captured from the Kepler Telescope, reads a file, and identifies potentially habitable planets based on specific criteria. It includes information on how to set up the project, install dependencies, run the script, and view the output. Feel free to explore the code and customize it to meet your requirements.

### Prerequisites

Before starting, ensure you have the following installed on your system:

- Node.js (version 16.20.0 or higher). * As stated on Node.js website today, latest LTS Node.js version is 18.16.0 (includes npm 9.5.1) and Latest Current Version: 20.2.0 (includes npm 9.6.6)

* The project already comes with sample data, eg. a manually download file from [NASA Exoplanet Archive](https://exoplanetarchive.ipac.caltech.edu/cgi-bin/TblView/nph-tblView?app=ExoTbls&config=cumulative) @ caltech.edu @ KOI (Kepler Objects of Interest) page

If you wish, you can manually download a sample file and replace the existing one. Just follow these steps:
- Go to [https://exoplanetarchive.ipac.caltech.edu/cgi-bin/TblView/nph-tblView?app=ExoTbls&config=cumulative](https://exoplanetarchive.ipac.caltech.edu/index.html) and click on
   - Data
   - Download table 
   - CSV format
   - Download table 

### Installation

To set up the project, follow these steps:

1- Clone the project repository:
   
   ```bash
   git clone https://github.com/aqualung22/nodejs-kepler-habitable-planets
```   

2- Navigate to the project directory:

   ```bash
   cd nodejs-kepler-habitable-planets
```
3- Install the required dependencies using npm:

   ```bash
    npm install
```
This will install the csv-parse library (version 5.3.6) as a dependency.

### Project Structure

The project consists of the following files:

* **cumulative_2023.04.15_17.24.53.csv:** Sample CSV data, manually downloaded from NASA Exoplanet Archive.
 
* **package.json:** Contains metadata and project dependencies.

* **index.js:** Node.js script that reads a CSV file containing Exoplanets data and identifies possibly habitable planets.

### Usage

To run the project and identify possibly habitable planets, execute the following command:

```bash
node index.js
```

The script will read the file cumulative_2023.04.15_17.24.53.csv and apply the isHabitablePlanet function to each data entry. The function checks if a planet is possibly habitable based on specific criteria.

### Output

The script will output the number of possibly habitable planets found and their Kepler names.

```bash
$ node index.js 
8 habitable planets found!
[
  'Kepler-1652 b',
  'Kepler-1410 b',
  'Kepler-296 f',
  'Kepler-442 b',
  'Kepler-296 e',
  'Kepler-1649 b',
  'Kepler-62 f',
  'Kepler-452 b'
]
```
Please note that the actual number of habitable planets and their names may vary based on the data present in the CSV file you´re using.

