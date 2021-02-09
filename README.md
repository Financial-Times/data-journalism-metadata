# FT data journalism metadata

An evolving collection of standard reference datasets.

The following are used to apply FT house style to geographic placenames:

* [Country names and populations](data/countries.csv)
* [US state and country names and populations](data/us-states-counties.csv)
* [EU NUTS units](http://bertha.ig.ft.com/view/publish/dsv/1f5D6R4WDtRSCuBzg9cquSHSEsH_yUOdXGWzmeRo3I_Q/populations.csv)

## How to use

Use the raw CSV view of these files to import them directly into Google sheets:

```excel
=IMPORTDATA("https://raw.githubusercontent.com/Financial-Times/data-journalism-metadata/main/data/countries.csv")
```

or R:

```r
ft_countries <- read_csv("https://raw.githubusercontent.com/Financial-Times/data-journalism-metadata/main/data/countries.csv")
```

## Sources

If you are using any of population figures or classification schemes contained in these files for calculations in a story, you must include sources (and, where possible, links) for these portions of the data:

* The source and year of each country population is shown in the `population_source` field of the `countries` dataset. The default source is the 2019 [World Bank](https://data.worldbank.org/indicator/SP.POP.TOTL) estimates, but there are exceptions for some countries, so make sure you provide a complete list of any exceptions that apply to your story.

* US state and county populations are the [US Census Bureau’s 2019 population estimates](https://www.census.gov/data/datasets/time-series/demo/popest/2010s-counties-total.html). Puerto Rico municipalities data comes from the [US Census Bureau’s 2019 population estimates for Puerto Rico](https://www.census.gov/data/tables/time-series/demo/popest/2010s-detail-puerto-rico-municipios.html). US territory populations reflect those useed in the `countries` dataset.

* EU NUTS population figures come from [Eurostat’s 2020 population estimates](https://ec.europa.eu/eurostat/databrowser/view/DEMO_R_PJANGRP3__custom_96216/default/table?lang=en).
