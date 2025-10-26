---
title: "Seasonality"
order: 3
weight: 3
format:
  html:
    toc: true
    toc-depth: 4
---

[Intermediate]{.tag .tag-intermediate}

## Overview

Seasonality refers to predictable, yearly changes driven by environmental factors such as rainfall, temperature, and humidity. In malaria, these changes matter because mosquito breeding and transmission depend heavily on rainfall. During rainy months, mosquito numbers and malaria cases rise; in dry months, breeding diminishes and cases drop.

Understanding these patterns helps programs plan **when** and **where** to act. Interventions such as **Seasonal Malaria Chemoprevention (SMC)**, **ITN distribution**, and **IRS campaigns** are most effective when scheduled before or during the high-transmission season.

::: {.callout-note title="Objectives" appearance="simple"}

* Identify areas with a seasonal rainfall pattern linked to predictable malaria transmission.
* Compare rainfall and malaria peaks to guide intervention timing.
* Use a rolling four-month window analysis to detect consistent seasonal patterns across multiple years.
* Classify areas as seasonal or non-seasonal based on pattern strength.
* Produce maps and summaries for program decision-making.
* Validate results with the SNT before using them for operational planning.

:::

## WHO 4-Month Rule

According to **WHO guidance**, a location is considered **seasonal** if **60% or more of total annual rainfall (or malaria cases)** occurs within **any 4 consecutive months**. This identifies likely periods of peak transmission and guides intervention timing.

::: {.callout-important title="Consult the SNT Team"}

The 4-month window and 60% threshold come from WHO recommendations, but rainfall and transmission patterns vary by country.

Before applying or adjusting this rule:

* Consult the **SNT** to confirm whether 60% is appropriate for the local context.
* Adjust if rainfall or malaria data show different timing patterns.
* Document and justify any modification to ensure national consistency.

:::

## Rolling Window Concept

Rather than fixing specific months (e.g., always June–September), test **all possible 4-month windows** in each year. For every starting month, compute:

* The **4-month total** (candidate rainy period), and
* The **12-month total** (comparison period).

Calculate the share of annual rainfall captured by each 4 month window. If the percentage is **≥ 60%**, that window is a **seasonal block**.

## Determine if Each Year is Seasonal

The table below tests rainfall concentration for a single year (**2023**). All twelve possible 4 month windows (from January through April to December through March) are examined. If any 4 month window exceeds 60% of the year's rainfall, the year is classified as **seasonal**.

| Start Month | End Month (4-Month Window) | 12-Month Comparison Period | Monthly Rainfall (mm) | Total Rainfall (4 Months) | Total Rainfall (12 Months) | % of Annual Rainfall | Meets 60% Rule? |
| :---------- | :------------------------- | :------------------------- | --------------------: | ------------------------: | -------------------------: | -------------------: | :-------------- |
| Jan 2023    | Apr 2023                   | Jan 2023 – Dec 2023        |   20 + 40 + 180 + 260 |                       500 |                        830 |                60.2% | Yes             |
| Feb 2023    | May 2023                   | Feb 2023 – Jan 2024        |  40 + 180 + 260 + 150 |                       630 |                        830 |                75.9% | Yes             |
| Mar 2023    | Jun 2023                   | Mar 2023 – Feb 2024        |  180 + 260 + 150 + 80 |                       670 |                        830 |                80.7% | Yes             |
| Apr 2023    | Jul 2023                   | Apr 2023 – Mar 2024        |   260 + 150 + 80 + 40 |                       530 |                        830 |                63.9% | Yes             |
| May 2023    | Aug 2023                   | May 2023 – Apr 2024        |    150 + 80 + 40 + 20 |                       290 |                        830 |                34.9% | No              |
| Jun 2023    | Sep 2023                   | Jun 2023 – May 2024        |     80 + 40 + 20 + 10 |                       150 |                        830 |                18.1% | No              |
| Jul 2023    | Oct 2023                   | Jul 2023 – Jun 2024        |     40 + 20 + 10 + 10 |                        80 |                        830 |                 9.6% | No              |
| Aug 2023    | Nov 2023                   | Aug 2023 – Jul 2024        |     20 + 10 + 10 + 20 |                        60 |                        830 |                 7.2% | No              |
| Sep 2023    | Dec 2023                   | Sep 2023 – Aug 2024        |     10 + 10 + 20 + 20 |                        60 |                        830 |                 7.2% | No              |
| Oct 2023    | Jan 2024                   | Oct 2023 – Sep 2024        |    10 + 20 + 40 + 180 |                       250 |                        830 |                30.1% | No              |
| Nov 2023    | Feb 2024                   | Nov 2023 – Oct 2024        |   20 + 40 + 180 + 260 |                       500 |                        830 |                60.2% | Yes             |
| Dec 2023    | Mar 2024                   | Dec 2023 – Nov 2024        |  40 + 180 + 260 + 150 |                       630 |                        830 |                75.9% | Yes             |

**Interpretation.** Several windows (e.g., **March–June** and **December–March**) exceed 60%, so **2023 is a seasonal year**. Repeat this process for every year in the dataset.

## Determine if the Location is Seasonal

Summarize results across all years to check **consistency**:

- Each 4-month period that meets the 60% rule counts as a **seasonal block**.
- If a year has at least one seasonal block, it is a **seasonal year**.
- If **all analyzed years** are seasonal, the **location is Seasonal overall**. If **any year** is not seasonal, the **location is Not Seasonal**.

### Scenario 1 — Non-Seasonal Location

| Year                       | Total 4-Month Blocks Tested | Seasonal Blocks (≥ 60%) | Is the Year Seasonal? |
| :------------------------- | --------------------------: | ----------------------: | :-------------------: |
| 2015                       |                          12 |                       2 |          Yes          |
| 2016                       |                          12 |                       1 |          Yes          |
| 2017                       |                          12 |                       1 |          Yes          |
| 2018                       |                          12 |                       2 |          Yes          |
| 2019                       |                          12 |                       0 |           No          |
| 2020                       |                          12 |                       1 |          Yes          |
| 2021                       |                          12 |                       2 |          Yes          |
| 2022                       |                          12 |                       1 |          Yes          |
| 2023                       |                          12 |                       3 |          Yes          |
| **Location Classification** |                           — |                       — | **Not Seasonal** (fails in 2019) |
**Interpretation.** Because **2019** fails, the pattern is inconsistent. The area is **Not Seasonal**, suggesting variable rainfall/transmission timing that weakens time-bound interventions like SMC.

### Scenario 2— Seasonal Location

| Year                       | Total 4-Month Blocks Tested | Seasonal Blocks (≥ 60%) | Is the Year Seasonal? |
| :------------------------- | --------------------------: | ----------------------: | :-------------------: |
| 2015                       |                          12 |                       1 |          Yes          |
| 2016                       |                          12 |                       2 |          Yes          |
| 2017                       |                          12 |                       1 |          Yes          |
| 2018                       |                          12 |                       1 |          Yes          |
| 2019                       |                          12 |                       1 |          Yes          |
| 2020                       |                          12 |                       1 |          Yes          |
| 2021                       |                          12 |                       2 |          Yes          |
| 2022                       |                          12 |                       1 |          Yes          |
| 2023                       |                          12 |                       1 |          Yes          |
| **Location Classification** |                           — |                       — | **Seasonal** (all years meet rule) |

**Interpretation.** Each year from 2015–2023 includes at least one 4-month period ≥ 60% of annual rainfall. The location is **Seasonal**, indicating a consistent rain-driven transmission cycle and **SMC eligibility**.

## Summary of the Logic

| Level of Analysis    | Criterion                      | Classification        |
| :------------------- | :----------------------------- | :-------------------- |
| 4-Month Block        | ≥ 60% of annual rainfall       | Seasonal Block        |
| Year                 | ≥ 1 seasonal block             | Seasonal Year         |
| Location (2015–2023) | All years seasonal             | Seasonal Location     |
|                      | One or more years not seasonal | Not Seasonal Location |

## Key Takeaways

* The rolling 4-month approach captures local variation in timing.
* A **seasonal block** means **≥ 60%** of annual rainfall.
* A **year** is seasonal if it contains at least one seasonal block.
* A **location** is seasonal if **all years** in scope have at least one seasonal block.
* Multi-year consistency supports precise timing for SMC and other rainfall-driven interventions.

## Data Requirements

Both rainfall and malaria case data can be used for seasonality analysis. This example uses rainfall because it closely reflects environmental drivers of transmission.

To ensure reliable classification:

