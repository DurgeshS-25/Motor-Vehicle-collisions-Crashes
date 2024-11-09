# Project Title: Traffic Collision Data ETL and Analysis

## Group: 03

### Project Overview
This project involves the end-to-end ETL (Extract, Transform, Load) process of traffic collision data from Austin, Chicago, and New York, followed by staging, integration, and dimensional modeling to enable comprehensive analysis and reporting. The data is transformed and loaded into a dimensional model for analysis and visualization using tools like Tableau and Power BI.

### Project Phases

#### Phase 1: Data Profiling, Staging, and Dimensional Modeling
1. **Data Profiling**:
   - Conducted using Ydata Profile.
2. **Data Staging**:
   - Created staging tables for each dataset using Talend ETL jobs.
   - Performed initial transformations to standardize the data format across cities.
   - Handled null values, data type conversions (e.g., date parsing), and applied transformations based on source-specific requirements.
3. **Dimensional Model**:
   - Developed dimensional models with Fact and Dimension tables.
   - Defined mappings from source columns to target columns.
   - Created a mapping document to explain the transformations applied.
4. **Database**:
   - Data is stored in an Azure SQL Server, MySQL, or SQL Server database.

#### Phase 2: Data Integration and Validation
1. **Staging to Integration**:
   - Used Talend ETL jobs to load data from staging tables to the dimensional model.
   - Validated the data integrity and quality in the dimensional tables.
2. **Error Handling**:
   - Detailed documentation for rejected rows with explanations for rejection.
3. **Business Queries**:
   - Used SQL queries on the dimensional model to answer business-specific questions.

#### Phase 3: Data Visualization
1. **Visualizations**:
   - Created reports and dashboards using Tableau and Power BI.
   - Uploaded screenshots of all visualizations for reference.
   - Optional: Published reports to the cloud, based on access availability.

### Project Workflow

1. **Austin Dataset**:
   - Staging table setup, with specific transformations applied to columns like `CRASH_DATE` and `CRASH_TIME`.
   - Null values in longitude, latitude, and street names were handled.

2. **Chicago Dataset**:
   - Similar staging and transformations as Austin, with additional handling for unique Chicago-specific attributes.

3. **New York Dataset**:
   - Specific transformations and error handling, especially for `NUMBER_OF_PERSONS_INJURED` with unparsable values.

4. **Dimensional Modeling**:
   - Created `Address`, `Date`, `Time`, `Vehicle Type`, and `Contributing Factors` dimensions.
   - Designed a `Crash Fact` table integrating the staged data from all cities.

### Technologies Used
- **ETL**: Talend
- **Data Profiling**: Alteryx, Ydata
- **Database**: Azure SQL Server, MySQL, SQL Server
- **Visualization**: Tableau, Power BI

### How to Run the Project
1. **ETL Jobs**:
   - Load the Talend ETL jobs and connect to the staging database.
   - Execute the staging workflow for each dataset.
2. **SQL Queries**:
   - Execute the provided SQL scripts to load the data into the dimensional model.
3. **Visualization**:
   - Open Tableau or Power BI, load the dimensional tables, and create the specified visualizations.

### Documentation
- **Mapping Document**: Contains details on column mappings from source to target tables.
- **Transformation Document**: Lists all transformations applied at each stage.
- **Business Queries**: Contains SQL queries for answering business-specific questions.
