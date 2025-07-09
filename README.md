
Certainly! Based on the previously shared data regarding the **Top 10 Most Used Programming Languages** and **Top 10 Most Wanted Programming Languages**, here's a sample **discussion/analysis** you can use in a report or presentation:

---

### 📊 Discussion: Top Programming Languages from the Developer Survey

#### 1. **PostgreSQL Leading Across Both Metrics**

PostgreSQL stands out as the most **used** and **wanted** database technology among developers. With over 25,000 mentions in usage and topping the "wanted" list, this reflects PostgreSQL's strong reputation for reliability, feature richness, and open-source development. It has become the go-to choice for many modern applications, especially in startups, analytics, and cloud-native environments.

#### 2. **Classic Relational Databases Still Dominate**

Despite the rise of NoSQL and cloud-native databases, **relational databases** such as MySQL, SQLite, Microsoft SQL Server, and Oracle remain heavily used. Their enduring popularity can be attributed to decades of integration into enterprise systems, strong tooling support, and well-understood performance characteristics.

* **MySQL** is still the second most used, reflecting its prevalence in web development, especially in LAMP stacks.
* **SQLite** ranks third, likely due to its lightweight nature and widespread use in mobile apps and embedded systems.

#### 3. **MongoDB and Redis – Popular NoSQL Options**

**MongoDB**, as a document-based NoSQL database, is holding a strong position in both usage and demand. It's particularly favored in flexible, agile web development. **Redis**, although more niche, remains critical for high-performance use cases like caching and message brokering.

#### 4. **Emerging Interest in Elastic and DynamoDB**

**Elasticsearch** and **DynamoDB** appear in the top 10, showing growing interest in **search and scalable cloud-based storage**. Elasticsearch is widely used for log analysis, monitoring, and full-text search, while DynamoDB’s inclusion reflects AWS’s influence in production infrastructure.

#### 5. **Oracle – Still Present but Losing Mindshare**

While **Oracle** appears in the usage top 10, it doesn’t rank among the most wanted. This discrepancy indicates that while legacy systems still depend on Oracle, developers do not see it as a desirable choice for new projects—likely due to cost, complexity, or licensing concerns.

#### 6. **Trends Toward Open Source and Cloud-Native**

The overall trend suggests developers are leaning toward **open-source, flexible, and cloud-friendly** tools. PostgreSQL, Redis, and MongoDB all benefit from active communities and modern deployment options like Docker and Kubernetes compatibility.

---

### 📈 Summary Insights:

* **PostgreSQL** dominates both current usage and future interest.
* Traditional relational databases are still deeply entrenched.
* **Cloud-native and NoSQL** solutions are gaining more attention and usage.
* There is a visible gap between legacy tools (like Oracle) and what developers want to work with moving forward.

These insights can guide both individual developers and organizations in choosing tech stacks that align with current trends and future developer satisfaction.

---

Let me know if you’d like to visualize this discussion with charts or graphs, or adapt it for a blog post, presentation, or internal report.





https://eu1.ca.analytics.ibm.com/bi/?perspective=dashboard&pathRef=.my_folders%2Fcoding_survey&action=view&mode=dashboard&subView=model00000197e52b1926_00000000
cognos capstone ibm dashboard

Okay, here's the content presented as normal text using bullet points:

This Jupyter Notebook details Lab 2: Data Wrangling and Exploratory Data Analysis (EDA), part of a larger project on SpaceX Falcon 9 First Stage Landing Prediction.

The primary goals for this lab are:
 To perform exploratory data analysis to discover patterns within the dataset.
 To determine the appropriate labels (1 for successful landing, 0 for unsuccessful) for training supervised machine learning models.
 The estimated completion time for this lab is 60 minutes.

The process follows these steps:

 Environment Setup:
     Installation of necessary Python libraries (`pandas`, `numpy`).
     Importation of `pandas` and `numpy` into the notebook.

 Data Loading:
     The `dataset_part_1.csv` file is loaded into a pandas DataFrame.
     The first 10 rows of the loaded DataFrame are displayed for initial inspection.

 Initial Data Exploration:
     Calculation of the percentage of missing values for each attribute (column) in the DataFrame.
     Identification of the data types (e.g., numerical, categorical, boolean) for all columns in the DataFrame.

Analyze Launch Sites:
     The `value_counts()` method is applied to the `LaunchSite` column to count the number of launches from each unique site (e.g., Cape Canaveral SLC 40, Vandenberg SLC 4E, Kennedy Space Center LC 39A).

Analyze Orbit Occurrences:
     The `value_counts()` method is used on the `Orbit` column to determine the frequency of each orbit type (e.g., LEO, VLEO, GTO, SSO, ISS). Contextual explanations for various orbit types are provided.

Analyze Mission Outcomes:
     The `value_counts()` method is applied to the `Outcome` column to tally the occurrences of different landing outc-omes (e.g., True ASDS, None None, True RTLS, False Ocean).
     A set named `bad_outcomes` is explicitly defined to include all outcomes that represent an unsuccessful first stage landing (e.g., 'None ASDS', 'False RTLS', 'False Ocean', 'None None', 'False ASDS').

