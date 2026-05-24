# Decode-TN-Elections-2026
## The objective was to analyze Tamil Nadu Assembly Election 2026 data using only Election Commission data and uncover meaningful stories.

The focus was not political commentary, but fact-based analytical storytelling using:
- turnout trends,
- regional mandate shifts,
- vote share movement,
- and constituency-level patterns.

## Video Walkthrough

[Watch Presentation Video on Loom](https://www.loom.com/share/23d46da4538247ec82a5f465e8b20d45)

[Watch Presentation Video on Youtube](https://youtu.be/VDZeRosjFcg)

## Live Dashboard

[Explore Live Dashboard](https://app.powerbi.com/view?r=eyJrIjoiNGIzYjkyODYtNmU2NC00MDMwLTk4ZGQtNzY5NGNkN2YwZjkwIiwidCI6ImM2ZTU0OWIzLTVmNDUtNDAzMi1hYWU5LWQ0MjQ0ZGM1YjJjNCJ9)

## Reproduction Steps

Follow the steps below to reproduce this project:

### Clone the Repository

The project was developed using Power BI with constituency-level Tamil Nadu election datasets for 2021 and 2026.

---

### 1. Data Collection

The following datasets were prepared before importing into Power BI:

- `tn_2021_results.csv`
- `tn_2026_results.csv`
- `constituency_master.csv`

Additional 2026 turnout-related data was collected from the official Tamil Nadu Election Commission website because the original `2026_results` dataset did not contain complete turnout-related columns.

Official Election Commission Form 20 constituency-level result data was used to obtain:
- Total Electors
- Total Votes Polled
- Constituency-level turnout information

---

### 2. Data Enrichment Using Excel

Before importing into Power BI:

- Election Commission turnout data was exported as CSV.
- Excel `XLOOKUP()` was used to map constituency-level turnout data to the existing `tn_2026_results` dataset.
- Constituency names and AC numbers were used as matching keys.

This enrichment step enabled:
- Turnout percentage calculations
- Turnout band analysis
- Comparative turnout analysis between 2021 and 2026

---

### 3. Data Cleaning & Validation

After loading the datasets into Power BI:

The following validation steps were performed:

- Removed / checked extra spaces in common columns
- Validated constituency naming consistency
- Checked for duplicate rows
- Corrected data types for:
  - AC Number
  - Votes
  - Turnout %
  - Party columns
- Verified relationship keys across all tables

---

### 4. Data Modeling in Power BI

The folder containing all datasets was connected directly to Power BI.

Relationships were established between:
- Constituency master table
- 2021 election results
- 2026 election results
- Party master table
- Turnout aggregation tables

Two additional aggregation tables were created:
- `TN_2021_Electors_vs_Votes`
- `TN_2026_Electors_vs_Votes`

These tables were specifically created to:
- Aggregate constituency-level electors
- Aggregate total votes polled
- Compute turnout percentages
- Support turnout trend analysis

The `2021_results` and `2026_results` tables retained party-level constituency data for:
- Seat conversion analysis
- Vote share movement
- Regional political shifts

---

### 5. Dashboard Development

A 4-page interactive Power BI report was designed covering:

1. Turnout Story
2. Geographic Story
3. Vote Share Story
4. Executive Summary

Key dashboard features include:
- Interactive filtering
- Regional analysis
- Dynamic storytelling visuals
- KPI cards
- Conditional formatting
- Bookmark-based visual switching
- Field parameters for dynamic metric selection

---

### 6. DAX & Analytical Logic

DAX measures were created for:

- Dynamic chart titles
- Turnout calculations
- Vote share %
- Seat conversion metrics
- Regional swing analysis
- KPI indicators
- Conditional formatting logic

Additional analytical calculations included:
- Turnout band categorization
- Comparative election trend analysis
- Regional aggregation metrics

---

### 7. Presentation Deck Preparation

An executive-style presentation deck was prepared to summarize the dashboard findings in a storytelling format.

Presentation structure:
1. Election Outcome Snapshot
2. Regional Political Shifts
3. Geographic Realignment
4. Vote Share Movement
5. Turnout Influence Analysis
6. Key Election Insights
7. Editorial Recommendations
8. Data Limitations & Methodology Notes

The deck was designed using:
- Infographic-first storytelling
- Minimal cognitive load layouts
- Consistent party color hierarchy
- Executive dashboard presentation principles
## Tools & Technologies

- Power BI
- DAX
- Power Query
- Microsoft Excel
- Election Commission Data
  
---
## Data Sources

- Tamil Nadu Election Commission
- Election Commission Form 20 constituency-level result data
- Public constituency-level election datasets

---

## Important Note

This project was created for analytical storytelling and educational purposes.

The analysis identifies observable electoral patterns and correlations, but does not establish direct causation or political endorsement.

