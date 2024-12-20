# Project Title: Urban Traffic Collision Analytics ETL and Analysis

## Group: 03

### Project Overview
This project involves the end-to-end ETL (Extract, Transform, Load) process of traffic collision data from Austin, Chicago, and New York, followed by staging, integration, and dimensional modeling to enable comprehensive analysis and reporting. The data is transformed and loaded into a dimensional model for analysis and visualization using tools like Tableau and Power BI.

### Project Phases

#### [Phase 1](https://github.com/DurgeshS-25/Motor-Vehicle-collisions-Crashes/tree/main/Phase_01): Data Profiling, Staging, and Dimensional Modeling
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
   - Data is stored in  MySQL database.

#### [Phase 2](https://github.com/DurgeshS-25/Motor-Vehicle-collisions-Crashes/tree/main/Phase_02): Data Integration and Validation
1. **Staging to Integration**:
   - Used Talend ETL jobs to load data from staging tables to the dimensional model.
   - Validated the data integrity and quality in the dimensional tables.
2. **Error Handling**:
   - Detailed documentation for rejected rows with explanations for rejection.
3. **Business Queries**:
   - Used SQL queries on the dimensional model to answer business-specific questions.

#### [Phase 3](https://github.com/DurgeshS-25/Motor-Vehicle-collisions-Crashes/tree/main/Phase_03): Data Visualization
1. **Visualizations**:
   - Created reports and dashboards using [Tableau](https://github.com/DurgeshS-25/Motor-Vehicle-collisions-Crashes/blob/main/Phase_03/Final_Project_Tableau.twbx) and [Power BI](https://github.com/DurgeshS-25/Motor-Vehicle-collisions-Crashes/blob/main/Phase_03/Final_Project_PowerBI.pbit).
   - Uploaded screenshots of all visualizations for reference.
   - Optional: Published reports to the cloud, based on access availability.

### Project Workflow

1. [**Austin Dataset**](https://northeastern-my.sharepoint.com/:u:/r/personal/naveenhks_northeastern_edu/Documents/DAMG7370_Spring_2024/Final_Project_Datasets/Austin_Crash_Report_Data_-_Crash_Level_Records_20240326.tsv?csf=1&web=1&e=CmVozv):
   - Staging table setup, with specific transformations applied to columns like `CRASH_DATE` and `CRASH_TIME`.
   - Null values in longitude, latitude, and street names were handled.

2. [**Chicago Dataset**](https://northeastern-my.sharepoint.com/:u:/r/personal/naveenhks_northeastern_edu/Documents/DAMG7370_Spring_2024/Final_Project_Datasets/Chicago_Traffic_Crashes_-_Crashes_20240326.tsv?csf=1&web=1&e=oLyAEp):
   - Similar staging and transformations as Austin, with additional handling for unique Chicago-specific attributes.

3. [**New York Dataset**](https://northeastern-my.sharepoint.com/:u:/r/personal/naveenhks_northeastern_edu/Documents/DAMG7370_Spring_2024/Final_Project_Datasets/NY_Motor_Vehicle_Collisions_-_Crashes_20240326.tsv?csf=1&web=1&e=DFzsue):
   - Specific transformations and error handling, especially for `NUMBER_OF_PERSONS_INJURED` with unparsable values.

4. [**Dimensional Modeling**](https://github.com/DurgeshS-25/Motor-Vehicle-collisions-Crashes/blob/main/Phase_01/Dimensional_Model_Schema.sql):
   - Created `Address`, `Date`, `Time`, `Vehicle Type`, and `Contributing Factors` dimensions.
   - Designed a `Crash Fact` table integrating the staged data from all cities.

### Technologies Used
- **ETL**: Talend
- **Data Profiling**: Ydata
- **Database**: MySQL
- **Visualization**: Tableau, Power BI

### How to Run the Project
1. **ETL Jobs**:
   - Load the Talend ETL jobs and connect to the staging database.
   - Execute the staging workflow for each dataset.
2. **SQL Queries**:
   - Execute the provided SQL scripts to load the data into the dimensional model.
3. **Visualization**:
   - Open Tableau or Power BI, load the dimensional tables, and create the specified visualizations.

### [**Documentation**](https://github.com/DurgeshS-25/Motor-Vehicle-collisions-Crashes/blob/main/Phase_01/Workflow_explaination_final.docx)
- [**Mapping Document**](https://github.com/DurgeshS-25/Motor-Vehicle-collisions-Crashes/blob/main/Phase_01/Mapping_Document_final.xlsx): Contains details on column mappings from source to target tables.
- [**Business Queries**](https://github.com/DurgeshS-25/Motor-Vehicle-collisions-Crashes/blob/main/Phase_02/Business%20queries.sql): Contains SQL queries for answering business-specific questions.