Create Landing Outcome Label:
     A new list, `landing_class`, is generated.
     For each outcome in the DataFrame's `Outcome` column, `0` is appended to `landing_class` if the outcome is in the `bad_outcomes` set (unsuccessful landing).
     Otherwise, `1` is appended (successful landing).
     This `landing_class` is intended to be added as a 'Class' column to the DataFrame, serving as the binary target variable for classification models.

The lab concludes with the dataset prepared, having undergone data wrangling and the creation of the essential target variable for subsequent machine learning model training.



Okay, here's the content presented as normal text using bullet points:

This Jupyter Notebook details *Lab 2: Data Wrangling and Exploratory Data Analysis (EDA)**, part of a larger project on **SpaceX Falcon 9 First Stage Landing Prediction**.

The primary goals for this lab are:

* To determine the appropriate labels (1 for successful landing, 0 for unsuccessful) for training supervised machine learning models.
* The estimated completion time for this lab is 60 minutes.
* To perform exploratory data analysis to discover patterns within the dataset.


The process follows these steps:

* **Environment Setup:**
    * Installation of necessary Python libraries (`pandas`, `numpy`).
    * Importation of `pandas` and `numpy` into the notebook.

* **Data Loading:**
    * The `dataset_part_1.csv` file is loaded into a pandas DataFrame.
    * The first 10 rows of the loaded DataFrame are displayed for initial inspection.

* **Initial Data Exploration:**
    * Calculation of the percentage of missing values for each attribute (column) in the DataFrame.
    * Identification of the data types (e.g., numerical, categorical, boolean) for all columns in the DataFrame.

* **Task 1: Analyze Launch Sites:**
    * The `value_counts()` method is applied to the `LaunchSite` column to count the number of launches from each unique site (e.g., Cape Canaveral SLC 40, Vandenberg SLC 4E, Kennedy Space Center LC 39A).

* **Task 2: Analyze Orbit Occurrences:**
    * The `value_counts()` method is used on the `Orbit` column to determine the frequency of each orbit type (e.g., LEO, VLEO, GTO, SSO, ISS). Contextual explanations for various orbit types are provided.

* **Task 3: Analyze Mission Outcomes:**
    * The `value_counts()` method is applied to the `Outcome` column to tally the occurrences of different landing outcomes (e.g., True ASDS, None None, True RTLS, False Ocean).
    * A set named `bad_outcomes` is explicitly defined to include all outcomes that represent an unsuccessful first stage landing (e.g., 'None ASDS', 'False RTLS', 'False Ocean', 'None None', 'False ASDS').

* **Task 4: Create Landing Outcome Label:**
    * A new list, `landing_class`, is generated.
    * For each outcome in the DataFrame's `Outcome` column, `0` is appended to `landing_class` if the outcome is in the `bad_outcomes` set (unsuccessful landing).
    * Otherwise, `1` is appended (successful landing).
    * This `landing_class` is intended to be added as a 'Class' column to the DataFrame, serving as the binary target variable for classification models.

The lab concludes with the dataset prepared, having undergone data wrangling and the creation of the essential target variable for subsequent machine learning model training.



Okay, here's the content presented as normal text using bullet points:

This Jupyter Notebook details **Lab 2: Data Wrangling and Exploratory Data Analysis (EDA)**, part of a larger project on **SpaceX Falcon 9 First Stage Landing Prediction**.

The primary goals for this lab are:
* To perform exploratory data analysis to discover patterns within the dataset.
* To determine the appropriate labels (1 for successful landing, 0 for unsuccessful) for training supervised machine learning models.
* The estimated completion time for this lab is 60 minutes.

The process follows these steps:

* **Environment Setup:**
    * Installation of necessary Python libraries (`pandas`, `numpy`).
    * Importation of `pandas` and `numpy` into the notebook.

* **Data Loading:**
    * The `dataset_part_1.csv` file is loaded into a pandas DataFrame.
    * The first 10 rows of the loaded DataFrame are displayed for initial inspection.

* **Initial Data Exploration:**
    * Calculation of the percentage of missing values for each attribute (column) in the DataFrame.
    * Identification of the data types (e.g., numerical, categorical, boolean) for all columns in the DataFrame.

* **Task 1: Analyze Launch Sites:**
    * The `value_counts()` method is applied to the `LaunchSite` column to count the number of launches from each unique site (e.g., Cape Canaveral SLC 40, Vandenberg SLC 4E, Kennedy Space Center LC 39A).

* **Task 2: Analyze Orbit Occurrences:**
    * The `value_counts()` method is used on the `Orbit` column to determine the frequency of each orbit type (e.g., LEO, VLEO, GTO, SSO, ISS). Contextual explanations for various orbit types are provided.

* **Task 3: Analyze Mission Outcomes:**
    * The `value_counts()` method is applied to the `Outcome` column to tally the occurrences of different landing outcomes (e.g., True ASDS, None None, True RTLS, False Ocean).
    * A set named `bad_outcomes` is explicitly defined to include all outcomes that represent an unsuccessful first stage landing (e.g., 'None ASDS', 'False RTLS', 'False Ocean', 'None None', 'False ASDS').

