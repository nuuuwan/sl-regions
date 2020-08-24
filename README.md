# Region Data

Data is stored as CSVs

Contains data about the following regions:
* Country
* Provinces
* Electoral Districts (ED)
* Districts
* Divisional Secretariat Divisions (DSD)
* Polling Divisions (PD)
* Grama Niladari Divisions (GND)

For each region, there is a table. The table contains the following information:
* Region ID
* Region Name
* All Parent IDs

## Child-Parent relationships

Region Type A is a child of Region Type B iff for any instance of A, there is exactly one instance of B that completely contains it.

E.g.

* District is a child of ED. Because all districts are contained in some ED.
* ED is not a child of District. The Jaffna ED contains two Districts (Jaffna and Kilinochchi), and hence is not contained in a single one.
* DSD is not a child of PD. While some PDs contain several DSD, some DSDs (in the Colombo and Kandy EDs) are contained within DSDs and are collections of GNDs.

All Child -> Parent relationships are as follows:

* Country -> None
* Province -> Country
* ED -> Province, Country
* District -> ED, Province, Country
* DSD -> District, ED, Province, Country
* PD -> District, ED, Province, Country
* GND -> PD, DSD, District, ED, Province, Country

## ID Formats
