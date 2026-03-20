# Naukri Jobs Feed

Extract structured job listings from naukri.com — India's largest job portal with 100M+ registered users. Includes detail enrichment, salary data, AmbitionBox ratings, incremental monitoring, and compact output for AI-agent workflows.

Available on:
- **Apify:** https://apify.com/blackfalcondata/naukri-jobs-feed

## Example request

Run the actor via the Apify API:

POST https://api.apify.com/v2/acts/blackfalcondata~naukri-jobs-feed/runs

Example input:
```json
{
  "keyword": "python developer",
  "location": "Bangalore",
  "maxResults": 50,
  "fetchDetails": true
}
```

## Example response
```json
{
  "jobId": "180326019917",
  "title": "Python Software Developer",
  "companyName": "HCLTech",
  "companyId": 4263814,
  "experienceText": "6-10 Yrs",
  "minimumExperience": 6,
  "maximumExperience": 10,
  "salary": "25-30 Lacs PA",
  "salaryMin": 2500000,
  "salaryMax": 3000000,
  "salaryCurrency": "INR",
  "location": "Hyderabad, Bengaluru",
  "skills": ["GCP", "Google Api", "Python", "SQL", "Rest API"],
  "createdDate": "2026-03-19T14:37:16.515Z",
  "portalUrl": "https://www.naukri.com/job-listings-python-software-developer-hcltech-hyderabad-bengaluru-6-to-10-years-180326019917",
  "industry": "IT Services & Consulting",
  "ambitionBox": {
    "url": "https://www.ambitionbox.com/reviews/hcl-technologies-reviews",
    "rating": "3.4",
    "reviewsCount": 45343
  },
  "description": "<p>Primary skills (Mandatory)...</p>",
  "roleCategory": "IT & Information Security - Other",
  "employmentType": "Full Time, Permanent",
  "vacancy": 1,
  "applyCount": 352,
  "scrapedAt": "2026-03-20T20:35:00.000Z",
  "searchKeyword": "python developer"
}
```

## Key features

- Keyword search with location, experience, and salary filters
- Structured salary data: min, max, currency (INR)
- AmbitionBox company ratings and review counts
- Full job description and education requirements via detail enrichment
- Direct job ID lookup (skip search, fetch specific jobs)
- Incremental mode for scheduled monitoring (new/changed jobs only)
- Compact output mode for AI-agent and MCP workflows
- Description truncation for token budget control
- Work-from-home / remote filter
- Freshness filter (jobs posted within N days)

## Filters

- Keyword (job title or skill)
- Location (city)
- Minimum / maximum experience (years)
- Salary range (lakhs per annum)
- Work from home only
- Posted within N days (freshness)

## Pricing

- $0.005 per run start
- $0.002 per job listing

## Use cases

- Job market intelligence for Indian tech sector
- Recruitment and staffing pipeline
- Salary benchmarking across roles and locations
- Sales intelligence and lead generation
- Competitor hiring monitoring
- Academic labour market research

## Documentation

Full documentation, input/output reference, and sample output:
https://apify.com/blackfalcondata/naukri-jobs-feed

## Related

- [StepStone Jobs API](https://github.com/BlackFalconData-org/stepstone-jobs-api) — search and extract job listings from 18 StepStone Group portals
- [Arbeitsagentur Jobs Feed](https://github.com/BlackFalconData-org/arbeitsagentur-jobs-feed) — extract job listings from Germany's federal employment portal
- [Indeed Jobs Feed](https://github.com/BlackFalconData-org/indeed-jobs-feed) — extract job listings from Indeed
- [Glassdoor Jobs Feed](https://github.com/BlackFalconData-org/glassdoor-jobs-feed) — extract job listings from Glassdoor
- [Company Jobs Tracker](https://github.com/BlackFalconData-org/company-jobs-tracker-api) — track new and removed job listings per company