* **Task 4: Create Landing Outcome Label:**
    * A new list, `landing_class`, is generated.
    * For each outcome in the DataFrame's `Outcome` column, `0` is appended to `landing_class` if the outcome is in the `bad_outcomes` set (unsuccessful landing).
    * Otherwise, `1` is appended (successful landing).
    * This `landing_class` is intended to be added as a 'Class' column to the DataFrame, serving as the binary target variable for classification models.

The lab concludes with the dataset prepared, having undergone data wrangling and the creation of the essential target variable for subsequent machine learning model training.











In this video, we will review data wrangling. Let’s review some of the attributes: Flight Number, Date, Booster version, Payload mass Orbit, Launch Site, Outcome: this is the status of the first stage Flights, Grid Fins: these help with landing Reused, Legs: used in landing Landing pad, Block, Reused count, Serial, Longitude and latitude of launch Let’s take a look at some of these attributes. The column “LaunchSite” contains the different launch sites, including: Vandenberg AFB Space Launch Kennedy Space Center CCAFS SLC 40 The column orbits are the different orbits of the payload. For Example: LEO: Low Earth orbit (LEO)is an Earth-centered orbit with an altitude of 2,000 km GTO A geosynchronous orbit is a high Earth orbit that allows satellites to match Earth's rotation. It is located at 22,236 miles (35,786 kilometers) above Earth's equator. The column Outcome indicates if the first stage successfully landed. There are 8 of them, for example. True ASDS means the booster successfully landed to a drone ship as shown the following looped video. False ASDS means the mission outcome was unsuccessfully landed to a drone ship as shown in the video loop. Outcome We would like landing outcomes to be converted to Classes y. y. (either 0 or 1). 0 is a bad outcome, that is, the booster did not land. 1 is a good outcome, that is, the booster did land. The variable Y will represent the classification variable that represents the outcome of each launch.











Based on the provided code and documentation, I'll create a detailed flowchart that captures the actual web scraping process implemented in your Python code.Here's the textual breakdown of the web scraping process extracted from your code:

## **Web Scraping Process Flow (Text Format)**

Setup & Preparation:
 Installing and importing Packages: beautifulsoup4, requests
 Define Helper Functions
Request and get the HTML data:
 Conducting the HTTP Request and set target URL: Wikipedia Falcon 9 launches page 
 Send GET Request and verify Response: 200 status code
HTML parsing:
 Get raw HTML content from response
 Extract HTML Text and BeautifulSoup Object for 
 Verify and locate tables Page 
Further actions:
Transform the HTML through data wrangling using Python, BeautifulSoup and the helper functions


### **Phase 4: Data Structure Setup (TASK 3)**
16. **Create Empty Dictionary**: Initialize `launch_dict` with column keys
17. **Initialize Dictionary Values**: Set each key to empty list
18. **Add Additional Columns**: Include 'Version Booster', 'Booster landing', 'Date', 'Time'

### **Phase 5: Main Data Extraction Loop**
19. **Find Target Tables**: Locate tables with class 'wikitable plainrowheaders collapsible'
20. **Iterate Through Tables**: Process each relevant table
21. **Iterate Through Rows**: Process each `<tr>` element
22. **Check Row Header**: Verify if row has `<th>` element
23. **Validate Flight Number**: Confirm header contains numeric flight number
24. **Extract Table Data**: Get all `<td>` elements from valid rows

### **Phase 6: Data Field Extraction (Per Valid Row)**
25. **Flight Number**: Extract and store flight number
26. **Date & Time**: Use `date_time()` helper function
27. **Booster Version**: Use `booster_version()` helper function
28. **Launch Site**: Extract from anchor tag text
29. **Payload**: Extract from anchor tag text
30. **Payload Mass**: Use `get_mass()` with normalization
31. **Orbit**: Extract from anchor tag text
32. **Customer**: Extract with error handling for missing data
33. **Launch Outcome**: Extract from string content
34. **Booster Landing**: Use `landing_status()` helper function

### **Phase 7: Data Storage & Export**
35. **Store Values**: Add extracted data to `launch_dict`
36. **Continue Loop**: Process remaining rows and tables
37. **Create DataFrame**: Convert dictionary to pandas DataFrame
38. **Verify Structure**: Check DataFrame info and structure
39. **Export to CSV**: Save as 'spacex_web_scraped.csv'
40. **Process Complete**: End of web scraping workflow

### **Key Features of This Process:**
- **Error Handling**: Checks for missing anchor tags and data
- **Data Normalization**: Uses unicodedata for mass values
- **Helper Functions**: Modular approach for data extraction
- **Validation**: Confirms flight numbers are numeric
- **Multiple Tables**: Processes all relevant tables on the page
- **Clean Export**: Creates structured CSV for further analysis

This process successfully extracts Falcon 9 launch data from Wikipedia's HTML tables and converts it into a structured format for analysis.





















Based on the provided code and documentation, I'll create a detailed flowchart that captures the actual web scraping process implemented in your Python code.Here's the textual breakdown of the web scraping process extracted from your code:

