# Housing affordability for Miami artists and culture workers 


#### I. Introduction

Miami has long been a center of numerous cultures, experiences, and artistic traditions from all around the world, and in particular Latin America and the Caribbean. 

However, rapidly rising housing costs, rampant gentrification, and political pressures are making it increasingly difficult for the artistic community to survive and thrive. 

Objectives for this study: 
> Assess housing affordability for artists in Miami
> Analyze wage data and rental market trends 
> Identify affordable and unaffordable areas.


#### II. Data Collection 

Cleaned and processed four separate datasets: 

> 2023 Fair Market Rents by Zip Code and Unit Type     
> Average Rent over Time by Zip Code     
> OES Occupation - Hourly Wages     
> Quarterly Salary Earnings    
 
Datasets were sourced from:   
>[Department of Housing and Urban Development (FMR)](https://www.huduser.gov/portal/datasets/fmr/smallarea/index.html#rulemaking)  
>[Zillow Research - Housing Data](https://www.zillow.com/research/data/)   
>[Bureau of Labor Statistics](https://data.bls.gov/cew/apps/table_maker/v4/table_maker.htm#type=17&from=2022&to=2023&qtr=1&own=5&ind=7115&area=12086&supp=1)  
>[FloridaJobs.org](https://www.floridajobs.org/workforce-statistics/data-center/statistical-programs/occupational-employment-statistics-and-wages)  


#### III. Data Cleaning

#### 1. Fair Market Rent Dataset
- **Filter for Miami-Dade County:** Extracted all zip codes within Miami-Dade County.
- **Rental Affordability Calculations:** Added calculations to the dataset based on the widely-accepted financial principle of not spending more than 30% of monthly income on housing.
- **Hourly Wage Calculation (Future Consideration):** Initially included a calculation for the hourly wage required for a household with two breadwinners but removed it as it seemed redundant. This metric could be valuable for future visualizations.
- **Location Quotient Columns:** Clarified that these columns reveal a region's specialization in an industry compared to a larger geographic unit. Any value above 1 indicates a higher specialization.

#### 2. Average Rent over Time by Zip Code
- **Filter for Miami-Dade County:** Isolated data for Miami-Dade County.
- **Column Reduction:** Retained only the columns for dates and zip codes.
- **Transposition:** Transposed the dataset so that zip codes became column headers, and rows were dates.
- **Date Formatting:** Ensured all dates were converted to `pd.datetime` format for accurate interpretation in Tableau.

#### 3. Quarterly Salary Earnings
- **Data Cleaning and Merging:** Cleaned and merged four datasets.
- **NAICS-Occupation Code Filtering:** Filtered for codes related to the Arts/Design/Media industries.
- **Monthly Wage Calculation:** Converted weekly wages to monthly wages by adding a new calculation column.

#### 4. OES Occupation - Hourly Wages Dataset
- **Data Importation:** Imported the dataset starting from the fifth row.
- **Industry Filtering:** Filtered for OES Occupations within the Arts, Design, and Film Production industries. 

### Additional Notes
- The dataset and calculations are prepared with care to ensure accurate and meaningful insights when visualized in Tableau. Future iterations may expand upon the current metrics for deeper analysis such as hourly wage required for households with two breadwinners. 


#### IV. Key Findings 

> Rising Rent Across the County  
  - Regardless of zip code, rental prices rose much faster in comparison to previous years from 2021 onwards.

> Artists and Culture Workers are Vulnerable to the Rise in Cost of Living  
  - Due to the nature of gig work and in some cases having to take on a “day job” or several side gigs, artists as an occupational group are sensitive to these changes.
  
> More affordable zip codes are often very far from cultural centers  
  - As art is often a collaborative endeavor, artists having to move further away from their original neighborhoods or cultural touchstones can impact their work.

#### V. Additional Links 
> [Trello](https://trello.com/invite/b/10ctVZaQ/ATTI3eacb7eb5133048b958c7d8e6947139e3232A5E6/artists-and-housing-affordability-in-miami-dade-county)  
> [Presentation](https://www.canva.com/design/DAGJXw3wKwQ/LgAUV99pUsGYTQTcIJDjjg/view?utm_content=DAGJXw3wKwQ&utm_campaign=designshare&utm_medium=link&utm_source=editor)