* Provide **at least six consecutive years** of complete monthly data.
* Ensure **all twelve months** are present for each year.
* Handle missingness; incomplete data can misclassify areas.

::: {.callout-important title="Consult the SNT Team"}
The six-year minimum follows WHO analytical guidance. If the dataset is shorter (e.g., 4 years) the **SNT** should review and approve the adjustment.

Before proceeding, the SNT should:

- Confirm the time span reflects consistent climatic conditions.
- Ensure comparable data coverage across administrative areas.
- Document and justify any change for transparency and reproducibility.

:::

## Analytical Approach

This analysis uses **CHIRPS satellite-derived rainfall data** as a proxy for malaria transmission intensity. Sierra Leone serves as the case study, but the method generalizes to other countries with similar rainfall data.

* **Data Source:** Follow the procedures in the **CHIRPS data extraction guide** to obtain and prepare rainfall datasets:
  [https://ahadi-analytics.github.io/snt-code-library/english/library/data/climate/extract_raster_climate.html](https://ahadi-analytics.github.io/snt-code-library/english/library/data/climate/extract_raster_climate.html)

* **Processing:** Organize data by year, month, and administrative unit (e.g., district). Apply a **rolling 4-month window** within each 12-month period to compute rainfall concentration.

* **Classification:** If **≥ 60%** of annual rainfall falls within **any** 4 consecutive months, mark a **seasonal block** for that year/location. Repeat across multiple years to assess stability:

  * **Seasonal Location:** Every analyzed year contains ≥ 1 seasonal block.
  * **Not Seasonal Location:** ≥ 1 analyzed year contains **no** seasonal block.

* **Mapping:** Join results to geographic boundaries (e.g., district/ chiefdom shapefiles) to visualize spatial patterns of seasonality.

* **Review:** Share outputs with the **SNT** for validation against local transmission knowledge and for scheduling interventions (e.g., **SMC**).

## Profiling for Seasonality

The diagram below illustrates the complete seasonality analysis workflow used to determine SMC eligibility in malaria-endemic areas. This example uses **CHIRPS satellite-derived rainfall data from January 2018 to December 2023** (72 months total) for a hypothetical district in Sierra Leone.

![Profiling seasonality for SMC targeting](https://github.com/mohamedsillahkanu/snt-package/raw/7aca50c7688bbc679b33f5543150078c978c7edf/seasonality_eligibility_v2.png)

*Figure: Three-step seasonality profiling workflow using 2018-2023 rainfall data. The analysis identifies whether districts have consistent seasonal rainfall patterns suitable for SMC targeting.*



### What This Visualization Shows

The diagram demonstrates the three-step process for classifying locations as "Seasonal" or "Not Seasonal":

**Step 1: Divide data into month-blocks**
- The blue area chart shows monthly rainfall patterns across the 6-year period
- Colored horizontal bars represent different 4-month windows being tested (e.g., Jan-Apr 2018, Feb-May 2018, etc.)
- **Important limitation**: Not all possible blocks can be evaluated—month-blocks starting in 2023 cannot be fully assessed because they would require data extending into 2024 for the 12-month comparison period
- This creates a maximum of **61 evaluable month-blocks** rather than 72

**Step 2: Assess whether each month-block meets the 60% threshold**
- For each colored bar (4-month window), the analysis calculates:
  - The sum of rainfall in those 4 consecutive months (numerator)
  - The sum of rainfall in the 12 consecutive months starting from the same month (denominator)
- If the 4-month sum is **≥60% of the 12-month sum**, that block is considered a "seasonal peak"
- The 60% threshold is based on **WHO guidance** but should be validated with the Strategic National Team (SNT) for local applicability

**Step 3: Define and count seasonality peaks**
- The bar chart at the bottom shows all evaluated month-blocks across the timeline
- Purple bars = month-blocks that met the 60% threshold (seasonal peaks)
- Gray bars = month-blocks that did not meet the threshold
- Purple arrows highlight specific years where seasonal peaks occurred

### Classification Logic

A location is classified as **"Seasonal"** if it has **at least one seasonal peak in every analyzed year**. 

**Understanding this example:**
- The dataset contains rainfall data from **January 2018 to December 2023** (6 years total)
- However, only **5 complete years can be evaluated** (2018-2022)
- **Why is 2023 excluded?** Month-blocks starting in 2023 require data extending into 2024 for the 12-month comparison period. Since 2024 data is not available, 2023 cannot be fully assessed.
- This creates a maximum of **61 evaluable month-blocks** instead of 72

**In the diagram:**
- Purple arrows indicate years where seasonal peaks were identified
- The classification can be stated two ways:
  - **Including all data years:** "4 out of 5 years have seasonality peaks" (5 years of data, where year 5 is excluded from evaluation)
  - **Considering only evaluable years:** "4 out of 4 evaluable years have seasonality peaks" (only counting years that can be fully assessed)
- Both statements mean the same thing: **all evaluable years show seasonal patterns**, so this **district is classified as "Seasonal"**

::: {.callout-important title="Consult the SNT Team"}
Before applying this methodology, consult with the SNT to:
- Confirm the 60% threshold is appropriate for your local context
- Validate the "all evaluable years must be seasonal" classification rule
- Document any modifications to ensure consistency across the national program
:::

### Key Conventions Explained

1. **Why 4-month windows?** 
   - Malaria transmission typically peaks during a concentrated rainy season lasting 3-5 months
   - A 4-month window captures the core transmission period while being flexible enough to accommodate timing variations

2. **Why 60%?**
   - WHO recommends that locations where ≥60% of annual rainfall occurs in 4 consecutive months are suitable for seasonal interventions like SMC
   - This threshold ensures rainfall (and thus transmission) is sufficiently concentrated to make time-bound interventions effective

3. **Why rolling windows?**
   - Rather than assuming the rainy season always occurs in the same months (e.g., June-September), rolling windows test all possible 4-month periods
   - This accounts for geographic variation in rainy season timing across districts

4. **Why must ALL years be seasonal?**
   - Consistent, predictable patterns are essential for planning interventions like SMC
   - If transmission timing varies significantly between years, scheduled interventions may miss the actual peak

### Data Requirements for This Analysis

To replicate this analysis, you need:
- **Minimum 6 years** of continuous monthly data (WHO recommendation)
- **Complete coverage**: All 12 months must be present for each year
- **Data source**: CHIRPS satellite rainfall data or malaria case surveillance data
- **Geographic level**: Data aggregated by administrative unit (district, chiefdom, health facility catchment)

::: {.callout-important title="Consult the SNT Team"}
Before applying this methodology:

- Validate whether the 60% threshold is appropriate for your local context
- Confirm whether the "all years must be seasonal" rule should be relaxed (e.g., to "≥80% of years")
- Review whether 6 years of data adequately represents typical seasonal patterns in your setting
- Document any modifications to ensure consistency across the national program
:::


## Step-by-Step

The steps below walk through the complete seasonality analysis—from data preparation to classification and visualization. Each step explains the code logic and expected outputs.

To skip the step-by-step explanation, jump to the full code at the end of this page.

<a href="#bottom-section"><button class="btn btn-primary">Jump to Full Code</button></a>


### Step 1: Import packages and data

This step loads all the software tools (packages) needed for the analysis and reads your rainfall data file. The code first checks if the package manager 'pacman' is installed - this tool makes it easier to load multiple packages at once. Then it loads all required packages: readxl for reading Excel files, dplyr for data manipulation, openxlsx for writing Excel files, lubridate for handling dates, ggplot2 for creating plots, readr for reading data files, stringr for text manipulation, here for managing file paths, tidyr for data tidying, gridExtra for arranging plots, knitr for creating tables, writexl for writing Excel files, and sf for handling spatial data. Finally, it sets the path to the data file and loads the rainfall data into memory.

::: {.panel-tabset}
## R
```{R}
#| message: false
#| echo: true
#| eval: true
#| code-fold: false

if (!requireNamespace("pacman", quietly = TRUE)) install.packages("pacman")

pacman::p_load(
  readxl, dplyr, openxlsx, lubridate, ggplot2, readr, stringr, 
  here, tidyr, gridExtra, knitr, writexl, sf
)

# Load rainfall data
file_path <- here::here("english/data_r/modeled", "chirps_data_2015_2023_lastest.xls")
data <- readxl::read_excel(file_path)
```

**To adapt the code:**

- **Line 14**: Update file path to your rainfall dataset location
- **Line 15**: Change file name to match your data file

## Python
:::

### Step 2: Configure analysis parameters

This step sets up the "rules" for your analysis by telling R which columns in your data contain which information, what time period to analyze, and what threshold defines "seasonal." The year_column variable should be set to the name of the column containing years (like 2015, 2016, etc.), month_column to the column with months (1-12), value_column to the column with rainfall amounts, and admin_columns to the geographic unit names (like district and chiefdom). The analysis_start_year sets the first year to include in the analysis, analysis_start_month defines which month to start from (usually January = 1), and seasonality_threshold sets the percentage of annual rainfall that must occur in a 4-month period to be considered seasonal (60 is the WHO standard, meaning 60% of annual rainfall concentrated in 4 months). 


::: {.panel-tabset}
## R
```{R}
#| message: false
#| echo: true
#| eval: true
#| code-fold: false

# Column names in your dataset
year_column <- "Year"
month_column <- "Month"
value_column <- "mean_rain"
admin_columns <- c("FIRST_DNAM", "FIRST_CHIE")

# Analysis parameters
analysis_start_year <- 2015
analysis_start_month <- 1
seasonality_threshold <- 60  # 60% of annual rainfall in 4-month peak

# Output file names (uncomment to save)
# detailed_output <- "detailed_seasonality_results.xlsx"
# yearly_output <- "yearly_analysis_summary.xlsx"
# location_output <- "location_seasonality_summary.xlsx"
```

**To adapt the code:**

- **Lines 3-6**: Update column names to match your dataset structure
- **Lines 9-10**: Set your analysis start year and month
- **Line 11**: Adjust threshold (60 means 60% of annual rainfall occurs in peak 4 months)
- **Lines 14-16**: Uncomment and modify output file names if you want to save results

## Python
:::

### Step 3: Prepare data for analysis

Validate the dataset structure, filter to analysis period, and create administrative groupings.

#### Step 3.1: Check required columns

::: {.panel-tabset}
## R
```{R}
#| message: false
#| echo: true
#| eval: true
#| code-fold: false

# Verify all required columns exist
required_cols <- c(year_column, month_column, value_column, admin_columns)
missing_cols <- required_cols[!required_cols %in% colnames(data)]

if (length(missing_cols) > 0) {
  stop(paste("Missing columns:", paste(missing_cols, collapse = ", ")))
}
```

**To adapt the code:**

- No changes needed - uses parameters from Step 2

## Python
:::

#### Step 3.2: Filter data and ensure numeric month

::: {.panel-tabset}
## R
```{R}
#| message: false
#| echo: true
#| eval: true
#| code-fold: false

# Filter to analysis period and convert month to numeric
filtered_data <- data |>
  dplyr::filter(
    !is.na(!!sym(year_column)) & 
    !is.na(!!sym(month_column)) & 
    !!sym(year_column) >= analysis_start_year
  ) |>
  dplyr::mutate(Month = as.numeric(!!sym(month_column)))
```

**To adapt the code:**

- No changes needed - automatically uses your start year from Step 2

## Python
:::

### Step 3: Prepare Data for Analysis

This step ensures that your dataset is valid, complete, and properly structured for seasonality analysis. It begins by verifying that all required columns such as year, month, rainfall value, and administrative units are present in your data. Once confirmed, the process filters the dataset to include only the desired analysis period and converts the month values to numeric format to support accurate calculations. Next, it creates administrative groupings by combining one or more geographic levels such as district and chiefdom into a single variable to ensure each unique area is analyzed independently. Finally, the step checks that your dataset spans at least six years of data which is the minimum recommended duration for reliable seasonality classification.


#### Step 3.1 Check Required Columns

The code below verifies that all the necessary columns exist in your dataset before analysis begins. It identifies any missing columns and stops the process with a clear message so you can correct the issue.

::: {.panel-tabset}

## R

```{R}
#| message: false
#| echo: true
#| eval: true
#| code-fold: false

# Verify all required columns exist
required_cols <- c(year_column, month_column, value_column, admin_columns)
missing_cols <- required_cols[!required_cols %in% colnames(data)]

if (length(missing_cols) > 0) {
  stop(paste("Missing columns:", paste(missing_cols, collapse = ", ")))
}
```

**To adapt the code:**
- No changes are needed; it automatically uses your Step 2 parameters


After running this code, R checks that all required columns are present in your dataset. If any columns are missing, the code will stop and show which columns to correct. When no columns are missing, the code runs successfully without any message.

## Python

:::


#### Step 3.2 Filter Data and Ensure Numeric Month

The code below filters your dataset to include only the selected analysis period and removes records with missing years or months. It then converts the month values into numeric format to ensure accurate calculations.

::: {.panel-tabset}

## R

```{R}
#| message: false
#| echo: true
#| eval: true
#| code-fold: false

# Filter to analysis period and convert month to numeric
filtered_data <- data |>
  dplyr::filter(
    !is.na(!!sym(year_column)) & 
    !is.na(!!sym(month_column)) & 
    !!sym(year_column) >= analysis_start_year
  ) |>
  dplyr::mutate(Month = as.numeric(!!sym(month_column)))
```

**To adapt the code:**
- No edits are required; it automatically applies the analysis start year from Step 2

This code removes any missing or incomplete records from your dataset and keeps only data from the defined analysis period. It also ensures that the month column is in numeric format so that subsequent calculations will be accurate. After running the code, confirm that the number of rows in your filtered dataset is reasonable. If many rows are lost, check your original data for missing values.


## Python

:::


#### Step 3.3 Create Administrative Grouping Variable

The code below creates a single administrative grouping variable by combining one or more columns such as district and chiefdom. This ensures each geographic unit is analyzed separately.

::: {.panel-tabset}

## R

```{R}
#| message: false
#| echo: true
#| eval: true
#| code-fold: false

# Create combined admin grouping
if (length(admin_columns) == 1) {
  filtered_data$admin_group <- filtered_data[[admin_columns[1]]]
} else {
  filtered_data <- filtered_data |>
    dplyr::mutate(
      admin_group = paste(!!!syms(admin_columns), sep = " | ")
    )
}
```

**To adapt the code:**
- No edits are needed; it automatically handles single or multiple administrative levels

After running this code, a new column called `admin_group` is created. If you have one administrative level, the column simply copies that level. If you have more than one, it combines them into a single text string separated by a vertical bar. This allows R to analyze each unique administrative unit independently.


## Python

:::

#### Step 3.4 Validate Data Span

The code below checks whether your dataset covers at least six years, which is the recommended duration for detecting seasonal patterns. It also calculates the number of complete years and monthly analysis blocks available for use.

::: {.panel-tabset}

## R

```{R}
#| message: false
#| echo: true
#| eval: true
#| code-fold: false

# Check data availability
available_years <- sort(unique(filtered_data[[year_column]]))
data_span_years <- length(available_years)

if (data_span_years < 6) {
  stop(paste(
    "Insufficient data: Requires at least 6 years, but only", 
    data_span_years, "years found."
  ))
}

# Calculate number of analysis blocks (one per month for complete years)
num_complete_years <- data_span_years - 1
total_num_blocks <- num_complete_years * 12
```

**To adapt the code:**
- You may change the minimum year requirement (6) only after consulting with SNT and documenting the reason

This code counts the number of unique years in your dataset and confirms whether you have at least six years of data. If not, the code stops and provides an error message showing how many years were found. It also calculates how many complete years and monthly blocks can be analyzed. For example, data from 2015 to 2023 includes nine years, providing eight complete years and ninety-six monthly blocks for analysis.


## Python

:::




### Step 4: Generate Rolling Time Blocks

This step creates all the time windows needed for seasonality analysis. Instead of assuming the rainy season always occurs during the same months each year, this approach tests every possible 4-month period to find when peak rainfall actually occurs. For each location and each starting month, the code creates two overlapping windows: a 4-month window representing a potential peak season and a 12-month window representing the full year for comparison. By systematically testing all possible 4-month windows across the entire dataset, this method identifies the true timing of seasonal peaks without making assumptions about when they should occur.


#### Step 4.1 Define Month Names

The code below creates readable month labels that will be used when displaying date ranges in the output. These labels make it easier to interpret results by showing month names instead of numbers.


::: {.panel-tabset}
## R
```{R}
#| message: false
#| echo: true
#| eval: true
#| code-fold: false

# Month labels for output
month_names <- c("Jan", "Feb", "Mar", "Apr", "May", "Jun",
                 "Jul", "Aug", "Sep", "Oct", "Nov", "Dec")
```

**To adapt the code:**
- No changes needed

This creates a simple vector of month abbreviations. R will use these to create readable date labels like "Mar 2019-Jun 2019" instead of "3 2019-6 2019".

## Python
:::

#### Step 4.2 Initialize Block Storage

The code below prepares an empty data structure to store information about each time block and sets the starting point for the analysis.


::: {.panel-tabset}
## R
```{R}
#| message: false
#| echo: true
#| eval: true
#| code-fold: false

# Initialize block tracking
blocks <- data.frame()
current_year <- analysis_start_year
current_month <- analysis_start_month
```

**To adapt the code:**
- No changes needed - uses parameters from Step 2

The `blocks` data frame will store all time window definitions. The `current_year` and `current_month` variables track the starting point as the code moves forward one month at a time through the entire dataset.

## Python
:::

#### Step 4.3 Generate Rolling Windows

The code below creates all possible 4-month and 12-month time windows by systematically moving forward one month at a time through the dataset. For each starting month, it defines both a 4-month window (the potential peak period) and a 12-month window (the comparison period). The code handles year transitions automatically, ensuring that windows spanning December-January are calculated correctly.

::: {.panel-tabset}
## R
```{R}
#| message: false
#| echo: true
#| eval: true
#| code-fold: false

for (i in 1:total_num_blocks) {
  # Define 4-month window
  start_4m_year <- current_year
  start_4m_month <- current_month
  end_4m_year <- current_year
  end_4m_month <- current_month + 3
  
  if (end_4m_month > 12) {
    end_4m_year <- end_4m_year + 1
    end_4m_month <- end_4m_month - 12
  }

  # Define 12-month window  
  start_12m_year <- current_year
  start_12m_month <- current_month
  end_12m_year <- current_year
  end_12m_month <- current_month + 11
  
  if (end_12m_month > 12) {
    end_12m_year <- end_12m_year + 1
    end_12m_month <- end_12m_month - 12
  }

  # Create readable date range label
  date_range <- paste0(
    month_names[start_4m_month], " ", start_4m_year, "-",
    month_names[end_4m_month], " ", end_4m_year
  )
  
  # Store block definition
  blocks <- rbind(blocks, data.frame(
    block_number = i,
    start_4m_year = start_4m_year,
    start_4m_month = start_4m_month,
    end_4m_year = end_4m_year,
    end_4m_month = end_4m_month,
    start_12m_year = start_12m_year,
    start_12m_month = start_12m_month,
    end_12m_year = end_12m_year,
    end_12m_month = end_12m_month,
    date_range = date_range
  ))

  # Advance to next month
  current_month <- current_month + 1
  if (current_month > 12) {
    current_month <- 1
    current_year <- current_year + 1
  }
}
```

**To adapt the code:**
- No changes needed - automatically generates all blocks based on your data span

This loop creates one time block for each month in your dataset. For example, if you have data from January 2015 to December 2023 (9 years), it creates 96 blocks (8 complete years × 12 months). Each block contains the start and end dates for both the 4-month and 12-month windows, plus a readable label like "Jan 2015-Apr 2015". The code automatically handles transitions between months and years, so a 4-month window starting in November 2019 will correctly span November 2019 through February 2020.

## Python
:::

### Step 5: Calculate Seasonality for Each Block

This step applies the WHO 60% rule to determine which time blocks represent seasonal peaks. For each location and each time block, the code calculates how much rainfall fell during the 4-month window and compares it to the total rainfall during the corresponding 12-month period. If the 4-month total represents 60% or more of the 12-month total, that block is marked as seasonal. This calculation is repeated for every location and every time block, creating a comprehensive dataset that shows exactly when and where seasonal patterns occur.


#### Step 5.1 Initialize Results Storage

The code below prepares a data structure to store seasonality calculations for all locations and time blocks, and creates a list of all unique geographic units to analyze.


::: {.panel-tabset}
## R
```{R}
#| message: false
#| echo: true
#| eval: true
#| code-fold: false

# Initialize results dataframe
detailed_results <- data.frame()

# Get all locations to analyze
admin_groups <- unique(filtered_data$admin_group)
```

**To adapt the code:**
- No changes needed

The `detailed_results` data frame will store seasonality calculations for every combination of location and time block. The `admin_groups` variable contains all unique geographic units (districts, chiefdoms, etc.) that need to be analyzed separately.

## Python
:::

#### Step 5.2 Calculate Seasonality Per Location and Block

The code below performs the core seasonality calculation. It loops through each location and each time block, extracting the relevant rainfall data for both the 4-month and 12-month windows. It then calculates what percentage of the annual rainfall occurred during the 4-month period and determines whether this meets the 60% threshold for being classified as seasonal.

::: {.panel-tabset}
## R
```{R}
#| message: false
#| echo: true
#| eval: true
#| code-fold: false

for (admin_unit in admin_groups) {
  # Get data for this location
  unit_data <- filtered_data |> dplyr::filter(admin_group == admin_unit)
  
  for (i in 1:nrow(blocks)) {
    block <- blocks[i, ]
    
    # Convert year-month to comparable format
    unit_data_ym <- unit_data[[year_column]] * 12 + unit_data$Month
    
    # Extract 4-month window data
    start_4m_ym <- block$start_4m_year * 12 + block$start_4m_month
    end_4m_ym <- block$end_4m_year * 12 + block$end_4m_month
    data_4m <- unit_data |> 
      dplyr::filter(unit_data_ym >= start_4m_ym & unit_data_ym <= end_4m_ym)
    total_4m <- sum(data_4m[[value_column]], na.rm = TRUE)

    # Extract 12-month window data
    start_12m_ym <- block$start_12m_year * 12 + block$start_12m_month
    end_12m_ym <- block$end_12m_year * 12 + block$end_12m_month
    data_12m <- unit_data |> 
      dplyr::filter(unit_data_ym >= start_12m_ym & unit_data_ym <= end_12m_ym)
    total_12m <- sum(data_12m[[value_column]], na.rm = TRUE)

    # Calculate seasonality percentage
    percent_seasonality <- ifelse(total_12m > 0, (total_4m / total_12m) * 100, 0)
    is_seasonal <- as.numeric(percent_seasonality >= seasonality_threshold)

    # Build result row
    result_row <- data.frame(
      Block = i,
      DateRange = block$date_range,
      Total_4M = total_4m,
      Total_12M = total_12m,
      Percent_Seasonality = round(percent_seasonality, 2),
      Seasonal = is_seasonal,
      stringsAsFactors = FALSE
    )

    # Add administrative unit columns
    if (length(admin_columns) > 1) {
      admin_parts <- strsplit(admin_unit, " \\| ")[[1]]
      for (j in seq_along(admin_columns)) {
        result_row[[admin_columns[j]]] <- 
          ifelse(j <= length(admin_parts), admin_parts[j], NA)
      }
    } else {
      result_row[[admin_columns[1]]] <- admin_unit
    }

    detailed_results <- rbind(detailed_results, result_row)
  }
}
```

**To adapt the code:**
- No changes needed - uses threshold from Step 2

This nested loop performs calculations for every combination of location and time block. For each combination, it: (1) converts year-month values to a single comparable number to make date filtering easier, (2) extracts all rainfall data falling within the 4-month window and sums it, (3) extracts all rainfall data falling within the 12-month window and sums it, (4) calculates what percentage the 4-month total represents of the 12-month total, (5) determines if this percentage meets or exceeds the 60% threshold, and (6) stores all these values along with the location information in the results data frame. By the end of this step, you will have a complete record showing whether each time block at each location qualified as seasonal.

## Python
:::

#### Step 5.3 Preview Results

The code below displays a sample of the detailed seasonality results and optionally saves the complete results to an Excel file for further analysis.

::: {.panel-tabset}
## R
```{R}
#| message: false
#| echo: true
#| eval: false
#| code-fold: false

# Save detailed results (uncomment to use)
# writexl::write_xlsx(detailed_results, detailed_output)

# Display preview
knitr::kable(head(detailed_results), caption = "Preview of Block-Level Results")
```

::: {.callout-note title="Output" icon="false"}
```{R}
#| message: false
#| echo: false
#| eval: true

knitr::kable(head(detailed_results), caption = "Preview of Block-Level Results")
```
:::

**To adapt the code:**
- **Line 2**: Uncomment to save results to Excel

The table preview shows the first few rows of block-level results. Each row represents one time block at one location, showing: the block number, date range, rainfall totals for both the 4-month and 12-month periods, the calculated seasonality percentage, whether it meets the seasonal threshold (1 = yes, 0 = no), and the geographic unit. Uncommenting line 2 will save all results to Excel for detailed review and quality checking.

## Python
:::

### Step 6: Generate Yearly Summary

This step aggregates the block-level results to determine whether each location showed seasonal behavior in each year of the analysis. A year is classified as seasonal if it contains at least one 4-month block that meets the 60% threshold. This year-by-year summary is essential for the final classification because a location is only considered "Seasonal overall" if it shows seasonal patterns consistently across all analyzed years. The code groups the detailed results by location and year, counts how many seasonal blocks occurred in each year, and determines whether each year qualifies as seasonal.


#### Step 6.1 Extract Year from Date Ranges

The code below extracts the starting year from each date range label so that blocks can be grouped by year. This allows the analysis to assess seasonality on a year-by-year basis.


::: {.panel-tabset}
## R
```{R}
#| message: false
#| echo: true
#| eval: true
#| code-fold: false

# Extract start year from DateRange column
detailed_results$StartYear <- sapply(detailed_results$DateRange, function(x) {
  parts <- strsplit(x, "-")[[1]]
  first_part <- trimws(parts[1])
  as.numeric(substr(first_part, nchar(first_part) - 3, nchar(first_part)))
})
```

**To adapt the code:**
- No changes needed

This code parses each date range label (like "Jan 2015-Apr 2015") to extract the starting year. It splits the text at the dash, takes the first part, trims any whitespace, and extracts the last four characters which represent the year. This year value is added as a new column called `StartYear` that will be used for grouping in the next step.

## Python
:::

#### Step 6.2 Summarize by Location and Year

The code below groups the block-level results by location and year, then counts how many seasonal blocks occurred in each year at each location. A year is classified as seasonal if it contains at least one seasonal block.


::: {.panel-tabset}
## R
```{R}
#| message: false
#| echo: true
#| eval: true
#| code-fold: false

# Count seasonal blocks per location per year
yearly_summary <- detailed_results |>
  dplyr::group_by(dplyr::across(dplyr::all_of(admin_columns)), StartYear) |>
  dplyr::summarise(
    Year = dplyr::first(StartYear),
    SeasonalCount = sum(Seasonal, na.rm = TRUE),
    total_blocks_in_year = 12,
    at_least_one_seasonal_block = as.numeric(SeasonalCount > 0),
    .groups = 'drop'
  )
```

**To adapt the code:**
- No changes needed

This code groups all the detailed results by location and year, then summarizes them. For each location-year combination, it counts how many of the twelve possible 4-month blocks met the seasonal threshold (`SeasonalCount`), records the total number of blocks tested (always 12), and creates a binary indicator showing whether at least one block was seasonal (1 = yes, 0 = no). This binary indicator is crucial because it implements the WHO rule that a year is seasonal if it has at least one seasonal peak, regardless of how many seasonal blocks it contains.

## Python
:::

#### Step 6.3 Add Readable Year Labels

The code below adds descriptive labels to each year showing example date ranges that represent typical seasonal blocks for that year. These labels help with interpretation and reporting.


::: {.panel-tabset}
## R
```{R}
#| message: false
#| echo: true
#| eval: true
#| code-fold: false

# Add descriptive year period labels
yearly_summary <- yearly_summary |>
  dplyr::mutate(
    year_period = paste0(
      "(Jan ", Year, "-Apr ", Year, ", Dec ", Year, "-Mar ", Year + 1, ")"
    )
  ) |>
  dplyr::select(
    Year, 
    dplyr::all_of(admin_columns), 
    year_period, 
    total_blocks_in_year, 
    at_least_one_seasonal_block
  ) |>
  dplyr::arrange(Year, dplyr::across(dplyr::all_of(admin_columns)))
```

**To adapt the code:**
- No changes needed

This code creates a readable year label showing example blocks from each year. For instance, for 2019 it creates "(Jan 2019-Apr 2019, Dec 2019-Mar 2020)" which shows that blocks being evaluated for 2019 start as early as January and can extend into the following year. The code then reorders the columns to put the most important information first and sorts the results by year and location for easier review.

## Python
:::

#### Step 6.4 Preview Yearly Summary

The code below displays the last ten rows of the yearly summary to show recent years, and optionally saves the complete yearly summary to Excel.

::: {.panel-tabset}
## R
```{R}
#| message: false
#| echo: true
#| eval: false
#| code-fold: false

# Save yearly summary (uncomment to use)
# writexl::write_xlsx(yearly_summary, yearly_output)

# Display last 10 rows
knitr::kable(
  tail(yearly_summary, 10), 
  caption = "Yearly Seasonality Summary (Last 10 rows)"
)
```

::: {.callout-note title="Output" icon="false"}
```{R}
#| message: false
#| echo: false
#| eval: true

knitr::kable(
  tail(yearly_summary, 10), 
  caption = "Yearly Seasonality Summary (Last 10 rows)"
)
```
:::

**To adapt the code:**
- **Line 2**: Uncomment to save results to Excel

The table shows the yearly classification for the most recent years in your dataset. Each row represents one location in one year. The `at_least_one_seasonal_block` column shows whether that location-year combination qualified as seasonal (1 = yes, 0 = no). Uncommenting line 2 will save the complete yearly summary for all years and all locations to Excel.

## Python
:::

### Step 7: Location-Level Seasonality Classification

This step produces the final classification by determining whether each location shows consistent seasonal patterns across all analyzed years. According to WHO guidance, a location is classified as "Seasonal" only if every year in the analysis contains at least one seasonal block. If even a single year fails to show a seasonal pattern, the location is classified as "Not Seasonal" because the inconsistency makes it unsuitable for time-bound interventions like SMC. The code aggregates the yearly results, counts how many years were seasonal at each location, and applies the classification rule.


#### Step 7.1 Aggregate Across Years

The code below groups the yearly summary by location and counts how many years showed seasonal patterns at each location, along with the total number of years analyzed.


::: {.panel-tabset}
## R
```{R}
#| message: false
#| echo: true
#| eval: true
#| code-fold: false

# Count how many years each location was seasonal
location_summary <- yearly_summary |>
  dplyr::group_by(dplyr::across(dplyr::all_of(admin_columns))) |>
  dplyr::summarise(
    SeasonalYears = sum(at_least_one_seasonal_block, na.rm = TRUE),
    TotalYears = dplyr::n(),
    .groups = 'drop'
  )
```

**To adapt the code:**
- No changes needed

This code collapses the yearly summary to the location level. For each unique location, it sums up how many years qualified as seasonal (`SeasonalYears`) and counts how many years were analyzed in total (`TotalYears`). For example, if a location has data from 2015-2023, and six of those eight evaluable years had at least one seasonal block, `SeasonalYears` would be 6 and `TotalYears` would be 8.

## Python
:::

#### Step 7.2 Apply Classification Rule

The code below implements the WHO classification rule: a location is "Seasonal" if and only if every analyzed year showed at least one seasonal block. If any year failed to show seasonality, the location is classified as "Not Seasonal".


::: {.panel-tabset}
## R
```{R}
#| message: false
#| echo: true
#| eval: true
#| code-fold: false

# Classify: Seasonal = all years seasonal, otherwise Not Seasonal
location_summary <- location_summary |>
  dplyr::mutate(
    Seasonality = ifelse(
      SeasonalYears == TotalYears, 
      "Seasonal", 
      "Not Seasonal"
    )
  ) |>
  dplyr::arrange(dplyr::across(dplyr::all_of(admin_columns)))
```

**To adapt the code:**
- **Lines 5-8**: Modify classification logic if you want different criteria (e.g., seasonal in ≥80% of years)

This code applies the classification rule by checking if the number of seasonal years equals the total number of years. If they match, every year was seasonal and the location is classified as "Seasonal". If they don't match, at least one year failed the seasonal test and the location is classified as "Not Seasonal". The strict "all years" requirement ensures that only locations with highly consistent, predictable patterns are recommended for seasonal interventions. You can modify lines 5-8 to use a less strict rule (such as requiring 80% of years to be seasonal) only after consulting with the SNT team and documenting the rationale.

## Python
:::

#### Step 7.3 Preview and Save Classification

The code below displays the first ten locations from the final classification and optionally saves the complete classification to Excel for program planning.

::: {.panel-tabset}
## R
```{R}
#| message: false
#| echo: true
#| eval: false
#| code-fold: false

# Save location classification (uncomment to use)
# writexl::write_xlsx(location_summary, location_output)

# Display results
knitr::kable(
  head(location_summary, 10), 
  caption = "Location Seasonality Classification"
)
```

::: {.callout-note title="Output" icon="false"}
```{R}
#| message: false
#| echo: false
#| eval: true

knitr::kable(
  head(location_summary, 10), 
  caption = "Location Seasonality Classification"
)
```
:::

**To adapt the code:**
- **Line 2**: Uncomment to save final classification to Excel

The output table shows each location with its seasonal year count, total years analyzed, and final classification. For example, a location showing "SeasonalYears = 8, TotalYears = 8, Seasonality = Seasonal" had seasonal patterns in all eight analyzed years and is therefore eligible for seasonal interventions. Uncommenting line 2 saves this classification to Excel for distribution to the SNT team and program planners.

## Python
:::

### Step 8: Merge with Spatial Data for Visualization

This step prepares the seasonality results for mapping by joining them with geographic boundary data. Maps are essential for communicating seasonality patterns to decision-makers and identifying spatial clusters of seasonal or non-seasonal areas. The code loads a shapefile containing the geographic boundaries of administrative units, reads the seasonality classification results, and merges them based on matching administrative unit names. This creates a spatial dataset where each geographic boundary is tagged with its seasonality classification, enabling the creation of informative maps in the following steps.


::: {.panel-tabset}
## R
```{R}
#| message: false
#| echo: true
#| eval: true
#| code-fold: false

# Load spatial data
shapefile_path <- here::here("english/data_r/shapefiles", "Chiefdom2021.shp")
spatial_data <- sf::st_read(shapefile_path)

# Load seasonality results if not in environment
seasonality_path <- here::here(
  "english/library/stratification/other", 
  "final_SMC_eligibility.xlsx"
)
category_data <- readxl::read_excel(seasonality_path)

# Merge spatial and seasonality data
merged <- spatial_data |>
  dplyr::left_join(category_data, by = c("FIRST_DNAM", "FIRST_CHIE"))
```

**To adapt the code:**
- **Line 3**: Update shapefile path to your administrative boundary file
- **Lines 6-9**: Update path to your seasonality results file
- **Line 13**: Adjust join columns to match your admin unit names in both datasets

This code performs three operations: First, it loads the shapefile containing geographic boundaries using the `sf` package. Second, it loads the seasonality classification results from an Excel file. Third, it joins these datasets using a left join, which keeps all geographic boundaries and adds seasonality information where available. The join is based on administrative unit names (in this example, district and chiefdom). After merging, each geographic boundary polygon now has associated seasonality attributes such as the classification (Seasonal or Not Seasonal) and the number of seasonal years. If your admin unit names don't match exactly between the shapefile and classification file, the join will fail - you may need to clean and standardize the names first.

## Python
:::

### Step 9: Map Years with Seasonal Peaks

This step creates a map showing how many years each location exhibited seasonal rainfall patterns. This visualization is useful for understanding the strength and consistency of seasonal signals across different areas. Locations that were seasonal in many years have strong, reliable patterns suitable for intervention planning, while locations with fewer seasonal years may have more variable rainfall patterns. The code prepares the data for mapping, defines a color scheme where different numbers of seasonal years receive different colors, and creates a map with a legend showing how many locations fall into each category.


::: {.panel-tabset}
## R
```{R}
#| message: false
#| echo: true
#| eval: false
#| code-fold: true

# Prepare data for mapping
merged$category <- as.character(merged$SeasonalYears)
merged$category[is.na(merged$category)] <- "0"

# Define color palette
category_colors <- c(
  "0" = "gray80",   # No seasonal years
  "1" = "#4E79A7",  "2" = "#F28E2B", "3" = "#E15759",
  "4" = "#76B7B2",  "5" = "#59A14F", "6" = "#EDC948",
  "7" = "#4E79A7",  "8" = "#AF7AA1"
)

# Convert to factor with proper ordering
merged$category <- factor(merged$category, levels = as.character(0:8))

# Count locations in each category
cat_counts <- table(merged$category)
cat_counts <- cat_counts[cat_counts > 0]

# Create legend labels with counts
legend_labels <- paste0(names(cat_counts), " (", cat_counts, ")")
names(legend_labels) <- names(cat_counts)

# Filter colors to categories that exist
category_colors_filtered <- category_colors[names(category_colors) %in% names(cat_counts)]

# Create map
p <- ggplot(merged) +
  geom_sf(aes(fill = category), color = "white", size = 0.2) +
  scale_fill_manual(
    values = category_colors_filtered,
    labels = legend_labels,
    name = "Years with\nSeasonal Peak"
  ) +
  theme_void() +
  theme(
    legend.position = "right",
    plot.title = element_text(hjust = 0.5, size = 14, face = "bold")
  ) +
  labs(title = "Number of Years with Seasonal Rainfall Patterns")

print(p)
```

::: {.callout-note title="Output" icon="false"}
```{R}
#| message: false
#| echo: false
#| eval: true

# Prepare data
merged$category <- as.character(merged$SeasonalYears)
merged$category[is.na(merged$category)] <- "0"

category_colors <- c(
  "0" = "gray80", "1" = "#4E79A7", "2" = "#F28E2B", "3" = "#E15759",
  "4" = "#76B7B2", "5" = "#59A14F", "6" = "#EDC948",
  "7" = "#4E79A7", "8" = "#AF7AA1"
)

merged$category <- factor(merged$category, levels = as.character(0:8))

cat_counts <- table(merged$category)
cat_counts <- cat_counts[cat_counts > 0]

legend_labels <- paste0(names(cat_counts), " (", cat_counts, ")")
names(legend_labels) <- names(cat_counts)

category_colors_filtered <- category_colors[names(category_colors) %in% names(cat_counts)]

p <- ggplot(merged) +
  geom_sf(aes(fill = category), color = "white", size = 0.2) +
  scale_fill_manual(
    values = category_colors_filtered,
    labels = legend_labels,
    name = "Years with\nSeasonal Peak"
  ) +
  theme_void() +
  theme(
    legend.position = "right",
    plot.title = element_text(hjust = 0.5, size = 14, face = "bold")
  ) +
  labs(title = "Number of Years with Seasonal Rainfall Patterns")

print(p)
```
:::

**To adapt the code:**
- **Lines 11-15**: Modify color palette if desired
- **Line 43**: Change map title as needed

This code creates a choropleth map where each location is colored according to how many years it showed seasonal patterns. The process involves: (1) converting the seasonal year count to a categorical variable and replacing missing values with "0", (2) defining a color palette with one color for each possible number of seasonal years (0 through 8), (3) counting how many locations fall into each category to create informative legend labels that show both the number of seasonal years and the count of locations in that category, (4) filtering the color palette to include only categories that actually exist in the data, and (5) creating the map using ggplot2 with geographic boundaries colored by category. The legend shows, for example, "6 (45)" meaning 45 locations had seasonal patterns in 6 out of 8 years. This map helps identify geographic clusters and assess the spatial distribution of seasonal pattern strength.

## Python
:::

### Step 10: Map Final Seasonality Classification

This step creates the definitive map showing which locations are classified as "Seasonal" versus "Not Seasonal" for program planning. Unlike the previous map which showed the number of seasonal years, this binary classification map directly communicates SMC eligibility based on the WHO criterion of consistent seasonality across all years. The map uses distinct colors for seasonal and non-seasonal areas, overlays district boundaries in black for geographic reference, and includes a legend showing the count of locations in each category. This is typically the primary map shared with the SNT team and used for intervention planning.


::: {.panel-tabset}
## R
```{R}
#| message: false
#| echo: true
#| eval: false
#| code-fold: true

# Handle missing values
merged$Seasonality[is.na(merged$Seasonality)] <- "No data"

# Define colors
colors <- c(
  "Seasonal" = "#47B5FF",
  "Not Seasonal" = "#FFB3BA",
  "No data" = "white"
)

# Create district boundaries for overlay
boundaries <- merged |>
  dplyr::group_by(FIRST_DNAM) |>
  dplyr::summarise(geometry = sf::st_union(geometry))

# Convert to factor
merged$Seasonality <- factor(
  merged$Seasonality, 
  levels = c("Seasonal", "Not Seasonal", "No data")
)

# Count categories
cat_counts <- table(merged$Seasonality)
cat_counts <- cat_counts[cat_counts > 0]

# Create legend labels with counts
legend_labels <- paste0(names(cat_counts), " (", cat_counts, ")")
names(legend_labels) <- names(cat_counts)

# Filter colors
colors_filtered <- colors[names(colors) %in% names(cat_counts)]

# Create final map
p <- ggplot() +
  geom_sf(data = merged, aes(fill = Seasonality), 
          color = "gray", linewidth = 0.3) +
  geom_sf(data = boundaries, fill = NA, 
          color = "black", linewidth = 0.8) +
  scale_fill_manual(
    values = colors_filtered,
    labels = legend_labels,
    name = "Classification"
  ) +
  labs(title = "Malaria Seasonality Classification") +
  theme_void() +
  theme(
    plot.title = element_text(hjust = 0.5, size = 14, face = "bold"),
    legend.position = "right",
    legend.background = element_rect(fill = "white", color = "black")
  )

print(p)
```

::: {.callout-note title="Output" icon="false"}
```{R}
#| message: false
#| echo: false
#| eval: true

merged$Seasonality[is.na(merged$Seasonality)] <- "No data"

colors <- c(
  "Seasonal" = "#47B5FF",
  "Not Seasonal" = "#FFB3BA",
  "No data" = "white"
)

boundaries <- merged |>
  dplyr::group_by(FIRST_DNAM) |>
  dplyr::summarise(geometry = sf::st_union(geometry))

merged$Seasonality <- factor(
  merged$Seasonality, 
  levels = c("Seasonal", "Not Seasonal", "No data")
)

cat_counts <- table(merged$Seasonality)
cat_counts <- cat_counts[cat_counts > 0]

legend_labels <- paste0(names(cat_counts), " (", cat_counts, ")")
names(legend_labels) <- names(cat_counts)

colors_filtered <- colors[names(colors) %in% names(cat_counts)]

p <- ggplot() +
  geom_sf(data = merged, aes(fill = Seasonality), 
          color = "gray", linewidth = 0.3) +
  geom_sf(data = boundaries, fill = NA, 
          color = "black", linewidth = 0.8) +
  scale_fill_manual(
    values = colors_filtered,
    labels = legend_labels,
    name = "Classification"
  ) +
  labs(title = "Malaria Seasonality Classification") +
  theme_void() +
  theme(
    plot.title = element_text(hjust = 0.5, size = 14, face = "bold"),
    legend.position = "right",
    legend.background = element_rect(fill = "white", color = "black")
  )

print(p)
```
:::

**To adapt the code:**
- **Lines 6-9**: Modify colors for seasonal and non-seasonal categories to match your organization's style
- **Lines 13-15**: Change grouping variable (`FIRST_DNAM`) if you want boundaries at a different admin level
- **Line 44**: Update map title as needed

This code creates the final classification map through several steps: First, it replaces any missing seasonality values with "No data" to ensure all locations appear on the map. Second, it defines a color scheme where Seasonal areas are blue, Not Seasonal areas are light pink, and any areas with no data are white. Third, it creates district-level boundaries by dissolving chiefdom boundaries, which will be overlaid in black to help viewers orient themselves geographically. Fourth, it converts the Seasonality variable to a factor with defined levels for proper legend ordering. Fifth, it counts locations in each category and creates legend labels showing both the classification and the count (for example, "Seasonal (89)" means 89 locations are classified as seasonal). Sixth, it filters the color palette to only include categories that exist in the data. Finally, it creates the map with two layers: filled chiefdom polygons colored by classification and district boundaries in black for reference. The resulting map clearly shows which areas meet WHO criteria for seasonal interventions and can be directly used for program planning discussions with the SNT team.

## Python
:::

## Summary

This analysis provides a comprehensive framework for determining SMC eligibility based on:

1. **Seasonality assessment**: Using time-block analysis to identify consistent seasonal patterns
2. **Peak period identification**: Determining optimal intervention timing through rolling window analysis

::: {#bottom-section}

## Full code

**Find the full code for seasonality stratification below.**

<div id="bottom-section"></div>


::: {.panel-tabset}
## R
```r
# ============================
# Step 1: Import packages and data
# ============================
if (!requireNamespace("pacman", quietly = TRUE)) install.packages("pacman")

pacman::p_load(
  readxl, dplyr, openxlsx, lubridate, ggplot2, readr, stringr, 
  here, tidyr, gridExtra, knitr, writexl, sf
)

# File path
file_path <- here::here("english/data_r/modeled", "chirps_data_2015_2023_lastest.xls")

# Load your data
data <- readxl::read_excel(file_path)


# ============================
# Step 2: Configure analysis parameters
# ============================
year_column <- "Year"
month_column <- "Month"
value_column <- "mean_rain"
admin_columns <- c("FIRST_DNAM", "FIRST_CHIE")

analysis_start_year <- 2015
analysis_start_month <- 1
seasonality_threshold <- 60

#detailed_output <- "detailed_seasonality_results.xlsx"
#yearly_output <- "yearly_analysis_summary.xlsx"
#location_output <- "location_seasonality_summary.xlsx"


# ============================
# Step 3: Prepare data for analysis
# ============================
required_cols <- c(year_column, month_column, value_column, admin_columns)
missing_cols <- required_cols[!required_cols %in% colnames(data)]
if (length(missing_cols) > 0) {
  stop(paste("Missing columns:", paste(missing_cols, collapse = ", ")))
}

filtered_data <- data |>
  dplyr::filter(
    !is.na(!!sym(year_column)) & 
    !is.na(!!sym(month_column)) & 
    !!sym(year_column) >= analysis_start_year
  ) |>
  dplyr::mutate(Month = as.numeric(!!sym(month_column)))

if (length(admin_columns) == 1) {
  filtered_data$admin_group <- filtered_data[[admin_columns[1]]]
} else {
  filtered_data <- filtered_data |>
    dplyr::mutate(
      admin_group = paste(!!!syms(admin_columns), sep = " | ")
    )
}

available_years <- sort(unique(filtered_data[[year_column]]))
data_span_years <- length(available_years)

if (data_span_years < 6) {
  stop(paste(
    "Insufficient data: Analysis requires at least 6 years of data, but only", 
    data_span_years, "years found."
  ))
}

num_complete_years <- data_span_years - 1
total_num_blocks <- num_complete_years * 12


# ============================
# Step 4: Generate rolling time blocks
# ============================
month_names <- c("Jan", "Feb", "Mar", "Apr", "May", "Jun",
                 "Jul", "Aug", "Sep", "Oct", "Nov", "Dec")

blocks <- data.frame()
current_year <- analysis_start_year
current_month <- analysis_start_month

for (i in 1:total_num_blocks) {
  # 4-month period
  start_4m_year <- current_year
  start_4m_month <- current_month
  end_4m_year <- current_year
  end_4m_month <- current_month + 3
  
  if (end_4m_month > 12) {
    end_4m_year <- end_4m_year + 1
    end_4m_month <- end_4m_month - 12
  }

  # 12-month period  
  start_12m_year <- current_year
  start_12m_month <- current_month
  end_12m_year <- current_year
  end_12m_month <- current_month + 11
  
  if (end_12m_month > 12) {
    end_12m_year <- end_12m_year + 1
    end_12m_month <- end_12m_month - 12
  }

  # Create date range label
  date_range <- paste0(
    month_names[start_4m_month], " ", start_4m_year, "-",
    month_names[end_4m_month], " ", end_4m_year
  )
  
  # Store block information
  blocks <- rbind(blocks, data.frame(
    block_number = i,
    start_4m_year = start_4m_year,
    start_4m_month = start_4m_month,
    end_4m_year = end_4m_year,
    end_4m_month = end_4m_month,
    start_12m_year = start_12m_year,
    start_12m_month = start_12m_month,
    end_12m_year = end_12m_year,
    end_12m_month = end_12m_month,
    date_range = date_range
  ))

  # Move to next month
  current_month <- current_month + 1
  if (current_month > 12) {
    current_month <- 1
    current_year <- current_year + 1
  }
}


# ============================
# Step 5: Calculate seasonality for each block
# ============================
detailed_results <- data.frame()
admin_groups <- unique(filtered_data$admin_group)

for (admin_unit in admin_groups) {
  unit_data <- filtered_data |> dplyr::filter(admin_group == admin_unit)
  
  for (i in 1:nrow(blocks)) {
    block <- blocks[i, ]
    unit_data_ym <- unit_data[[year_column]] * 12 + unit_data$Month
    
    # 4-month window
    start_4m_ym <- block$start_4m_year * 12 + block$start_4m_month
    end_4m_ym <- block$end_4m_year * 12 + block$end_4m_month
    data_4m <- unit_data |> dplyr::filter(unit_data_ym >= start_4m_ym & unit_data_ym <= end_4m_ym)
    total_4m <- sum(data_4m[[value_column]], na.rm = TRUE)

    # 12-month window
    start_12m_ym <- block$start_12m_year * 12 + block$start_12m_month
    end_12m_ym <- block$end_12m_year * 12 + block$end_12m_month
    data_12m <- unit_data |> dplyr::filter(unit_data_ym >= start_12m_ym & unit_data_ym <= end_12m_ym)
    total_12m <- sum(data_12m[[value_column]], na.rm = TRUE)

    # Percentage & flag
    percent_seasonality <- ifelse(total_12m > 0, (total_4m / total_12m) * 100, 0)
    is_seasonal <- as.numeric(percent_seasonality >= seasonality_threshold)

    # Build result row
    result_row <- data.frame(
      Block = i, DateRange = block$date_range,
      Total_4M = total_4m, Total_12M = total_12m,
      Percent_Seasonality = round(percent_seasonality, 2),
      Seasonal = is_seasonal,
      stringsAsFactors = FALSE
    )

    if (length(admin_columns) > 1) {
      admin_parts <- strsplit(admin_unit, " \\| ")[[1]]
      for (j in seq_along(admin_columns)) {
        result_row[[admin_columns[j]]] <- ifelse(j <= length(admin_parts), admin_parts[j], NA)
      }
    } else {
      result_row[[admin_columns[1]]] <- admin_unit
    }

    detailed_results <- rbind(detailed_results, result_row)
  }
}

# Preview results
knitr::kable(head(detailed_results), caption = "Preview of Detailed Block Results")


# ============================
# Step 6: Generate yearly summary
# ============================
detailed_results$StartYear <- sapply(detailed_results$DateRange, function(x) {
  parts <- strsplit(x, "-")[[1]]
  first_part <- trimws(parts[1])
  as.numeric(substr(first_part, nchar(first_part) - 3, nchar(first_part)))
})

yearly_summary <- detailed_results |>
  dplyr::group_by(dplyr::across(dplyr::all_of(admin_columns)), StartYear) |>
  dplyr::summarise(
    Year = dplyr::first(StartYear),
    SeasonalCount = sum(Seasonal, na.rm = TRUE),
    total_blocks_in_year = 12,
    at_least_one_seasonal_block = as.numeric(SeasonalCount > 0),
    .groups = 'drop'
  ) |>
  dplyr::mutate(
    year_period = paste0(
      "(Jan ", Year, "-Apr ", Year, ", Dec ", Year, "-Mar ", Year + 1, ")"
    )
  ) |>
  dplyr::select(
    Year, dplyr::all_of(admin_columns),
    year_period, total_blocks_in_year, at_least_one_seasonal_block
  ) |>
  dplyr::arrange(Year, dplyr::across(dplyr::all_of(admin_columns)))

# Preview summary
knitr::kable(tail(yearly_summary, 10), caption = "Yearly Seasonality Summary (Last 10 rows)")


# ============================
# Step 7: Location-level seasonality classification
# ============================
location_summary <- yearly_summary |>
  dplyr::group_by(dplyr::across(dplyr::all_of(admin_columns))) |>
  dplyr::summarise(
    SeasonalYears = sum(at_least_one_seasonal_block, na.rm = TRUE),
    TotalYears = dplyr::n(),
    .groups = 'drop'
  ) |>
  dplyr::mutate(
    Seasonality = ifelse(SeasonalYears == TotalYears, "Seasonal", "Not Seasonal")
  ) |>
  dplyr::arrange(dplyr::across(dplyr::all_of(admin_columns)))

# Preview classification
knitr::kable(head(location_summary, 10), caption = "Location Seasonality Classification")


# ============================
# Step 8: Merge data for visualization
# ============================
file_path <- here::here("english/data_r/shapefiles", "Chiefdom2021.shp")
file_path_2 <- here::here("english/library/stratification/other", "final_SMC_eligibility.xlsx")

spatial_data <- sf::st_read(file_path)
category_data <- readxl::read_excel(file_path_2)

merged <- spatial_data |>
  dplyr::left_join(category_data, by = c("FIRST_DNAM", "FIRST_CHIE"))


# ============================
# Step 9: Map for years of seasonal peak
# ============================
merged$category <- as.character(merged$SeasonalYears)
merged$category[is.na(merged$category)] <- "0"

category_colors <- c(
  "0" = "gray80",
  "1" = "#4E79A7", "2" = "#F28E2B", "3" = "#E15759",
  "4" = "#76B7B2", "5" = "#59A14F", "6" = "#EDC948",
  "7" = "#4E79A7", "8" = "#AF7AA1"
)

merged$category <- factor(merged$category, levels = as.character(0:8))

cat_counts <- table(merged$category)
cat_counts <- cat_counts[cat_counts > 0]

legend_labels <- paste0(names(cat_counts), " (", cat_counts, ")")
names(legend_labels) <- names(cat_counts)

category_colors_filtered <- category_colors[names(category_colors) %in% names(cat_counts)]

p <- ggplot(merged) +
  geom_sf(aes(fill = category), color = "white", size = 0.2) +
  scale_fill_manual(values = category_colors_filtered, labels = legend_labels, name = "Category") +
  theme_minimal() + theme_void() +
  theme(
    legend.position = "right",
    plot.title = element_text(hjust = 0.5, size = 14, face = "bold"),
    panel.grid = element_blank()
  ) +
  labs(title = "Map by Category (0-8)")

print(p)

### Seasonality plot

# Replace NA with "No data" if needed
merged$Seasonality[base::is.na(merged$Seasonality)] <- "No data"

# Assign colors
colors <- c(
  "Seasonal" = "#47B5FF",      # Blue
  "Not Seasonal" = "#FFB3BA",  # Light pink
  "No data" = "white"
)

# Boundaries for FIRST_DNAM 
boundaries <- merged |>
  dplyr::group_by(FIRST_DNAM) |>
  dplyr::summarise(geometry = sf::st_union(geometry))

# Convert to factor
merged$Seasonality <- base::factor(
  merged$Seasonality, 
  levels = c("Seasonal", "Not Seasonal", "No data")
)

# Count categories (excluding zero counts) 
cat_counts <- base::table(merged$Seasonality)
cat_counts <- cat_counts[cat_counts > 0]

# Create labels with counts
legend_labels <- base::paste0(base::names(cat_counts), " (", cat_counts, ")")
base::names(legend_labels) <- base::names(cat_counts)

# Filter colors to only include categories that exist
colors_filtered <- colors[base::names(colors) %in% base::names(cat_counts)]

# Plot
p <- ggplot2::ggplot() +
  ggplot2::geom_sf(data = merged, ggplot2::aes(fill = Seasonality), 
                   color = "gray", linewidth = 0.3) +
  ggplot2::geom_sf(data = boundaries, fill = NA, 
                   color = "black", linewidth = 0.8) +
  ggplot2::scale_fill_manual(
    values = colors_filtered,
    labels = legend_labels,
    name = "Seasonality"
  ) +
  ggplot2::labs(title = "Malaria Seasonality Classification") +
  ggplot2::theme_void() +
  ggplot2::theme(
    plot.title = ggplot2::element_text(hjust = 0.5, size = 14, face = "bold"),
    legend.position = "right",
    legend.background = ggplot2::element_rect(fill = "white", color = "black"),
    legend.key = ggplot2::element_rect(color = "black")
  )

# Display plot
base::print(p)
```

**To adapt the code:**

- **Lines 3-5**: File paths for spatial data and SMC eligibility can be customized for your project structure
- **Lines 7-9**: Join key columns (FIRST_DNAM, FIRST_CHIE) should match your shapefile attributes
- **Lines 11-27**: Category colors and mapping can be adjusted based on your data ranges
- **Lines 29-64**: Seasonality classification colors and legend styling can be customized as needed

## Python
:::

::: {#bottom-section}
:::

## Full code

**Find the full code script for seasonality analysis below.**

```{r}
#| label: showing get current document path
#| echo: false
#| eval: true
#| message: true
#| warning: false
qmd_page_path <- here::here(
    "english/library/stratification/seasonality.qmd"
)

# now build the full script
build_fullcode_scripts(
    quarto_path = qmd_page_path,
    chunk_label = "fullcode")
```

::: {.panel-tabset}
## R

```{r}
#| label: showing full r code
#| echo: false
#| eval: true
#| results: asis
show_full_code(qmd_page_path, "r")
```

## Python

```{r}
#| label: showing full python code
#| echo: false
#| eval: true
#| results: asis
show_full_code(qmd_page_path, "python")
```

:::
