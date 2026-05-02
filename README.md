Patient Data Analysis Dashboard
A Power BI project built to make sense of patient data across demographics, clinical trends, and operational healthcare metrics. The goal was to give healthcare administrators and medical staff a single place to look at their data without having to dig through spreadsheets.

Dashboard Previews
Overview Page
A high-level snapshot of the patient population — who's coming in, when, and in what volumes. This is the first page most stakeholders will land on.
<img width="1473" height="832" alt="image" src="https://github.com/user-attachments/assets/996d448c-e0bf-42f2-b344-fb3219ddc907" />
Clinical Metrics Page
Where things get more granular. This page breaks down health outcomes, admission rates, and segment-level trends over time. Useful for department leads who need more than just totals.
<img width="1483" height="829" alt="image" src="https://github.com/user-attachments/assets/8bb7c114-21d1-49d4-ab64-d04c9e6445f2" />
What's in the Dashboard
Interactive Filtering
Slicers let you cut the data by date range, patient demographics, and department. Most of the visuals respond to these filters simultaneously, so you're not jumping between pages to answer a single question.
Clinical KPIs
Patient volume, admission rates, and outcome metrics are tracked at the top level so they're always visible regardless of which filters are active.
Trend Analysis
Month-over-month and year-over-year views for the metrics that matter. Useful for spotting patterns that don't show up in aggregate numbers.

Repository Structure
patient-data-analysis/
│
├── Patient data.pbix          # Main Power BI report file
│
├── Data/                      # Raw source data
│   ├── patients.csv
│   └── clinical_events.xlsx
│
├── Backgrounds/               # Custom background images used in the report
│
└── assets/                    # Images used in this README

Data Model Notes
The data model connects patient records to clinical events through a shared patient ID. Relationships are set to single-direction filtering to keep query performance reasonable on larger datasets.
The custom backgrounds in the Backgrounds/ folder are linked directly inside the .pbix file. If you move those files after cloning, you'll need to re-point the background images in the report's Format pane.
Tools used: Power BI Desktop

Getting Started
1. Clone the repository
bashgit clone https://github.com/atharvakadam-7/patient-data-analysis.git
2. Install Power BI Desktop
If you don't already have it, download the latest version from Microsoft's official site. The free version works fine for everything in this project.
3. Open the report
Open Patient data.pbix in Power BI Desktop.
4. Fix data source paths if needed
Power BI stores absolute file paths, so if the data doesn't load on your machine:

Go to Transform Data → Data Source Settings
Update the file paths to point to the files in the /Data folder

This is a one-time fix after cloning.

Notes

The .pbix file includes the data model, all visuals, and the report layout. You don't need anything else to explore the report locally.
The raw files in /Data are there in case you want to inspect the source data or rebuild the model from scratch.
If you want to connect this to a live data source rather than flat files, the query structure in Power Query Editor is straightforward to adapt.
