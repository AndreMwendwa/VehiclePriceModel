# Autotrader"# VehiclePriceModel" 

## Data Preprocessing and Cleaning Procedures
This appendix summarizes the preprocessing and cleaning procedures applied to the vehicle listings dataset prior to model estimation and analysis.

### Data Integration
Supplementary vehicle specification datasets containing automobile and engine information were imported from scraped JSON files. Nested JSON structures were flattened into tabular format and merged using vehicle identifiers.

### Standardization of Vehicle Identifiers
Vehicle make, model, and year were extracted and standardized using text-processing and regular-expression procedures. Identifiers were converted to lowercase and harmonized to improve matching accuracy across datasets.

### Cleaning of Technical Specification Variables
Technical variables such as engine displacement, horsepower, torque, dimensions, weight, acceleration, and fuel economy were converted from text strings containing units into numeric variables using regular-expression extraction and string cleaning procedures.

### Handling of Duplicate Records
Duplicate records generated during dataset merging were removed using duplicate elimination procedures. Where multiple technical specification records existed for the same make-model-year combination, numeric variables were aggregated using arithmetic means.

### Handling of Missing and Incomplete Data
Observations missing essential identifiers such as make, model, or year were removed. Missing technical specification variables were imputed using median values to reduce sensitivity to extreme observations.

### Handling of Outliers and Implausible Values
Observations with invalid or undefined price categories were removed. Descriptive statistics and ordered inspection procedures were used to identify implausible technical specification values, and a small number of clearly erroneous parsing outcomes were manually corrected.

### Categorical Variable Harmonization
Vehicle body types and related categorical variables were standardized using predefined mapping dictionaries to reduce inconsistencies across data sources.

### Final Dataset Construction
The cleaned and enriched dataset was exported for downstream statistical modelling and analysis. A smaller random sample was additionally generated for testing and reproducibility purposes.
