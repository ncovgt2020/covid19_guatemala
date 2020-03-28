# Dataset of patients infected with COVID-19 in Guatemala

Description: This is a ***non-official*** dataset, compiled from oficial sources and news reports, of the confirmed cases of corona virus infection in Guatemala.

Disclaimer: This is a dataset put together by volunteers. We make a best effort to collect reliable and truthfull information, but do not provide any guarantees.

Purpose: 
- Recollect reliable and granular information from official sources or news reports on patients infected with corona virus COVID-19
- That others use this dataset to generate and publish their own visualizations and analysis, and inform the rest
- Leave a record on the evolultion of corona virus COVID-19 in Guatemala 
- Combat misinformation 

***License: [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)***


# Field Description

## patients.csv

Contains information available on each confirmed case of corona virus in Guatemala.

- id: patient unique identifier (numerical, integer)
- sex: m: male, f: female, x: unknown (string)
- birth_date: yy-mm-dd, birth year. Calculated as follows: birth_date = 2020 - age. This means that day and month are not recorded and default to 01-01. (string or empty field)
- age: age of the patient(numerical, integer), -99: unknown
- country: origin country/nationality (string or empty field)
- department: region where patient's most activity ocurred ('department' is similar to 'state' in US or 'province' in China)(string)
- illness: known previous medical background (string) or 'unknown'
- group: relation to an especific infection group, -99: unknown or not apply (numerical, integer)
	- 1: march 11th flight, aeromexico
	- 2: march 6th flight, iberia
	- 3: direct or indirect contact with patient id 2 (first fatality)
	- 4: rescue flight march 26th, from Spain to Guatemala
- infection_cause: reason for infection (travel, relative visit, hospital visit, contact with patient, etc) (string)
- infected_by: id of patient from whom infection was transmitted, -99: unknown (numerical, integer)
- confirmation_date: yy-mm-dd date when infection was confirmed, or empty field if unknown (string)
- recovery_date: yy-mm-dd date when patient recovered, or empty field if unknown (string)
- deceased_date: yy-mm-dd date when patient deceased, or empty field if unknown (string)
- status: 0: isolated  1: recovered  2: deceased (numerical, integer)
- source: link to the information source from wayback machine. When various sources were used, they are separated by asterisk "*" (see below) (string)

### [Wayback Machine](https://archive.org/web/)?

Is an organization that stores the internet. To this project, serves two purposes:
1) That the information source is permanently stored
2) Prevent malicious actors from spreading dangerous content or misinformation through this project

To create a link using wayback machine:

a) Go to https://archive.org/web/:

b) Copy the source url and paste it in the field "Save Page Now"

c) Click the button "Save Page"

d) This will store the url and load a new webpage with the source content. Copy the link to the new webpage. This should start with https://web.archive.org: 
	- Example: https://web.archive.org/web/20200315072155/https://www.prensalibre.com/guatemala/comunitario/coronavirus-alejandro-giammattei-confirma-el-primer-caso-de-covid-19-en-guatemala/

Contact: Use the  [issues](https://github.com/ncovgt2020/ncovgt2020/issues) tab to leave suggestions/comments, notify of new cases. Make a pull request to contribute. Write an email to ncovgt2020[arroba]hotmail.com.