## **Web Scraping Process Flow (Text Format)**

### **Phase 1: Setup & Preparation**
1. **Install and  Required Packages**: beautifulsoup4, requests
2. **Import Libraries**: requests, BeautifulSoup, pandas, re, unicodedata
3. **Define Helper Functions**:
   - `date_time()` - Extract date and time from table cells
   - `booster_version()` - Extract booster version information
   - `landing_status()` - Extract landing status
   - `get_mass()` - Extract and normalize payload mass
   - `extract_column_from_header()` - Clean column names from headers

### **Phase 2: HTTP Request (TASK 1)**
4. **Set Target URL**: Wikipedia Falcon 9 launches page (June 9, 2021 snapshot)
5. **Send GET Request**: Use `requests.get()` to fetch HTML content
6. **Verify Response**: Check for HTTP 200 status code
7. **Extract HTML Text**: Get raw HTML content from response

### **Phase 3: HTML Parsing (TASK 2)**
8. **Create BeautifulSoup Object**: Parse HTML with html.parser
9. **Verify Page Title**: Confirm correct page loaded
10. **Find All Tables**: Use `find_all('table')` to locate all tables
11. **Identify Target Table**: Select `html_tables[2]` (third table)
12. **Extract Column Headers**: Find all `<th>` elements
13. **Process Headers**: Use `extract_column_from_header()` for each header
14. **Build Column Names List**: Create list of clean column names
15. **Remove Irrelevant Columns**: Delete 'Date and time ( )' column

### **Phase 4: Data Structure Setup (TASK 3)**
16. **Create Empty Dictionary**: Initialize `launch_dict` with column keys
17. **Initialize Dictionary Values**: Set each key to empty list
18. **Add Additional Columns**: Include 'Version Booster', 'Booster landing', 'Date', 'Time'

### **Phase 5: Main Data Extraction Loop**
19. **Find Target Tables**: Locate tables with class 'wikitable plainrowheaders collapsible'
20. **Iterate Through Tables**: Process each relevant table
21. **Iterate Through Rows**: Process each `<tr>` element
22. **Check Row Header**: Verify if row has `<th>` element
23. **Validate Flight Number**: Confirm header contains numeric flight number
24. **Extract Table Data**: Get all `<td>` elements from valid rows

### **Phase 6: Data Field Extraction (Per Valid Row)**
25. **Flight Number**: Extract and store flight number
26. **Date & Time**: Use `date_time()` helper function
27. **Booster Version**: Use `booster_version()` helper function
28. **Launch Site**: Extract from anchor tag text
29. **Payload**: Extract from anchor tag text
30. **Payload Mass**: Use `get_mass()` with normalization
31. **Orbit**: Extract from anchor tag text
32. **Customer**: Extract with error handling for missing data
33. **Launch Outcome**: Extract from string content
34. **Booster Landing**: Use `landing_status()` helper function

### **Phase 7: Data Storage & Export**
35. **Store Values**: Add extracted data to `launch_dict`
36. **Continue Loop**: Process remaining rows and tables
37. **Create DataFrame**: Convert dictionary to pandas DataFrame
38. **Verify Structure**: Check DataFrame info and structure
39. **Export to CSV**: Save as 'spacex_web_scraped.csv'
40. **Process Complete**: End of web scraping workflow

### **Key Features of This Process:**
- **Error Handling**: Checks for missing anchor tags and data
- **Data Normalization**: Uses unicodedata for mass values
- **Helper Functions**: Modular approach for data extraction
- **Validation**: Confirms flight numbers are numeric
- **Multiple Tables**: Processes all relevant tables on the page
- **Clean Export**: Creates structured CSV for further analysis

This process successfully extracts Falcon 9 launch data from Wikipedia's HTML tables and converts it into a structured format for analysis.




Another popular data source for obtaining Falcon 9 Launch data is web scraping related Wiki pages. In this lesson, you will be using the Python BeautifulSoup package to web scrape some HTML tables that contain valuable Falcon 9 launch records. Then you need to parse the data from those tables and convert them into a Pandas data frame for further visualization and analysis.
More specifically, the launch records are stored in a HTML table shown below:

Image
Objectives

Web scrap Falcon 9 launch records with BeautifulSoup:

    Extract a Falcon 9 launch records HTML table from Wikipedia
    Parse the table and convert it into a Pandas data frame

First let's import required packages for this lab

!pip3 install beautifulsoup4

!pip3 install requests

Requirement already satisfied: beautifulsoup4 in c:\users\gamarandor\miniconda3\envs\data_analytics\lib\site-packages (4.13.4)
Requirement already satisfied: soupsieve>1.2 in c:\users\gamarandor\miniconda3\envs\data_analytics\lib\site-packages (from beautifulsoup4) (2.7)
Requirement already satisfied: typing-extensions>=4.0.0 in c:\users\gamarandor\miniconda3\envs\data_analytics\lib\site-packages (from beautifulsoup4) (4.9.0)
Requirement already satisfied: requests in c:\users\gamarandor\miniconda3\envs\data_analytics\lib\site-packages (2.31.0)
Requirement already satisfied: charset-normalizer<4,>=2 in c:\users\gamarandor\miniconda3\envs\data_analytics\lib\site-packages (from requests) (2.0.4)
Requirement already satisfied: idna<4,>=2.5 in c:\users\gamarandor\miniconda3\envs\data_analytics\lib\site-packages (from requests) (3.4)
Requirement already satisfied: urllib3<3,>=1.21.1 in c:\users\gamarandor\miniconda3\envs\data_analytics\lib\site-packages (from requests) (2.1.0)
Requirement already satisfied: certifi>=2017.4.17 in c:\users\gamarandor\miniconda3\envs\data_analytics\lib\site-packages (from requests) (2025.1.31)

