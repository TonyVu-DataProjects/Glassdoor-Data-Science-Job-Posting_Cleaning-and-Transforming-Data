# Glassdoor Data Science Job Posting - Data Cleaning & Transforming

## Table of Contents
- [Overview](#overview)
- [Dataset](#dataset)
- [Installation](#installation)
- [Methodology](#methodology)
- [Visualizations](#visualizations)
- [Conclusions](#conclusions)
- [Future Work](#future-work)
- [License](#license)
- [Contact](#contact)

## Overview
The aim of this project is to go through the dataset of Glassdoor Data Science Job Posting, identify any discrepancy in the data, and update those with various transformation techniques using Pandas functions. At the end of the project, we will have a cleaned and valid dataset which is ready for the next steps. 

## Dataset
Provide details about the dataset(s) used in the project.
- **Source**: [Kaggle](https://www.kaggle.com/datasets/rashikrahmanpritom/data-science-job-posting-on-glassdoor).
- **Description**: This is a dataset of data science job posts in Glassdoor. The data was scrapped from Glassdoor's website.

## Installation
Instructions for setting up the project locally. 

### Prerequisites
List any software, libraries, or tools required to run the project.
- [Jupyter Notebook](https://jupyter.org/install)

### Setup
Steps to install the necessary packages and set up the environment.

```bash
# Clone the repository
git clone https://github.com/TonyVu-DataProjects/Glassdoor-Data-Science-Job-Posting_Cleaning-and-Transforming-Data.git

or download zip file

# Navigate to the project directory
cd Glassdoor-Data-Science-Job-Posting_Cleaning-and-Transforming-Data

# Access Dashboards locally
# After install Jupyter Notebook, in the terminal type following command
jupyter notebook

# Notebook interface will prompt in your default browser. Then from the directory tree, select the file
Select "glassdoor-data-science-job-post-cleaning-data.ipynb" file
```

## Methodology
**Various data exploratory techniques were used as following:**
1. Descriptive statistics
    - Mean, median, mode, standard deviation, variance, percentiles, and etc.
2. Missing values detection
    - Total missing value counts
    - Heatmap
3. Feature Engineering
    - Transformation: Change the existing format to a new, more informative format.
    - New feature creation: Create new features derived from  existing features.
4. Shape & data types inspection

## Conclusions
**Detected issues**
1. Some Categorical features have meaningless value of '-1' like 'Industry', 'Sector'
2. Categorical features with values as ranges are too complex and hard to follow. E.g: 'Salary estimate' and 'Revenue' columns.
3. Some numerical feature like 'Rating' have uninformative value of -1.
4. The 'Job Description' feature has newline characters that provide no contextual meaning to the values.
5. The 'Company name' feature has newline characters and the rating attached to the actual values.
6. 'Location' and 'Headquarters' are both categorical and geographical. The values include City, State and Country together. Separating them would be better for visualization.
7. There are 13 duplicated rows.
8. Some useful new features include:
    - 'Company age': taking the difference between current year and the founded year.
    - 'tableau','excel','hadoop','python', 'power bi','r','sql': Boolean values to determine if a certain skill is required for the posting. These values can be derived by looking at content in the 'Job Description' feature. 

**Solutions:**  
*_Each solution's order corresponds to the issue's order_* 
1. Update '-1' values to 'Unknown'.
2. Transform long form formats to shorter, easy to read formats. 
3. Update value of -1 to 0.
4. Use replace function to remove newline characters.
5. Use replace function to remove newline characters and extra rating values.
6. Separate values into 'City', 'State', and 'Country' columns.
7. Drop duplicated rows using drop_duplicates function
8. Create new columns and do the needed operations.  

*_Details can be found in the notebook file_*

## License
- MIT License

## Contact
- Name: Tony Vu
- Email: [tonyknvu1@gmail.com](mailto:tonyknvu1@gmail.com)
- LinkedIn: [linkedin.com/in/tonyknvu](https://www.linkedin.com/in/tonyknvu/)
