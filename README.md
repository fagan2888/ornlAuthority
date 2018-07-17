# ORNL Name Authority Metadata Application Profile



ORNL Name Authority, whenever possible, maps to several controlled vocabularies. They are listed in the chart below.

|Prefix | Namespace |
|---|---|
|foaf | http://xmlns.com/foaf/0.1/|
|schema | http://schema.org|
|adms| http://www.w3.org/ns/adms# |
|org | http://www.w3.org/ns/org# |
|dcterms|http://purl.org/dc/terms/ |


This Application Profile follows the generic MAP template created by the Metadata Working Group at Cornell University Library. 



*Field:* the name of the field  
*Schema mapping:* mapping of a shared standard, nampespace, or specification  
*Domain:* expected resource or object type this field is asserted against (useful if specifying fields that only apply to certain   resources, e.g. "title" may only apply to the domain "Book", as opposed to "Person")  
*Expected Value /  Range:* expected metadata value for field (e.g. string, integer...)  
*Definition:* definition for field  
*Obligation:* if required / repeatable {number of times expected, number of times can be present}  
*Usage Notes:* any notes on using this field in the metadata generated  
*Source:* the source of the filed (e.g. user-entered, pulled from internal database, API...)  
*Remediation Notes:* any notes on cleanup, normalization, or enhancement  
*Exposure / Other Representation:* other places this field may appear  


|Dim_City| schema.org/City|
|--------------|----------------|

| Field | Schema Mapping | Domain  | Expected Value | Definition | Obligation | Usage Notes | Source | Remediation Notes| Exposure / Other Representation |
| ------------- |:-------------:| :-----:| :-------------:| :--------------:|:----------:|:------:|:----:|:---:|:---:|
| Org City      | schema.org/City | City, Country | string | a city, town, or municipality | {0, 1}| | Scopus | may be incorrect | | 
| Org Country   | schema.org/Country |   City, Country | string | a country  | {1, 1} | | Scopus  | may be incorrect | name field in Dim_Country| 
| Org State     | schema.org/State |  State | string | a state or province  | {0, 1} | | Scopus | may be incorrect | | 
| Org Postal Code | schema.org/postalCode | City | string | the postal code | {0, 1} | | Scopus | may be incorrect | |
| Dim_Country.iso3c |schema.org/addressCountry | City, Country | 3-letter string | the ISO 3166-1 alpha-3 country code | {0, 1} | Providers are recommended to use the two letter code whenever possible | Worldbank |  |iso3c field in Dim_Country|
| Dim_Country.iso2c |schema.org/addressCountry | City, Country | 2-letter string | the ISO 3166-1 alpha-2 country code | {1, 1} | | Worldbank |  |iso2c field in Dim_Country | 
| Dim_Country.capitalCity | schema.org/City | City, Country | string | a city, town, or municipality | 
| City Key |
| Dim_Country.Country Key |
| is Oak Ridge |

|Dim_Country | schema.org/Country|
|------------|-------------------|

| Field | Schema Mapping | Domain  | Expected Value | Definition | Obligation | Usage Notes | Source | Remediation Notes| Exposure / Other Representation |
| ------------- |:-------------:| :-----:| :-------------:| :--------------:|:----------:|:------:|:----:|:---:|:---:|
|iso3c| schema.org/addressCountry | Country, City | 3-letter string | the ISO 3166-1 alpha-3 country code | {0, 1}
|iso2c| schema.org/addressCountry | Country, City | 2-letter string | the ISO 3166-1 alpha-2 country code | {1, 1}
|name | schema.org/Country | Country, City | string | name of the country | 
|region| schema.org/AdministrativeArea | Country | string | a geographical region | {0, 1} | | Scopus | May be incorrect | |
|capitalCity| schema.org/City | Country, City | string | a city, town, or municipality | {0, 1} | | Scopus | May be incorrect | Dim_City|
|incomeLevel|
|lendingType|
|latitude|
|longitude|
|Country Key|
|is USA|


|Dim_Scopus_Organization | ORG |
|------------|-------------------|

| Field    | Schema Mapping           | Domain  | Expected Value | Definition | Obligation | Usage Notes | Source | Remediation Notes| Exposure / Other Representation |
| ------------- |:-------------:| :-----:| :-------------:| :--------------:|:----------:|:------:|:----:|:---:|:---:|
|Org EID|
|Org Abbreviation|
|Org Name|
|Org Sort Name|
|Org Address|
|Org City|
|Org Country|
|Org State|
|Org Postal Code|
|City Key|
|Country Key|
|Clean Org name|
|Clean Org EID|


|Dim_Person_Identifiers | ADMS |
|------------|-------------------|

| Field    | Schema Mapping           | Domain  | Expected Value | Definition | Obligation | Usage Notes | Source | Remediation Notes| Exposure / Other Representation |
| ------------- |:-------------:| :-----:| :-------------:| :--------------:|:----------:|:------:|:----:|:---:|:---:|
|ORNLBadge|
|Orcid|
|Elsevier ID|
|Person_Bio_Durable_Key|
|Creation Date|
|Modified Date|
|Person Bio Key|

|Dim_ORNL_Organization | ORG |
|------------|-------------------|

| Field    | Schema Mapping           | Domain  | Expected Value | Definition | Obligation | Usage Notes | Source | Remediation Notes| Exposure / Other Representation |
| ------------- |:-------------:| :-----:| :-------------:| :--------------:|:----------:|:------:|:----:|:---:|:---:|
|

|Dim_Group | ORG |
|------------|-------------------|

| Field    | Schema Mapping           | Domain  | Expected Value | Definition | Obligation | Usage Notes | Source | Remediation Notes| Exposure / Other Representation |
| ------------- |:-------------:| :-----:| :-------------:| :--------------:|:----------:|:------:|:----:|:---:|:---:|


|Dim_Person_Bio | FOAF |
|------------|-------------------|

| Field    | Schema Mapping           | Domain  | Expected Value | Definition | Obligation | Usage Notes | Source | Remediation Notes| Exposure / Other Representation |
| ------------- |:-------------:| :-----:| :-------------:| :--------------:|:----------:|:------:|:----:|:---:|:---:|


|Dim_Org_Ranking | xxx |
|------------|-------------------|

| Field    | Schema Mapping           | Domain  | Expected Value | Definition | Obligation | Usage Notes | Source | Remediation Notes| Exposure / Other Representation |
| ------------- |:-------------:| :-----:| :-------------:| :--------------:|:----------:|:------:|:----:|:---:|:---:|


|Dim_Affiliation | ORG |
|------------|-------------------|

| Field    | Schema Mapping           | Domain  | Expected Value | Definition | Obligation | Usage Notes | Source | Remediation Notes| Exposure / Other Representation |
| ------------- |:-------------:| :-----:| :-------------:| :--------------:|:----------:|:------:|:----:|:---:|:---:|
