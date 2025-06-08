# Netflix Content Analysis Report

---

## 1. Project Context

This project aims to analyze the Netflix content catalog to better understand genre distribution, content availability by country, and seasonality of additions.  
The main tool used is Power BI, enabling the creation of an interactive and visual dashboard.

---

## 2. Dataset Description

- 8,807 Netflix titles (movies and TV shows)  
- Key columns: `type` (Movie, TV Show), `title`, `listed_in` (genres), `country`, `date_added`, `release_year`, `rating`, `duration`  
- Presence of missing values in some columns (`director`, `cast`, `country`)  
- Raw data imported as CSV into Power BI

---

## 3. Data Preparation and Cleaning in Power BI

- Imported the raw CSV file into Power BI Desktop  
- Converted `date_added` column to Date type  
- Created two calculated columns:  
  - `added_year` = year of addition  
  - `added_month` = month of addition  
- Split `listed_in` column to separate multiple genres into distinct rows (split by delimiter `,` then split into rows)  
- Split `country` column to handle titles available in multiple countries  
- Cleaned spaces and null values in key columns  
- Managed data misalignment due to line breaks in CSV (e.g., manual correction in Power Query)

---

## 4. Visualizations Created

### Page 1 – Overview

- **Top Genres (Bar Chart):** Shows most frequent genres in the catalog, sorted by title count.  
- **Number of Countries (KPI Card):** Distinct count of countries where Netflix is available.  
- **Countries with Most Content (Bar Chart):** Ranking of countries by number of available titles.  
- **Movies vs TV Shows Proportion (Pie Chart):** Distribution of content types.

### Page 2 – Dominant Genre by Country

- **Heatmap or Matrix:** Displays most frequent genre per country, highlighting regional preferences.

### Page 3 – Seasonality of Additions

- **Grouped Bar or Line Chart:** Number of titles added by month, distinguished by year (`added_year` and `added_month`) to detect seasonal trends.

### Bonus Pages

- **Content Type Classification (Stacked Bar Chart):** Comparison of movies and series by genre, showing category dominance.  
- **Geographical Distribution (Bing Map):** Interactive map showing Netflix content distribution by country and volume.  
- **Additions Evolution by Country and Year (Line Chart):** Temporal analysis of content volume added per country, revealing trends and peaks.

---

## 5. Key Insights

- "Drama," "Comedy," and "Documentary" genres dominate the Netflix catalog.  
- Netflix is available in over 70 countries, with strong content concentration in the United States.  
- Genre preferences vary significantly by region, useful for local strategy.  
- Content additions follow seasonal patterns with identifiable peaks.  
- Bonus analyses provide deeper understanding of content typology and geographic dynamics.

---

## 6. Netflix Branding and Design

- Used official Netflix colors: red (#E50914) and black to respect brand identity.  
- Integrated Netflix logo in the dashboard.  
- Selected simple, readable fonts (Segoe UI, Arial).  
- Implemented interactive filters and slicers for smooth user experience.

---

## 7. Navigation and Recommendations

- Use slicers to filter by genre, country, year, or rating.  
- Explore heatmaps to understand country and genre dynamics.  
- Visualize seasonality to plan releases and marketing strategies.

---

## 8. Conclusion

This project demonstrates comprehensive use of Netflix data with Power BI, combining data cleaning, advanced visualizations, and strategic analysis.  
It showcases the ability to transform complex datasets into actionable business insights.

---

*End of Report*