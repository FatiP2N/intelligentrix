# About Intelligentrix

Intelligentrix is a free platform for bibliometric analysis and technology watch. It maps the scientific output and patents of a topic, a country or a set of files, using open databases and your own exports.

## Get started in three steps

1. Pick a tab: **Live search** (OpenAlex publications), **Patents** or **Import and merge** (your Web of Science, Scopus or Publish or Perish exports).
2. Enter your criteria: a topic, one or more countries, a period, then **Analyze**.
3. Read the indicators, map, ranking and networks; copy tables as CSV for your reports.

## Live search

Publications come from **OpenAlex**, an open database of more than 300 million documents. The topic is searched in titles and abstracts; leave it empty to analyze a country's whole output.

- **Countries**: add one or more. A single country shows its **world rank** and share of world output; the map panel switches between the world ranking and **partner countries** (co-publications).
- **Compare with**: a second topic or country, drawn on the annual chart.
- **Map**: click a country (or a ranking row) to open its profile.
- **Auto refresh**: reruns the analysis every 5, 15 or 60 minutes.

## Patents

Filter by keywords, by **CPC** or **IPC** code (for example `H10K` or `Y02E10/549`, several codes separated by commas), by **applicant** and by **jurisdiction** (publishing office: Morocco, European Patent Office, WIPO…). Data comes live from the EPO; without a keyword, the tab shows all patents published in the most recent year, and the world map fills in progressively because the EPO limits searches per minute. Applicants, their countries, classification and networks are computed on the records of the first 100 families returned by the EPO. The **View sample** button shows a real Espacenet export (100 families on seawater desalination). EPO counts are **publications** (an invention published in five offices counts five times); the Espacenet sample is counted in **families**. The EPO does not provide legal status in aggregate form, so it is not shown.

- **Priority country**: country of first filing, which shows where the invention comes from.
- **Protection countries**: offices where the patent family is published.
- **Publishing office**: office that published each document.
- **Classification**: grouped by subclass (H10K), group (H10K30) or subgroup (H10K30/50); click a bar to filter.

## World Bank

The **World Bank** tab queries the free World Bank API (World Development Indicators) live. Choose an indicator (R&D spending, researchers, patents, scientific articles, high-technology exports, GDP, education, energy, water…) or enter any World Bank code, then the countries to compare and the period. The tab shows the trend by country with the world value as a dotted line, a map and a world ranking based on each country's latest available value, and the official definition of the indicator. Data can be downloaded as CSV.

## Import and merge

Drop one or more exports; the site recognizes each file's database. Duplicates are matched by DOI, then by title, year and first author, then by title and year when a record has no DOI. Titles that are only similar are listed for review, never merged automatically. The merged corpus can be downloaded as CSV. **Your files never leave your browser.**

- **Web of Science**: Export → “Tab delimited file”, record content “Full Record”.
- **Scopus**: select all, Export → CSV with citation, bibliographical, abstract and keyword information.
- **Publish or Perish**: save the results as CSV (Google Scholar, Crossref, OpenAlex…).

**Scopus and Web of Science via API**: with their own key (field in “Sources & API keys”), anyone can query Scopus or Web of Science Starter from the Import and merge tab; results are merged with the imported files. Keys stay in the browser; Web of Science goes through the site's proxy, without being stored. Nothing is stored or republished by the site, and each user remains responsible for using their key under their institution's license.

## Reading the networks

The networks follow VOSviewer's principles. Each **node** is a keyword, country, author, institution, code or applicant; its size reflects the number of documents. A **link** joins two items that appear in the same documents; its width reflects the number of shared documents. **Colors** show either clusters of closely linked items (Louvain method) or the **average year** of the documents, to spot emerging topics.

## Indicator definitions

- **h-index**: h publications each cited at least h times.
- **g-index**: the g most cited publications total at least g² citations.
- **m-quotient**: h-index divided by the number of years since the first publication (here: since the start of the selected period).
- **Citations per publication**: average number of citations received per publication. In Live search, when the corpus exceeds 200 publications, the average is estimated on 1,000 randomly drawn publications (sign ≈).
- **Where to see them**: the h-index and citations per publication are among the key figures; the g-index and the m-quotient are computed in the Import and merge tab (“Citation indicators” panel).
- **Full counting**: a publication counts once for each of its authors' countries, so country totals exceed the overall total.
- **World share**: the country's publications divided by world publications with a known country.
- **Open access**: gold (open journal), hybrid (open article in a subscription journal), green (repository copy), bronze (free to read without a license), diamond (no reading or publishing fees).
- **Patent family**: all publications of the same invention across patent offices.

## Sources and limits

- **OpenAlex** (CC0 license): broad coverage, but affiliations and countries are sometimes missing; a free key raises the request volume.
- **Patents**: EPO Open Patent Services (free once the account is approved) and Lens.org, under their terms of use. Only aggregated counts are shown.
- **Scopus and Web of Science**: through your exports (analyzed locally) or by API with your own key, in the Import and merge tab. **Crossref** (open) can be queried there too.
