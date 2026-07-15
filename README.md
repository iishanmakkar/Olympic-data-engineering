<<<<<<< HEAD
# Tokyo Olympics Data Engineering Project using Azure & Databricks

![Azure](https://img.shields.io/badge/Azure-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white)
![Databricks](https://img.shields.io/badge/Databricks-FF3621?style=for-the-badge&logo=databricks&logoColor=white)
![PySpark](https://img.shields.io/badge/PySpark-E25A1C?style=for-the-badge&logo=apachespark&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)

## Project Overview

This project demonstrates an end-to-end Azure data engineering pipeline using Azure Data Lake Storage Gen2 (ADLS Gen2) and Azure Databricks.

The pipeline ingests Tokyo Olympics datasets into Azure Data Lake, performs data cleaning and transformation with PySpark, generates analytical insights, and stores the transformed data back in ADLS for downstream analytics.

## Architecture

```text
Raw Dataset
  |
  v
Azure Data Lake Storage Gen2
  |
  v
Azure Databricks
(PySpark Transformations)
  |
  v
Cleaned / Transformed Data
  |
  v
Azure Data Lake Storage Gen2
  |
  v
Power BI / Azure Synapse / SQL Analytics
```

## Tech Stack

- Microsoft Azure
- Azure Data Lake Storage Gen2
- Azure Databricks
- Apache Spark
- PySpark
- Python
- Azure Active Directory OAuth Authentication
- Git and GitHub

## Dataset

The project uses Tokyo Olympics datasets:

- Athletes
- Coaches
- Medals
- Teams
- Entries by Gender

Example files:

- `athletes.csv`
- `coaches.csv`
- `medals.csv`
- `teams.csv`
- `entriesgender.csv`

## Project Structure

```text
Tokyo-Olympics-Data-Engineering/
|
├── data/
│   ├── athletes.csv
│   ├── coaches.csv
│   ├── medals.csv
│   ├── teams.csv
│   └── entriesgender.csv
|
├── Tokyo Olympic Transformation.ipynb
├── README.md
```

## Azure Services Used

| Service | Purpose |
| --- | --- |
| Azure Data Lake Storage Gen2 | Store raw and transformed datasets |
| Azure Databricks | Data processing using PySpark |
| Azure Active Directory | OAuth authentication |
| Azure Resource Group | Resource management |

## Authentication

Azure Databricks accesses ADLS Gen2 using OAuth authentication.

Authentication flow:

```text
Azure AD
  |
  v
Service Principal
  |
  v
OAuth Token
  |
  v
Azure Databricks
  |
  v
ADLS Gen2
```

Note: Never commit Client ID, Client Secret, or Tenant ID to GitHub. Use Databricks Secrets, Azure Key Vault, or environment variables instead.

## ETL Pipeline

### Step 1: Load CSV Files from ADLS

Raw data is loaded into PySpark DataFrames.

### Step 2: Data Cleaning

- Schema inference
- Data type conversion
- Remove invalid values
- Handle missing data
- Standardize columns

### Step 3: Data Transformation

- Convert columns to integer types
- Validate data
- Perform aggregations
- Sort records
- Run analytical queries

### Step 4: Analytics

Example analysis includes:

- Top countries by gold medals
- Gender participation ratio
- Dataset exploration
- Schema validation

### Step 5: Write Transformed Data

Transformed output is written back to ADLS Gen2 under `transformed-data/`.

## Sample Analysis

### Top Countries by Gold Medals

The medal dataset is sorted to display countries with the highest gold medal counts.

### Female vs Male Participation

Female and male participation percentages are calculated for each discipline.

## Running the Project

1. Clone the repository.

```bash
git clone https://github.com/<your-username>/Tokyo-Olympics-Data-Engineering.git
```

2. Open Azure Databricks and import the notebook: `Tokyo Olympic Transformation.ipynb`.

3. Configure ADLS access using OAuth authentication.

4. Run the notebook cells sequentially.

5. Verify the output in `transformed-data/` inside ADLS Gen2.

## Screenshots

Add project screenshots in an `images/` folder.

- `architecture.png`
- `adls.png`
- `databricks.png`
- `results.png`

## Future Improvements

- Delta Lake
- Medallion Architecture (Bronze, Silver, Gold)
- Azure Data Factory integration
- Azure Synapse Analytics
- Power BI dashboard
- Incremental data loading
- Automated data quality checks
- CI/CD using Azure DevOps
- Unity Catalog
- Workflow scheduling

## Learning Outcomes

Through this project, I learned:

- Azure Data Lake Storage Gen2
- Azure Databricks
- PySpark DataFrames
- Spark transformations
- Data cleaning
- Schema management
- Azure authentication
- Cloud data engineering
- Data analytics
- GitHub project deployment

## Skills Demonstrated

- Azure Cloud
- Azure Databricks
- ADLS Gen2
- PySpark
- Python
- Data Engineering
- ETL Pipelines
- Big Data Processing
- Data Transformation
- Cloud Storage
- Git
- GitHub

## Key Features

- End-to-end Azure data engineering project
- Azure Databricks
- ADLS Gen2
- OAuth authentication
- PySpark transformations
- Analytics
- Cloud storage
- Clean ETL pipeline
- GitHub ready

## Author

Ishan Makkar

- LinkedIn: https://www.linkedin.com/in/your-linkedin
- GitHub: https://github.com/iishanmakkar

## Star the Project

If you found this project helpful, please consider giving it a star on GitHub.
=======
# Olympic-data-engineering
>>>>>>> e3bb1e8b4aee0896fbc828cee226863b49e70569
