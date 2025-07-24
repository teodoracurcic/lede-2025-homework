# Homework: Interacting with Undocumented Airbnb API

This assignment was completed as part of coursework for the [Lede Program at Columbia Journalism School](https://ledeprogram.com).  
The goal was to explore and interact with an undocumented Airbnb API endpoint using HTTP requests, reverse-engineering techniques, and parameter customization.

The project focused on retrieving estimated earnings for different rental configurations (based on bedroom count) and locations using a hidden API used on Airbnb’s hosting page.

## Notebook

**File**: `undocumented-api-hw.ipynb`  
This notebook includes the entire process: identifying a hidden API endpoint via browser dev tools, reconstructing request headers and query parameters, looping through combinations of addresses and bedroom counts, and parsing JSON responses into structured data.

## API Targeted

- Airbnb internal endpoint exposed via [airbnb.com/host/homes](https://www.airbnb.com/host/homes)  
  The API provides estimated monthly and nightly earnings for listings in a given area, based on room configuration and listing type.

## Data Collected

- **Address** (search query location)  
- **Number of bedrooms**  
- **Estimated monthly earnings**  
- **Estimated nightly earnings**

Each combination of address and bedroom count was queried programmatically, and results were compiled into a DataFrame for analysis and export.

## Tools & Techniques

- `requests` — for sending GET requests with custom headers and parameters  
- `time.sleep()` — to manage pacing and avoid being rate-limited  
- `json` — for parsing API responses  
- `pandas` — for organizing and exporting the final dataset  

The project demonstrates how undocumented APIs can be identified and safely leveraged using careful inspection and controlled automation.