import sys

​

import requests

from bs4 import BeautifulSoup

import re

import unicodedata

import pandas as pd

and we will provide some helper functions for you to process web scraped HTML table

def date_time(table_cells):

    """

    This function returns the data and time from the HTML  table cell

    Input: the  element of a table data cell extracts extra row

    """

    return [data_time.strip() for data_time in list(table_cells.strings)][0:2]

​

def booster_version(table_cells):

    """

    This function returns the booster version from the HTML  table cell 

    Input: the  element of a table data cell extracts extra row

    """

    out=''.join([booster_version for i,booster_version in enumerate( table_cells.strings) if i%2==0][0:-1])

    return out

​

def landing_status(table_cells):

    """

    This function returns the landing status from the HTML table cell 

    Input: the  element of a table data cell extracts extra row

    """

    out=[i for i in table_cells.strings][0]

    return out

​

​

def get_mass(table_cells):

    mass=unicodedata.normalize("NFKD", table_cells.text).strip()

    if mass:

        mass.find("kg")

        new_mass=mass[0:mass.find("kg")+2]

    else:

        new_mass=0

    return new_mass

​

​

def extract_column_from_header(row):

    """

    This function returns the landing status from the HTML table cell 

    Input: the  element of a table data cell extracts extra row

    """

    if (row.br):

        row.br.extract()

    if row.a:

        row.a.extract()

    if row.sup:

        row.sup.extract()

        

    colunm_name = ' '.join(row.contents)

    

    # Filter the digit and empty names

    if not(colunm_name.strip().isdigit()):

        colunm_name = colunm_name.strip()

        return colunm_name    

​

print(landing_status.__doc__)


    This function returns the landing status from the HTML table cell 
    Input: the  element of a table data cell extracts extra row
    

To keep the lab tasks consistent, you will be asked to scrape the data from a snapshot of the List of Falcon 9 and Falcon Heavy launches Wikipage updated on 9th June 2021

static_url = "https://en.wikipedia.org/w/index.php?title=List_of_Falcon_9_and_Falcon_Heavy_launches&oldid=1027686922"

Next, request the HTML page from the above URL and get a response object
TASK 1: Request the Falcon9 Launch Wiki page from its URL

First, let's perform an HTTP GET method to request the Falcon9 Launch HTML page, as an HTTP response.

# use requests.get() method with the provided static_url

# assign the response to a object

​

response = requests.get(static_url)

print(response)

print(response.status_code)

<Response [200]>
200

response.text[:200]

'<!DOCTYPE html>\n<html class="client-nojs vector-feature-language-in-header-enabled vector-feature-language-in-main-page-header-disabled vector-feature-page-tools-pinned-disabled vector-feature-toc-pin'

Create a BeautifulSoup object from the HTML response

# Use BeautifulSoup() to create a BeautifulSoup object from a response text content

​

soup = BeautifulSoup(response.text, parser="html.parser")

print(type(soup))

<class 'bs4.BeautifulSoup'>

Print the page title to verify if the BeautifulSoup object was created properly

# Use soup.title attribute

print(soup.title)

<title>List of Falcon 9 and Falcon Heavy launches - Wikipedia</title>

TASK 2: Extract all column/variable names from the HTML table header

Next, we want to collect all relevant column names from the HTML table header

Let's try to find all tables on the wiki page first. If you need to refresh your memory about BeautifulSoup, please check the external reference link towards the end of this lab

# Use the find_all function in the BeautifulSoup object, with element type `table`

# Assign the result to a list called `html_tables`

html_tables = soup.find_all("table")

print(len(html_tables))

# print(html_tables[24])

print(html_tables[24].string)

# print(html_tables[24])

25
None

Starting from the third table is our target table contains the actual launch records.

# Let's print the third table and check its content

first_launch_table = html_tables[2]

# print(first_launch_table)

You should able to see the columns names embedded in the table header elements <th> as follows:

<tr>
<th scope="col">Flight No.
</th>
<th scope="col">Date and<br/>time (<a href="/wiki/Coordinated_Universal_Time" title="Coordinated Universal Time">UTC</a>)
</th>
<th scope="col"><a href="/wiki/List_of_Falcon_9_first-stage_boosters" title="List of Falcon 9 first-stage boosters">Version,<br/>Booster</a> <sup class="reference" id="cite_ref-booster_11-0"><a href="#cite_note-booster-11">[b]</a></sup>
</th>
<th scope="col">Launch site
</th>
<th scope="col">Payload<sup class="reference" id="cite_ref-Dragon_12-0"><a href="#cite_note-Dragon-12">[c]</a></sup>
</th>
<th scope="col">Payload mass
</th>
<th scope="col">Orbit
</th>
<th scope="col">Customer
</th>
<th scope="col">Launch<br/>outcome
</th>
<th scope="col"><a href="/wiki/Falcon_9_first-stage_landing_tests" title="Falcon 9 first-stage landing tests">Booster<br/>landing</a>
</th></tr>

