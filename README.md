# NY HELPS Agency Directory

[![Live site](https://img.shields.io/badge/live-frankstop.github.io%2FAgencyDirectory-0d6b5f)](https://frankstop.github.io/AgencyDirectory/)
[![GitHub Pages](https://img.shields.io/badge/published-GitHub%20Pages-222222)](https://frankstop.github.io/AgencyDirectory/)
[![Agencies](https://img.shields.io/badge/agencies-53-blue)](https://frankstop.github.io/AgencyDirectory/)
[![Links](https://img.shields.io/badge/links-official%20agency%20%2B%20careers-green)](https://frankstop.github.io/AgencyDirectory/)

Searchable public directory for New York State agency homepages and hiring routes.

Live page: <https://frankstop.github.io/AgencyDirectory/>

## What It Does

- Lists 53 New York State agencies from a May 2026 NY HELPS agency set.
- Provides official agency homepage links.
- Provides direct careers links when available.
- Falls back to StateJobsNY when agency hiring routes through statewide postings.
- Lets readers search by agency name, acronym, URL, or link note.
- Supports grid/list views and light/dark display.
- Publishes as a static GitHub Pages site.

## Reader Use Case

This repo is for public-sector job research. It helps a reader move from an agency acronym or agency name to an official hiring destination without hunting through scattered state sites.

## Site Contract

Tracked files are static and public:

```text
index.html
assets/logo.svg
robots.txt
sitemap.xml
.nojekyll
README.md
```

Directory entries live inside `index.html`. Each agency row contains:

- agency acronym
- full agency name
- official homepage URL
- careers or StateJobsNY URL
- short link note

## Source Boundary

Use official agency websites and official New York State hiring routes. Do not add job-board mirrors, scraped listings, or unofficial aggregators as directory destinations.

The page links out to hiring destinations. It does not store applications, personal profile data, salary targets, resumes, or private job-search notes.

## Run Locally

```bash
python3 -m http.server 8000
```

Open:

```text
http://localhost:8000
```

## Publish

This repo is built for GitHub Pages from the repo root.

Required public files:

```text
index.html
.nojekyll
assets/logo.svg
robots.txt
sitemap.xml
```

After pushing to `main`, publish with GitHub Pages using the root folder.

## Update An Agency

Edit the `agencies` array in `index.html`.

Entry shape:

```js
["OASAS", "Office of Addiction Services and Supports", "https://oasas.ny.gov/", "https://oasas.ny.gov/jobs", "Direct careers page"]
```

Keep notes short and consistent:

- `Direct careers page`
- `Direct employment page`
- `Direct jobs page`
- `StateJobsNY hiring route`

## Verification

Before publishing:

1. Run the site locally.
2. Search by an acronym such as `ITS`.
3. Search by a full name such as `Department of Health`.
4. Switch grid/list view.
5. Toggle dark mode.
6. Open one agency site link and one careers link.

## Maintenance Notes

- Check links when agency sites move or rename pages.
- Prefer direct agency career pages when present.
- Keep StateJobsNY fallbacks for agencies without direct hiring pages.
- Keep the README aligned with the visible count on the live page.
