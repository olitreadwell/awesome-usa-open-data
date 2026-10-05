# Awesome USA Data [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of United States data sources, APIs, registers and portals, tagged with what each one is and what it takes to use it.

The list is also published as a searchable site at <https://olitreadwell.github.io/awesome-usa-open-data/>, generated from this README by `scripts/build_site.py`.

## Contents

- [Legend](#legend)
- [Start here](#start-here)
- [Federal government and agencies](#federal-government-and-agencies)
- [Statistics and economics](#statistics-and-economics)
- [Money, markets and regulation](#money-markets-and-regulation)
- [Health and public health](#health-and-public-health)
- [Education, science and culture](#education-science-and-culture)
- [Environment, climate and geospatial](#environment-climate-and-geospatial)
- [Transport](#transport)
- [Energy, agriculture and food](#energy-agriculture-and-food)
- [State portals](#state-portals)
- [City portals](#city-portals)

## Legend

Every entry is tagged with what it is, what it takes to use, and whether it is still the current tool for that data.

Each tag has its own shape, so the tags can be told apart without relying on colour. On the site the colour marks which axis a tag belongs to: blue for type, green for access, amber for status.

- Type: `⇄ API` (a programmatic interface), `▦ Data` (datasets you download or query), `☰ Portal` (a site you search across many datasets), `☑ Register` (an official register you look records up in), `¶ Docs` (documentation or metadata with no data of its own).
- Access: `○ Open` (no key and no account needed), `◑ Key` (API key or developer registration), `◕ Login` (user account), `● Paid`. The shape fills up as the access gets harder: empty is open, solid is paid.
- Status: `⟳ Legacy` (still online, but superseded) or `▣ Archived` (frozen snapshot). No status tag means current.

Tags sit between the link and the description, in that order:

```
- [Name](https://example.gov/) - ▦ Data - ○ Open - what it holds.
- [Name](https://example.gov/) - ⇄ API - ◑ Key - ⟳ Legacy - what it holds.
```

Dead links are repaired or dropped as they are found, and a weekly job re-checks every link.

## Start here

These cover most requests. Each one is listed in full under its publisher below.

- Data.gov - the catalogue of federal datasets
- Census Bureau Data APIs - population, ACS estimates and TIGER geography
- BLS Public Data API - employment, prices and pay
- FRED - economic time series from the St. Louis Fed
- openFDA - drug, device and food safety data
- USGS Earthquake Hazards - near-real-time seismic data
- EPA Environmental Data - air, water and toxics
- NYC Open Data - 3,000+ datasets from 40+ agencies

## Federal government and agencies

- [Data.gov](https://data.gov/) - ☰ Portal - ○ Open - US federal open data catalog. 200,000+ datasets via catalog.data.gov, CKAN API, and the DCAT metadata standard.
- [api.data.gov](https://api.data.gov/) - ☰ Portal - ○ Open - The API management gateway for federal agency APIs. Free API keys for public services like USGS and the National Weather Service.
- [Federal Register API](https://www.federalregister.gov/) - ⇄ API - ○ Open - Official rules, proposed rules, and notices from federal agencies with a free public JSON API, no key required.
- [Congress.gov API](https://api.congress.gov/) - ⇄ API - ◑ Key - Library of Congress API over congressional data: bills and their actions, amendments, Member records, House roll-call votes, committees, the Congressional Record, nominations, treaties, and CRS reports. JSON or XML on api.congress.gov/v3, up to 250 records per page, with a free key from api.data.gov.
- [GovInfo API](https://www.govinfo.gov/) - ⇄ API - ◑ Key - The Government Publishing Office's GovInfo: authenticated PDF and XML of Congressional bills, bill status, the Congressional Record, the Federal Register, the Code of Federal Regulations, the US Code, public laws, court opinions, and budget documents. The REST API at api.govinfo.gov takes an api.data.gov key, and GPO runs a bulk data repository and link service beside it.
- [Regulations.gov API](https://www.regulations.gov/) - ⇄ API - ◑ Key - Federal rulemaking records from the GSA-run Regulations.gov: dockets, documents, and public comments, with search and detail endpoints plus comment submission. The v4 API is documented at open.gsa.gov/api/regulationsgov with an OpenAPI specification, and DEMO_KEY works for a first call.
- [SAM.gov](https://sam.gov/entity-information) - ☰ Portal - ○ Open - Federal procurement system of record: entity registrations, contract awards, and assistance data, browsable at sam.gov and via API.
- [Open States](https://open.pluralpolicy.com/) - ⇄ API - ◑ Key - State legislative data for all 50 states, DC, and Puerto Rico: bills, votes, and legislators, from the Open States project that Plural Policy adopted in 2021. Bulk downloads and API key registration moved to open.pluralpolicy.com, and openstates.org now redirects to the Plural site.
- [FCC Open Data](https://opendata.fcc.gov/) - ☰ Portal - ○ Open - FCC open data: broadband maps, licensing, and Universal Service datasets served through opendata.fcc.gov and the FCC APIs.
- [FEMA OpenFEMA](https://www.fema.gov/about/reports-and-data/openfema) - ⇄ API - ○ Open - OpenFEMA datasets and APIs: disaster declarations, individual assistance, and NFIP claims as downloadable CSV plus JSON API.
- [FBI Crime Data Explorer API](https://cde.ucr.cjis.gov/LATEST/webapp/#/pages/docApi) - ⇄ API - ○ Open - Uniform Crime Reporting data behind the FBI Crime Data Explorer. The summarized endpoints return monthly offense rates for the nation, a state, or a single agency from a from/to date range, with a free api.data.gov key.
- [BJS Crime Statistics](https://bjs.ojp.gov/) - ▦ Data - ○ Open - Bureau of Justice Statistics: national crime victimization survey, recidivism, and corrections data with the Crime Data Explorer.

## Statistics and economics

- [Census Bureau Data APIs](https://www.census.gov/data/developers/data-sets.html) - ⇄ API - ○ Open - Census Data API and datasets: population, ACS 1/5-year estimates, economic census, and TIGER/Line geography. No key needed for low volume.
- [BLS Public Data API](https://www.bls.gov/developers/) - ⇄ API - ○ Open - Bureau of Labor Statistics API: CPI, unemployment, payrolls, producer prices, and other labor market series with a free API key.
- [BEA API](https://apps.bea.gov/api/) - ⇄ API - ◑ Key - Bureau of Economic Analysis API: GDP, national and regional income, and industry accounts in structured JSON after free registration.
- [FRED (Federal Reserve Economic Data)](https://fred.stlouisfed.org/) - ⇄ API - ◑ Key - Economic time series from the Federal Reserve Bank of St. Louis: the catalog counts 853,000 series drawn from 126 sources, covering GDP, prices, employment, interest rates, and banking. The REST API at api.stlouisfed.org returns series metadata, observations, search results, and release dates with a free key, and ALFRED serves each series as it was first published.
- [IRS Statistics of Income](https://www.irs.gov/statistics) - ▦ Data - ○ Open - SOI tables: individual and corporate tax statistics, migration data, and ZIP-level aggregates published as CSV and PDF yearbook tables.
- US Department of the Treasury
    - [USAspending API](https://api.usaspending.gov/) - ⇄ API - ○ Open - Treasury API for federal spending under the DATA Act: awards, recipients, agency and geographic breakdowns, and account-level data, all as JSON.
    - [Treasury Fiscal Data API](https://fiscaldata.treasury.gov/) - ⇄ API - ○ Open - Treasury fiscal data as a REST API and bulk download: national debt, interest rates, federal spending and revenue, and savings bond values. No API key.

## Money, markets and regulation

- [SEC EDGAR APIs](https://www.sec.gov/edgar/search/) - ⇄ API - ○ Open - Securities and Exchange Commission filings and the XBRL facts extracted from them. data.sec.gov serves company submission histories, company facts, and frames as JSON without an API key, and the EDGAR full-index archive covers bulk download of every filing.
- [OpenFEC API](https://www.fec.gov/data/) - ⇄ API - ◑ Key - The Federal Election Commission's campaign finance data: candidate and committee registrations, filings, itemized contributions and disbursements, independent expenditures, audit cases, and legal records such as advisory opinions and enforcement matters. The REST API runs on api.data.gov behind a free key, and the FEC republishes the same extracts as bulk downloads.
- [FDIC BankFind Suite API](https://banks.data.fdic.gov/bankfind-suite/bankfind) - ⇄ API - ○ Open - FDIC records for every insured US bank and thrift, served as JSON with no API key: institution details, branch locations, quarterly financials, structure and ownership history, and the failed-bank list. Endpoints run under api.fdic.gov/banks and the Swagger reference is at api.fdic.gov/banks/docs; the same extracts are downloadable from the FDIC bank data and statistics pages.
- [CPSC Product Recall API](https://www.saferproducts.gov/) - ⇄ API - ○ Open - Every consumer product recall the Consumer Product Safety Commission has published, one record per recall with the product, the hazard, the remedy offered, the countries that made it, and the model numbers. The REST endpoint answers JSON without a key, and the same records run SaferProducts.gov.
- Consumer Financial Protection Bureau
    - [CFPB Open Data](https://www.consumerfinance.gov/data-research/) - ☰ Portal - ○ Open - Consumer Financial Protection Bureau data products: the public Consumer Complaint Database (more than 18 million complaints, searchable as JSON through its search API), HMDA mortgage data, the small business lending database, and consumer credit trend dashboards.
    - [CFPB Consumer Complaint Database](https://www.consumerfinance.gov/data-research/consumer-complaints/) - ▦ Data - ○ Open - The Consumer Complaint Database, one row for every complaint the Consumer Financial Protection Bureau has sent to a company since December 2011: more than 18 million records with the product, the issue, the company, the date received, and the company response. The search API answers JSON without a key, and the same rows run the public complaint search.

## Health and public health

- US Department of Health and Human Services (HHS)
    - [CDC Open Data](https://data.cdc.gov/) - ☰ Portal - ○ Open - CDC data.cdc.gov Socrata portal: disease surveillance, vital statistics, health behaviors, and NCHS datasets with REST and SODA API.
    - [openFDA](https://open.fda.gov/) - ⇄ API - ○ Open - FDA public APIs: drug adverse events, device recalls and 510(k) clearances, food enforcement reports, and product labels. No key needed for low volume.
    - [CMS Provider Data](https://data.cms.gov/provider-data/) - ▦ Data - ○ Open - Care Compare provider data from the Centers for Medicare & Medicaid Services, covering hospitals, dialysis facilities, home health agencies, hospices, and nursing facilities. Public metastore API and bulk CSV downloads, no key needed.
    - [NIH RePORTER](https://reporter.nih.gov/) - ⇄ API - ○ Open - NIH database of funded biomedical research: projects, principal investigators, award amounts, and linked publications. JSON search API, no key.
    - [HealthData.gov](https://healthdata.gov/) - ☰ Portal - ○ Open - HHS open data catalog at healthdata.gov: a DCAT feed of about 19,700 datasets from FDA, CDC, CMS, NIH, and other HHS divisions, plus a Socrata discovery API for search across the catalog.
    - [ClinicalTrials.gov API](https://clinicaltrials.gov/) - ⇄ API - ○ Open - Clinical study registry from the National Library of Medicine: 605,000+ studies with sponsor, recruitment status, phase, enrollment, outcome measures, and locations. The v2 REST API answers JSON without a key, and /api/v2/studies/download streams every record as a zip of JSON.
    - [NCBI E-utilities](https://www.ncbi.nlm.nih.gov/home/develop/) - ⇄ API - ○ Open - The National Center for Biotechnology Information's keyless REST interface to 38 databases, from PubMed and PMC to GenBank, dbSNP, Protein, Taxonomy, and ClinVar. Search, summary, fetch, and link requests answer as JSON or XML.

## Education, science and culture

- [ED Open Data](https://data.ed.gov/) - ☰ Portal - ○ Open - Department of Education data.ed.gov: college scorecard, civil rights data collection, and federal student aid statistics.
- [NASA Open APIs](https://api.nasa.gov/) - ⇄ API - ◑ Key - NASA api.nasa.gov: APOD, Mars rover photos, NEO asteroid tracking, and satellite imagery, key optional for most endpoints.
- [Smithsonian Open Access](https://edan.si.edu/openaccess/apidocs/) - ⇄ API - ◑ Key - CC0 object records and media from the Smithsonian's museums, archives, and research centers: specimen and catalogue metadata, images, library volumes, and research data. The EDAN Open Access API at api.si.edu takes an api.data.gov key and its stats endpoint publishes CC0 record counts per unit each month (48 units in September 2026); the same release is on the AWS Open Data registry as bulk files.

## Environment, climate and geospatial

- [EPA Environmental Data](https://cdx.epa.gov/) - ☰ Portal - ○ Open - EPA Central Data Exchange and dataset catalog: air quality, water, toxics release inventory, and enforcement data with public APIs.
- [AirNow API](https://www.airnow.gov/) - ⇄ API - ◑ Key - Air quality observations and forecasts from the EPA's AirNow program, which draws on more than 150 local, state, tribal, provincial, and federal partner agencies and more than 2,500 monitoring stations. The REST API returns current AQI by ZIP code, reporting area, or latitude and longitude, plus forecasts, with a free key. Values are preliminary, not regulatory-grade.
- NOAA
    - [NOAA Open APIs](https://www.noaa.gov/) - ⇄ API - ○ Open - National Oceanic and Atmospheric Administration: weather, climate, tides, oceans, and satellite APIs, many reachable without a key.
    - [National Weather Service API](https://api.weather.gov/) - ⇄ API - ○ Open - The National Weather Service's public forecast and hazard service at api.weather.gov: point forecasts and hourly forecasts, active watches, warnings and advisories, observations from surface stations, radar and marine products, and climate reports. Every endpoint answers GeoJSON without an API key, and the service asks only that callers send a User-Agent that identifies their application.
- US Geological Survey
    - [USGS Earthquake Hazards](https://earthquake.usgs.gov/fdsnws/event/1/) - ⇄ API - ○ Open - FDSN event API for near-real-time earthquakes worldwide plus US hazard models. No key required, GeoJSON and KML formats.
    - [USGS Water Services](https://waterdata.usgs.gov/) - ⇄ API - ○ Open - USGS Water Services, the web services behind the National Water Information System (NWIS): daily, monthly, and annual streamflow for tens of thousands of river gauges, plus the annual peak-flow record for each one, as JSON, RDB, or WaterML. Keyless.

## Transport

- US Department of Transportation
    - [US DOT Open Data](https://data.transportation.gov/) - ☰ Portal - ○ Open - Department of Transportation open data portal: aviation, highways, rail, maritime, and vehicle safety datasets with Socrata APIs and bulk exports.
    - [Bureau of Transportation Statistics](https://data.bts.gov/) - ☰ Portal - ○ Open - The US DOT Bureau of Transportation Statistics portal at data.bts.gov: monthly transportation indicators, freight and supply-chain measures, and state-level transportation finance tables, published through Socrata SODA APIs with CSV and JSON downloads.
    - [NHTSA Vehicle APIs](https://api.nhtsa.gov/) - ⇄ API - ○ Open - National Highway Traffic Safety Administration APIs on api.nhtsa.gov: recalls and safety complaints by make, model, and year, product model lists, NCAP safety ratings, and VIN decoding through vPIC, all JSON with no key.

## Energy, agriculture and food

- [EIA Open Data API](https://www.eia.gov/opendata/) - ⇄ API - ◑ Key - US Energy Information Administration API: energy production, consumption, prices, and forecasts as JSON series with a free API key.
- US Department of Agriculture (USDA)
    - [USDA NASS Quick Stats API](https://quickstats.nass.usda.gov/) - ⇄ API - ◑ Key - National Agricultural Statistics Service estimates behind the Quick Stats query tool: crop and livestock production, inventories, prices, and county-level estimates, plus Census of Agriculture tables. The JSON API at quickstats.nass.usda.gov/api takes a free key, and NASS publishes bulk datasets for offline use.
    - [USDA FoodData Central](https://fdc.nal.usda.gov/) - ⇄ API - ◑ Key - USDA nutrition data: Foundation Foods with analytically measured nutrient values, SR Legacy, Branded Foods built from manufacturer labels, and the Food and Nutrient Database for Dietary Studies behind national dietary research. The REST API at api.nal.usda.gov/fdc/v1 searches foods and returns their nutrient values, with a DEMO_KEY for light use, and USDA republishes the whole release as CSV and JSON bulk downloads.

## State portals

- [New York State Open Data](https://data.ny.gov/) - ☰ Portal - ○ Open - New York State portal at data.ny.gov: health, transportation, labor, and environment datasets from state agencies, with the Socrata API and bulk exports.
- [California Open Data Portal](https://data.ca.gov/) - ☰ Portal - ○ Open - State of California data.ca.gov: budget, health, education, transportation, and environmental datasets with Socrata APIs.
- [Texas Open Data](https://data.texas.gov/) - ☰ Portal - ○ Open - State of Texas data.texas.gov: finance, health, licensing, and transportation datasets on the Socrata platform.
- [Colorado Open Data](https://data.colorado.gov/) - ☰ Portal - ○ Open - State of Colorado data.colorado.gov: water, health, environment, and agency datasets with Socrata APIs.
- [Washington State Open Data](https://data.wa.gov/) - ☰ Portal - ○ Open - State of Washington data.wa.gov: agency datasets on health, education, transportation, environment, and corrections, with Socrata SODA APIs and bulk exports.
- [Michigan Open Data](https://data.michigan.gov/) - ☰ Portal - ○ Open - State of Michigan portal at data.michigan.gov: agency datasets on procurement, public health, veterans services, and local government finance, served through the Socrata SODA API with bulk exports.
- [Oregon Open Data](https://data.oregon.gov/) - ☰ Portal - ○ Open - Oregon's state portal at data.oregon.gov: agency datasets on public safety, health and human services, education, business, and natural resources, published through Socrata SODA APIs with CSV, JSON, and XML exports.
- [Pennsylvania Open Data](https://data.pa.gov/) - ☰ Portal - ○ Open - Pennsylvania's state open data portal at data.pa.gov: agency datasets on elections, revenue, education, health, and transportation, served through Socrata SODA APIs with CSV, JSON, and XML exports.
- [Illinois Open Data](https://data.illinois.gov/) - ☰ Portal - ○ Open - The State of Illinois portal at data.illinois.gov: 404 datasets from state agencies covering health and human services, public safety, revenue, transportation, and the environment, published through the Socrata SODA API with CSV, JSON, and XML exports.
- [New Jersey Open Data](https://data.nj.gov/) - ☰ Portal - ○ Open - The State of New Jersey portal at data.nj.gov: 621 datasets from state agencies covering the environment, public safety, health, transportation, and the state budget, published through the Socrata SODA API with CSV, JSON, and XML exports.
- [Vermont Open Data](https://data.vermont.gov/) - ☰ Portal - ○ Open - The State of Vermont portal at data.vermont.gov: 270 datasets from state agencies covering education, health, transportation, energy, and the environment, published through the Socrata SODA API with CSV, JSON, and XML exports.

## City portals

- [NYC Open Data](https://www.nyc.gov/opendata) - ☰ Portal - ○ Open - New York City Socrata portal: 3,000+ datasets from 40+ agencies, covering permits, 311, taxi trips, and building data.
- [Chicago Data Portal](https://data.cityofchicago.org/) - ☰ Portal - ○ Open - City of Chicago Socrata portal: crime, permits, building violations, and transit datasets, a long-running civic open data program.
- [Los Angeles Data Portal](https://data.lacity.org/) - ☰ Portal - ○ Open - Los Angeles open data: myla311, permits, code enforcement, budgets, and mobility datasets on the Socrata platform.
- [Seattle Open Data](https://data.seattle.gov/) - ☰ Portal - ○ Open - City of Seattle Socrata portal: permits, land use, tree inventory, and 911 call data.
- [San Francisco Open Data](https://data.sf.gov/) - ☰ Portal - ○ Open - DataSF, the City and County of San Francisco's open data portal, which moved from data.sfgov.org to data.sf.gov. Department datasets on policing, transit, permits, housing, and the city budget, published through the Socrata Open Data API with JSON, CSV, and GeoJSON exports.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md). Pull requests are very welcome :smile:.

Tags are checked by the engine, so every entry needs a type (`API`, `Data`, `Portal`, `Register`, `Docs`) and an access level (`Open`, `Key`, `Login`, `Paid`), plus a status (`Legacy`, `Archived`) if the tool has been superseded.

If you spot a dead link, or a link that points at a page instead of the data itself, open an issue or send a PR.

Released under the MIT license, see [LICENSE](LICENSE).