Next, we just need to iterate through the <th> elements and apply the provided extract_column_from_header() to extract column name one by one

column_names = []

​

# Apply find_all() function with `th` element on first_launch_table

# Iterate each th element and apply the provided extract_column_from_header() to get a column name

# Append the Non-empty column name (`if name is not None and len(name) > 0`) into a list called column_names

​

column_names = []

​

soup_th = first_launch_table.find_all('th')

​

for row in soup_th:

    name = extract_column_from_header(row)

    if name is not None and len(name) > 0:

        column_names.append(name)

        

print(column_names)

['Flight No.', 'Date and time ( )', 'Launch site', 'Payload', 'Payload mass', 'Orbit', 'Customer', 'Launch outcome']

Check the extracted column names

print(column_names)

['Flight No.', 'Date and time ( )', 'Launch site', 'Payload', 'Payload mass', 'Orbit', 'Customer', 'Launch outcome']

TASK 3: Create a data frame by parsing the launch HTML tables

We will create an empty dictionary with keys from the extracted column names in the previous task. Later, this dictionary will be converted into a Pandas dataframe

launch_dict= dict.fromkeys(column_names)

​

# Remove an irrelvant column

del launch_dict['Date and time ( )']

​

# Let's initial the launch_dict with each value to be an empty list

launch_dict['Flight No.'] = []

launch_dict['Launch site'] = []

launch_dict['Payload'] = []

launch_dict['Payload mass'] = []

launch_dict['Orbit'] = []

launch_dict['Customer'] = []

launch_dict['Launch outcome'] = []

# Added some new columns

launch_dict['Version Booster']=[]

launch_dict['Booster landing']=[]

launch_dict['Date']=[]

launch_dict['Time']=[]

Next, we just need to fill up the launch_dict with launch records extracted from table rows.

Usually, HTML tables in Wiki pages are likely to contain unexpected annotations and other types of noises, such as reference links B0004.1[8], missing values N/A [e], inconsistent formatting, etc.

To simplify the parsing process, we have provided an incomplete code snippet below to help you to fill up the launch_dict. Please complete the following code snippet with TODOs or you can choose to write your own logic to parse all launch tables:

extracted_row = 0

#Extract each table 

for table_number,table in enumerate(soup.find_all('table',"wikitable plainrowheaders collapsible")):

   # get table row 

    for rows in table.find_all("tr"):

        #check to see if first table heading is as number corresponding to launch a number 

        if rows.th:

            if rows.th.string:

                flight_number=rows.th.string.strip()

                flag=flight_number.isdigit()

        else:

            flag=False

        #get table element 

        row=rows.find_all('td')

        #if it is number save cells in a dictonary 

        if flag:

            extracted_row += 1

            # Flight Number value

            # TODO: Append the flight_number into launch_dict with key `Flight No.`

            launch_dict['Flight No.'] = flight_number 

            #print(flight_number)

            datatimelist=date_time(row[0])

            

            # Date value

            # TODO: Append the date into launch_dict with key `Date`

            launch_dict['Date']= datatimelist

            date = datatimelist[0].strip(',')

            print(date)

​

            

            # Time value

            # TODO: Append the time into launch_dict with key `Time`

            # launch_dict['Time']= time

            time = datatimelist[1]

            launch_dict['Time']= time

            #print(time)

              

            # Booster version

            # TODO: Append the bv into launch_dict with key `Version Booster`

            

            bv=booster_version(row[1])

            if not(bv):

                bv=row[1].a.string

            print(bv)

            launch_dict['Version Booster']= bv

            

            # Launch Site

            # TODO: Append the bv into launch_dict with key `Launch Site`

            

            launch_site = row[2].a.string

            launch_dict['Launch site'] = bv

            #print(launch_site)

            

            # Payload

            # TODO: Append the payload into launch_dict with key `Payload`

            

            payload = row[3].a.string

            launch_dict['Payload'] = payload

            #print(payload)

            

            # Payload Mass

            # TODO: Append the payload_mass into launch_dict with key `Payload mass`

            

            payload_mass = get_mass(row[4])

            launch_dict['Payload mass'] = payload_mass

            #print(payload)

            

            # Orbit

            # TODO: Append the orbit into launch_dict with key `Orbit`

            

            orbit = row[5].a.string

            launch_dict['Orbit'] = orbit

            #print(orbit)

            

            # Customer

            # TODO: Append the customer into launch_dict with key `Customer`

            # Check if row[6] and row[6].a exist before accessing .string

            if len(row) > 6 and row[6].a:

                 customer = row[6].a.string

            else:

                 customer = None  # Assign a default value, like None or an empty string

