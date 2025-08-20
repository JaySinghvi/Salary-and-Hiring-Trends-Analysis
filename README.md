# Data Science Salary Analysis Project

## Overview
This project analyzes salary trends and hiring patterns in data science roles using automated data extraction from Glassdoor. The analysis provides insights into compensation patterns across different experience levels, company sizes, and years, with a focus on identifying market trends in the evolving data science landscape.

## Key Findings
- **Surge in hiring** by medium-sized companies for mid-level data roles
- **Notable decline** in total industry compensation in 2024 compared to 2023
- Comprehensive analysis of salary distributions based on experience, company size, and temporal trends

## Project Structure
```
├── README.md                    # Project documentation
├── data preprocessing.ipynb     # Data cleaning and preprocessing notebook
├── data_science_salaries.csv   # Raw dataset (6,599 entries)
├── salaries.csv                # Cleaned dataset (3,415 entries)
├── power_bi_dashboard.pbix      # Interactive Power BI dashboard
└── selenium_scraper.py          # Web scraping script (if applicable)
```

## Data Collection
- **Source**: Glassdoor job postings
- **Method**: Automated data extraction using Selenium
- **Original Dataset**: 6,599 salary records
- **Final Dataset**: 3,415 records (after preprocessing)

## Data Preprocessing Pipeline

### Initial Dataset
- **Size**: 6,599 entries × 11 columns
- **Columns**: job_title, experience_level, employment_type, work_models, work_year, employee_residence, salary, salary_currency, salary_in_usd, company_location, company_size

### Data Cleaning Steps
1. **Column Selection**: Removed redundant columns (salary, salary_currency, employee_residence)
2. **Filtering**:
   - Excluded non-full-time positions (Contract, Freelance, Part-time)
   - Focused on US-based companies only
   - Selected top data science roles: Data Scientist, Data Engineer, Data Analyst, ML Engineer, AI Scientist
3. **Data Standardization**:
   - Renamed columns for clarity (work_models → Work_Mode, etc.)
   - Standardized job titles (Machine Learning Engineer → ML Engineer)
4. **Final Cleanup**: Reset indices and exported clean dataset

### Final Dataset Characteristics
- **Size**: 3,415 entries × 6 columns
- **Time Range**: 2020-2024
- **Geographic Focus**: United States only
- **Employment Type**: Full-time positions only

## Dataset Schema
| Column | Description | Data Type |
|--------|-------------|-----------|
| Job_Title | Position title (Data Scientist, Data Engineer, etc.) | String |
| Experience | Experience level (Entry, Mid, Senior, Executive) | String |
| Work_Mode | Work arrangement (Remote, On-site, Hybrid) | String |
| Year | Work year (2020-2024) | Integer |
| Salary | Annual salary in USD | Integer |
| Company_Size | Company size category (Small, Medium, Large) | String |

## Analysis & Visualization

### Power BI Dashboard Features
- **Interactive Visualizations**: Dynamic charts and filters for exploring salary data
- **Salary Distribution Analysis**: Breakdown by experience level, company size, and year
- **Trend Analysis**: Year-over-year compensation changes
- **Comparative Views**: Cross-functional role comparisons
- **Market Insights**: Hiring pattern analysis by company size

### Key Metrics Tracked
- Average salary by job title and experience level
- Salary trends over time (2020-2024)
- Distribution of roles by company size
- Work mode preferences across different roles
- Geographic salary variations (US focus)

## Technical Implementation

### Tools & Technologies
- **Python**: Data preprocessing and analysis
  - pandas: Data manipulation
  - numpy: Numerical operations
- **Selenium**: Web scraping automation
- **Power BI**: Interactive dashboard development
- **Jupyter Notebook**: Data exploration and preprocessing

### Data Processing Workflow
1. **Data Extraction**: Automated scraping using Selenium
2. **Data Cleaning**: Comprehensive preprocessing in Jupyter notebook
3. **Data Analysis**: Statistical analysis and trend identification
4. **Visualization**: Interactive dashboard creation in Power BI

## Installation & Usage

### Prerequisites
```python
pip install pandas numpy selenium jupyter
```

### Running the Analysis
1. **Data Preprocessing**:
   ```bash
   jupyter notebook "data preprocessing.ipynb"
   ```

2. **Power BI Dashboard**:
   - Open `power_bi_dashboard.pbix` in Power BI Desktop
   - Refresh data connections if needed
   - Interact with visualizations using built-in filters

## Key Insights

### Market Trends (2023-2024)
- Overall compensation decline in 2024 compared to 2023
- Increased hiring activity in medium-sized companies
- Growing demand for mid-level data professionals

### Salary Patterns
- **Data Scientists**: Highest average compensation, especially at senior levels
- **Data Engineers**: Strong demand with competitive salaries
- **ML Engineers**: Premium compensation for specialized skills
- **Data Analysts**: Entry-level opportunities with growth potential

### Company Size Impact
- **Medium Companies**: Leading hiring surge for mid-level roles
- **Large Companies**: Higher compensation for senior positions
- **Small Companies**: Competitive entry-level opportunities

## Future Enhancements
- [ ] Real-time data updates integration
- [ ] Geographic expansion beyond US markets
- [ ] Skills-based salary analysis
- [ ] Industry-specific breakdowns
- [ ] Predictive modeling for salary trends

## Data Sources & Disclaimer
- Data sourced from Glassdoor through automated extraction
- Analysis focuses on US market trends (2020-2024)
- Salary figures represent reported compensation in USD
- Results should be considered alongside other market research

## Contributing
Contributions welcome! Please feel free to submit pull requests or open issues for:
- Data quality improvements
- Additional analysis dimensions
- Visualization enhancements
- Documentation updates