​

            # customer = row[6].a.string

            launch_dict['Customer'] = customer

            

            # print(customer)

            

            # Launch outcome

            # TODO: Append the launch_outcome into launch_dict with key `Launch outcome`

            

            launch_outcome = list(row[7].strings)[0]

            launch_dict['Launch outcome'] = launch_outcome 

            #print(launch_outcome)

            

            # Booster landing

            # TODO: Append the launch_outcome into launch_dict with key `Booster landing`

            

            booster_landing = landing_status(row[8])

            launch_dict['Launch outcome'] = launch_outcome

            #print(booster_landing)

            

4 June 2010
F9 v1.07B0003.18
8 December 2010
F9 v1.07B0004.18
22 May 2012
F9 v1.07B0005.18
8 October 2012
F9 v1.07B0006.18
1 March 2013
F9 v1.07B0007.18
29 September 2013
F9 v1.17B10038
3 December 2013
F9 v1.1
6 January 2014
F9 v1.1
18 April 2014
F9 v1.1
14 July 2014
F9 v1.1
5 August 2014
F9 v1.1
7 September 2014
F9 v1.1[
21 September 2014
F9 v1.1[
10 January 2015
F9 v1.1[
11 February 2015
F9 v1.1[
2 March 2015
F9 v1.1[
14 April 2015
F9 v1.1[
27 April 2015
F9 v1.1[
28 June 2015
F9 v1.1[
22 December 2015
F9 FT[
17 January 2016
F9 v1.1[
4 March 2016
F9 FT[
8 April 2016
F9 FT[
6 May 2016
F9 FT[
27 May 2016
F9 FT[
15 June 2016
F9 FT[
18 July 2016
F9 FT[
14 August 2016
F9 FT[
14 January 2017
F9 FT[
19 February 2017
F9 FT[
16 March 2017
F9 FT[
30 March 2017
F9 FT♺[
1 May 2017
F9 FT[
15 May 2017
F9 FT[
3 June 2017
F9 FT[
23 June 2017
F9 FTB1029.2195
25 June 2017
F9 FT[
5 July 2017
F9 FT[
14 August 2017
F9 B4[
24 August 2017
F9 FT[
7 September 2017
F9 B4[
9 October 2017
F9 B4[
11 October 2017
F9 FTB1031.2220
30 October 2017
F9 B4[
15 December 2017
F9 FTB1035.2227
23 December 2017
F9 FTB1036.2227
8 January 2018
F9 B4[
31 January 2018
F9 FTB1032.2245
22 February 2018
F9 FTB1038.2268
6 March 2018
F9 B4[
30 March 2018
F9 B4B1041.2268
2 April 2018
F9 B4B1039.2292
18 April 2018
F9 B4[
11 May 2018
F9 B5311B1046.1268
22 May 2018
F9 B4B1043.2322
4 June 2018
F9 B4B1040.2268
29 June 2018
F9 B4B1045.2336
22 July 2018
F9 B5
25 July 2018
F9 B5349B1048[
7 August 2018
F9 B5B1046.2354
10 September 2018
F9 B5[
8 October 2018
F9 B5B1048.2364
15 November 2018
F9 B5B1047.2268
3 December 2018
F9 B5B1046.3268
5 December 2018
F9 B5[
23 December 2018
F9 B5[
11 January 2019
F9 B5B1049.2397
22 February 2019
F9 B5B1048.3399
2 March 2019
F9 B5[]413
4 May 2019
F9 B5[
24 May 2019
F9 B5B1049.3434
12 June 2019
F9 B5B1051.2420
25 July 2019
F9 B5B1056.2465
6 August 2019
F9 B5B1047.3472
11 November 2019
F9 B5
5 December 2019
F9 B5[
17 December 2019
F9 B5B1056.3482
7 January 2020
F9 B5
19 January 2020
F9 B5
29 January 2020
F9 B5
17 February 2020
F9 B5
7 March 2020
F9 B5
18 March 2020
F9 B5
22 April 2020
F9 B5
30 May 2020
F9 B5[
4 June 2020
F9 B5
13 June 2020
F9 B5
30 June 2020
F9 B5
20 July 2020
F9 B5B1058.2544
7 August 2020
F9 B5
18 August 2020
F9 B5B1049.6544
30 August 2020
F9 B5
3 September 2020
F9 B5B1060.2563
6 October 2020
F9 B5B1058.3565
18 October 2020
F9 B5B1051.6568
24 October 2020
F9 B5
5 November 2020
F9 B5
16 November 2020
F9 B5[
21 November 2020
F9 B5
25 November 2020
F9 B5 ♺[
6 December 2020
F9 B5 ♺[
13 December 2020
F9 B5 ♺
19 December 2020
F9 B5 ♺
8 January 2021
F9 B5
20 January 2021
F9 B5B1051.8609
24 January 2021
F9 B5B1058.5613
4 February 2021
F9 B5 ♺[
16 February 2021
F9 B5 ♺
4 March 2021
F9 B5 ♺[
11 March 2021
F9 B5 ♺[
14 March 2021
F9 B5 ♺
24 March 2021
F9 B5B1060.6643
7 April 2021
F9 B5 ♺
23 April 2021
F9 B5B1061.2647
29 April 2021
F9 B5B1060.7652
4 May 2021
F9 B5B1049.9655
9 May 2021
F9 B5B1051.10657
15 May 2021
F9 B5B1058.8660
26 May 2021
F9 B5B1063.2665
3 June 2021
F9 B5B1067.1668
6 June 2021
F9 B5

After you have fill in the parsed launch record values into launch_dict, you can create a dataframe from it.

df= pd.DataFrame({ key:pd.Series(value) for key, value in launch_dict.items() })

df.info()

<class 'pandas.core.frame.DataFrame'>
RangeIndex: 2 entries, 0 to 1
Data columns (total 11 columns):
 #   Column           Non-Null Count  Dtype 
---  ------           --------------  ----- 
 0   Flight No.       1 non-null      object
 1   Launch site      1 non-null      object
 2   Payload          1 non-null      object
 3   Payload mass     1 non-null      object
 4   Orbit            1 non-null      object
 5   Customer         1 non-null      object
 6   Launch outcome   1 non-null      object
 7   Version Booster  1 non-null      object
 8   Booster landing  0 non-null      object
 9   Date             2 non-null      object
 10  Time             1 non-null      object
dtypes: object(11)
memory usage: 304.0+ bytes

We can now export it to a CSV for the next section, but to make the answers consistent and in case you have difficulties finishing this lab.

Following labs will be using a provided dataset to make each lab independent.

df.to_csv('spacex_web_scraped.csv', index=False)





Here’s a conceptual flowchart for the data collection process described in your text. Each step corresponds to a key part of the process:

1. **Start**

   * Initiate the data collection process.

2. **Define Data Source**

   * Identify the API and specific endpoint (e.g., `api.spacexdata.com/v4/launches/past`).

3. **Perform API Request**

   * Use the `requests` library to send a GET request to the API endpoint.

4. **Receive JSON Response**

   * Receive the response from the API in JSON format.

5. **Check Response Status**

   * Verify if the response status code indicates success (e.g., 200 OK).

     * **If unsuccessful**, log the error and stop.
     * **If successful**, proceed.

6. **Extract Data**

   * Call the `.json()` method to parse the JSON response into Python objects.

7. **Normalize JSON**

   * Use the `json_normalize` function to flatten the JSON into a tabular structure.

8. **Convert to DataFrame**

   * Convert the normalized JSON into a Pandas DataFrame.

9. **Inspect & Store Data**

   * Inspect the DataFrame and save it for further analysis.

10. **End**

Would you like me to create this flowchart visually for you?


In this video, we will review Collecting the Data with an API. In this capstone assignment, we will be working with SpaceX launch data that is gathered from an API, specifically the SpaceX REST API. This API will give us data about launches, including information about the rocket used, payload delivered, launch specifications, landing specifications, and landing outcome. Our goal is to use this data to predict whether SpaceX will attempt to land a rocket or not. The SpaceX REST API endpoints, or URL, starts with api.spacexdata.com/v4/. We have the different end points, for example: /capsules and /cores We will be working with the endpoint api.spacexdata.com/v4/launches/past. Let’s see how the API works. We will use this URL to target a specific endpoint of the API to get past launch data. We will perform a get request using the requests library to obtain the launch data, which we will use to get the data from the API. This result can be viewed by calling the .json() method. Our response will be in the form of a JSON, specifically a list of JSON objects. Since we are using an API, you will notice in the lab that when we get a response it is in the form of a JSON. Specifically, we have a list of JSON objects which each represent a launch. To convert this JSON to a dataframe, we can use the json_normalize function. This function will allow us to “normalize” the structured json data into a flat table. This is what your JSON will look like in a table form. 

Another popular data source for obtaining Falcon 9 Launch data is web scraping related Wiki pages. In this lesson, you will be using the Python BeautifulSoup package to web scrape some HTML tables that contain valuable Falcon 9 launch records. Then you need to parse the data from those tables and convert them into a Pandas data frame for further visualization and analysis. We want to transform this raw data into a clean dataset which provides meaningful data on the situation we are trying to address: Wrangling Data using an API, Sampling Data, and Dealing with Nulls. You will notice, in some of the columns, like rocket, we have an identification number, not actual data. This means we will need to use the API again targeting another endpoint to gather specific data for each ID number. These functions are already created for you, and will use the following: Booster, Launchpad, payload, and core. The data will be stored in lists and will be used to create our dataset. Another issue we have is that the launch data we have includes data for the Falcon 1 booster whereas we only want falcon 9. In this lab, you will need to figure out how to filter/sample the data to remove Falcon 1 launches. Finally, not all gathered data is perfect. We may end up with data that contains NULL values. We must sometimes deal with these null values in order to make the dataset viable for analysis. In this case, we will deal with the NULL values inside the PayloadMass. In this lab, you must figure out a way to calculate the mean of the PayloadMass data and then replace the null values in PayloadMass with the mean. We will leave the column LandingPad with NULL values, as it is represented when a landing pad is not used. This will be dealt with using one hot encoding later on.
