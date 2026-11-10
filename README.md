# Hiring Cafe Jobs Scraper & API - Salary & Visa Sponsorship Jobs

Hiring Cafe jobs scraper and API: search HiringCafe (hiringcafe.com, formerly hiring.cafe), the job search engine built from 6 million jobs on employers' own career sites, live by job title, place, remote or hybrid, posting date, years of experience, seniority, published salary, company size and visa sponsorship, and get each job's title, company, places, work arrangement, job type, seniority, years asked, published pay, tools and skills, requirements, the employer's own apply link and the hiring system it came from, newest first. Turn on full details for the description.

Use it as a HiringCafe API with no login and no API key, a hiring.cafe job scraper, an ATS jobs feed or a daily job alert from the Apify Console, the Apify API, Python, JavaScript, n8n, Make or an AI agent, and export JSON, CSV or Excel. Every row's title holds the words you typed, an employer's every match is read (not only the 4 the site shows), and a pasted HiringCafe search link keeps its filters. Available as an [Apify Actor](https://apify.com/anshumanatrey/hiringcafe-jobs-search). $0.0011 per job, $0.0012 with full details, $0.003 per run start at the default memory.

## What does it do?

- **Searches all of HiringCafe, live.** About 6.2 million open jobs at 186,000 companies (6,172,589 on 2026-11-10), read from HiringCafe's own search at the moment of your run, newest first by the time the employer posted the job.
- **The employer's own apply link on every row.** HiringCafe reads jobs straight from career sites and applicant tracking systems; `applyUrl` is the job's page there, `ats` names the system (Greenhouse, Lever, Workday, Ashby, iCIMS, Taleo, SmartRecruiters, Workable and over 40 more) and `atsJobId` its own ID, for matching against other feeds.
- **Titles that match.** HiringCafe's search box also returns jobs that only mention your words: of its 126,712 jobs for python developer, 1% of the newest had both words in the title. This actor asks HiringCafe's title search for every word in any order, in its singular and plural and as Front-End or Frontend, and checks every title again; Wider match (`searchDescriptions`) gives you the search box's answer instead.
- **Every match of an employer.** HiringCafe's search shows each employer's 4 newest matches and links to the rest. This actor reads that employer's own list whenever its other jobs can still be among the newest you asked for, so a big employer's tenth posting of the day is not lost.
- **Pay as the employer published it.** Pay comes as text and as numbers with its currency and period, only when the employer published it (HiringCafe's own estimates are left out). Minimum yearly pay (`minSalary`) compares hourly and monthly pay as a year's.
- **HiringCafe's reading of each ad, on every row.** Seniority, people manager or not, job function, the least years of experience asked, tools and skills, a one-line requirements summary and visa sponsorship, and the company's headcount, industries, founding year, type, latest funding and headquarters.
- **Places any way people type them.** A city (London, Bangalore or Bengaluru), a state (California, or TX for Texas), a country, a region (EMEA, Europe, LatAm, DACH, APAC) or Worldwide.
- **Checks job links.** Paste HiringCafe job links or IDs, and each comes back open with the job (its description too with full details), closed or not found.

## How is it different from other Hiring Cafe scrapers?

- **Newest first and complete per employer.** The leading Hiring Cafe actors return the site's search as it comes, 4 jobs per employer per search. Here the employer's own list fills in the rest whenever it can change your answer: a 48-hour full stack engineer search on 2026-11-10 returned 108 jobs, including five titles the site's grouped search had hidden.
- **The title matches what you typed.** Every row's title holds every word of one of your lines, so 100 rows for data analyst are 100 data analyst jobs, not jobs that mention data somewhere.
- **Visa sponsorship and company size as filters.** Tick Sponsors visas (`visaSponsorship`) or pick company sizes (`companySize`), and HiringCafe's own search applies them; no other Hiring Cafe actor offers either.
- **Places, regions and other names.** EMEA, LatAm, DACH and other regions, US state codes and Indian cities by their old and new names, besides cities and countries.
- **Clean, flat rows.** One row per job with plain fields, not HiringCafe's nested records: pay as numbers, places as text, skills as a list.
- **No browser, no third-party scraping keys.** It reads HiringCafe's JSON with a browser's TLS and moves to Apify's residential proxy by itself if HiringCafe's Cloudflare challenges the run's address, at no extra cost to you.

## When should I use it?

- **Job seekers and job boards:** new jobs by title, place, pay and seniority every morning, each with the employer's own apply link.
- **Recruiters and staffing firms:** who is hiring for a role right now, at what pay and experience, and on which hiring system.
- **Sales and market research:** companies hiring for a function or a place as a buying signal, with their size, funding and industry.
- **Data teams and AI agents:** one clean feed of jobs from employers' own sites through the API or MCP.

## How much does it cost to scrape Hiring Cafe jobs?

Pay per event: $1.10 per 1,000 jobs, or $1.20 per 1,000 with full details, plus $0.003 per run at the default 512 MB. Apify's free $5 monthly credit covers about 4,400 jobs in runs of 100. Platform usage is included, and there is no monthly fee.

| Event | Price | When it is charged |
|---|---|---|
| Job | $0.0011 | One saved job, and one checked link that is closed or not found |
| Job with details | $0.0012 | One saved job with full details on |
| Run start | $0.003 per GB of memory | Charged by Apify when a run starts: once up to 1 GB and once more for each extra GB, so $0.003 at the default 512 MB |

| Run (default memory) | Cost |
|---|---|
| 100 newest jobs | $0.113 |
| 100 jobs with full details | $0.123 |
| 1,000 jobs | $1.10 |

## How does the price compare with other Hiring Cafe scrapers?

Every actor on the Apify Store whose title or slug names Hiring Cafe and had 4 or more users in the last 30 days, from the Store's own search on 2026-11-10 (34 actors read), ordered by users. Free-plan prices from each actor's current pricing.

| Actor | Users, 30 days | Per job | Start fee | Input |
|---|---|---|---|---|
| memo23/apify-hiring-cafe-scraper | 183 | $0.00125 | $0.005 | Search URLs or filters, salary, years, incremental mode |
| blackfalcondata/hiringcafe-scraper | 149 | $0.00115 | $0.005 | Keyword, 50 country markets, radius, notifications, incremental mode |
| parsebird/hiring-cafe-scraper | 46 | $0.003 | $0.00005 | Keywords and filters, through a browser on a residential proxy |
| corvuslab/hiringcafe-scraper | 8 | $0.00115 | $0.004 | Keyword, location or URL, notifications |
| azzouzana/hiring-cafe-scraper | 7 | $0.001 | $0.005 | A search URL |
| shahidirfan/hiring-cafe-jobs-scraper | 6 | $0.001 | $0.0005 | Keyword or URL, residential proxy |
| fetch_cat/hiring-cafe-jobs-scraper | 5 | $0.0001955 | $0.023 | Listings, apply links, salaries |
| manojachari/hiring-cafe-scraper | 4 | free | none | Keyword and filters |
| This actor | new | $0.0011, $0.0012 with details | $0.003 per GB | Titles, places, pay, seniority, company size, visa sponsorship, live |

Where others are cheaper: azzouzana and shahidirfan charge $0.001 a job and fetch_cat less than $0.0002 a job after a larger start fee, and manojachari is free. Where others do more: blackfalcondata and memo23 track changes between runs and blackfalcondata sends Telegram, Slack and webhook alerts; memo23 and blackfalcondata take a radius around a point and description and technology keywords.

## Which inputs does it take?

Nothing is required. Type a job title and press Start, or press Start with the form empty for the newest jobs of every kind.

| Field | What it does |
|---|---|
| Job titles to find (`searchTerms`) | One per line. A job matches when its title has every word, in any order: frontend also finds Front-End, nurses finds Registered Nurse. A place typed with the title (nurse in California) is searched as the place. A pasted HiringCafe search link works too, with its filters |
| Where the job is (`location`) | Cities, states, countries or regions: London, California, Germany, EMEA, Worldwide. Bangalore and Bengaluru both work. Remote alone asks for remote jobs |
| Remote or office (`workType`) | remote, hybrid or onsite (in person, field work too), as HiringCafe reads every job |
| Posted in the last (`postedWithin`) | 24 hours, 3, 7, 14 or 30 days (the default), any time, or your own period such as 48 hours |
| Experience (`experienceYears`) | Your years: 3, a range such as 2-5, 5+ or fresher. Keeps the jobs whose least years asked fit yours; a job whose ad states none is left out |
| Job level (`seniority`) | no-experience, entry, mid or senior, as HiringCafe rates each job |
| Job type (`employmentType`) | full-time, part-time, contract, intern, temporary (seasonal too) or volunteer |
| Minimum yearly pay (`minSalary`) | The least yearly pay, such as 120000 or 120k: jobs whose published pay reaches it, in the currency below |
| Pay currency (`salaryCurrency`) | USD by default, or EUR, GBP, CAD, AUD, INR or any three-letter code |
| Company size (`companySize`) | Employees, as HiringCafe groups them: 1-10 up to 10001+, or a range such as 1-500 |
| Sponsors visas (`visaSponsorship`) | Only jobs whose ad says the employer sponsors work visas |
| Only these companies (`companies`) | Company names as HiringCafe writes them (OpenAI, Stripe), or a HiringCafe company page link |
| Number of jobs (`maxJobs`) | How many, newest first: 100 by default, 0 for every match |
| Full details (`includeDetails`) | Adds the description as text and HTML, and the city, state and country |
| Leave out words (`excludeTerms`) | Drops jobs whose title has these words, such as senior or intern |
| Wider match (`searchDescriptions`) | Every job HiringCafe's search box finds for your words anywhere in the ad |
| Job links to check (`jobUrls`) | HiringCafe job links or IDs, to check whether they are still open, instead of searching |
| Connection (`proxyConfiguration`) | Off by default: the run moves to Apify's residential proxy by itself when HiringCafe challenges its address. Set one only to use your own |

Example input:

```json
{
  "searchTerms": ["data analyst", "business analyst"],
  "location": ["London", "Remote EMEA"],
  "seniority": ["entry", "mid"],
  "postedWithin": "7 days",
  "maxJobs": 100
}
```

## What does the output look like?

One row per job, newest first. This row is from a local run on 2026-11-10: software engineer, 100 jobs saved in 34 s. A job in several cities shows HiringCafe's place line in `location` and every city in `otherLocations`.

```json
{
  "title": "Software Development Engineer, Amazon Publisher Monetization - Video Ads, Ads - Video Demand - Fixed",
  "company": "Amazon",
  "location": "New York City, New York, United States",
  "otherLocations": [],
  "workType": "onsite",
  "employmentType": "full-time",
  "department": "Software Development",
  "salary": "USD 158,100 - 213,800 per year",
  "postedAt": "2026-11-10T08:07:47.805Z",
  "jobUrl": "https://hiringcafe.com/job/x3mo8glxcf7f8h0o",
  "applyUrl": "https://www.amazon.jobs/en/jobs/10600812/software-development-engineer-amazon-publisher-monetization-video-ads-ads-video-demand-fixed",
  "status": "open",
  "platform": "hiringcafe",
  "companySlug": "amazon.com",
  "companyWebsite": "https://amazon.com",
  "jobId": "x3mo8glxcf7f8h0o",
  "checkedAt": "2026-11-10T11:01:21+00:00",
  "experienceMin": 3,
  "seniority": "Mid Level",
  "roleType": "Individual Contributor",
  "employmentTypes": [
    "full-time"
  ],
  "skills": [
    "C#",
    "C++",
    "Java",
    "Perl"
  ],
  "requirementsSummary": "3+ years non-internship software development experience; 2+ years design/architecture; 1+ years large-scale distributed systems; object-oriented design; Bachelor's in CS, Engineering, Math or related; programming in C#, C++, Java, or Perl.",
  "salaryMin": 158100.0,
  "salaryMax": 213800.0,
  "salaryCurrency": "USD",
  "salaryPeriod": "year",
  "visaSponsorship": false,
  "companySize": 1576000,
  "companyIndustries": [
    "E-Commerce & Online Retail",
    "Data Centers & Cloud Infrastructure",
    "Logistics & Supply Chain Services",
    "Electronics Manufacturing",
    "Holding Companies & Conglomerates"
  ],
  "companyFounded": 1994,
  "companyType": "Public",
  "companyFunding": "IPO",
  "companyHeadquarters": "United States",
  "ats": "adhoc",
  "atsJobId": "10600812"
}
```

Full details add `description`, `descriptionHtml`, `city`, `region` (the state or province), `country` and `countryCode`. A checked link that is not found comes back with its `status` and link, and the other fields empty. A run also writes an `OUTPUT` record: how many jobs HiringCafe listed, how many matched and were saved, any notes on how your input was read, and the calls made.

## How fast is it?

Seconds to a minute for a few hundred jobs. On this laptop on 2026-11-10 (`apify run`, 75 to 84 MB of memory): the form as it opens (100 newest jobs) took 27 s, software engineer 25 s, nurse in California typed in one line (50 jobs) 15 s, registered nurse in California in the last 7 days 28 s, hybrid data analyst jobs in London 16 s (all 50 of the month), 20 remote product manager jobs in the United States with published pay of $150,000 or more and full details 45 s (one more call a job), 10 job links checked 44 s, and a search with no match 5 s. One search page holds about 130 jobs of 40 employers; the employers that show 4 jobs are read further, one call each. 2,000 data analyst jobs took 10 minutes from the laptop's own address (84 calls, 84 MB at the peak): Cloudflare blocked it twice and then challenged it, so the run waited, slowed down and saved the 2,000 newest it had, saying that some employers' lists past their 4 jobs were not read. One address gets about 80 calls 2 seconds apart before HiringCafe's Cloudflare blocks it for a minute or more, so a run without a proxy then waits and goes on 10 seconds a call; on Apify a run moves to the residential proxy at the first block, half a second between calls and a fresh address every 30 calls.

## Common questions

### Is HiringCafe the same as hiring.cafe?

Yes. HiringCafe moved from hiring.cafe to hiringcafe.com, and the old address redirects to the new one. Hiring Cafe Jobs Scraper reads hiringcafe.com and accepts links from both, such as hiring.cafe/job/... and hiringcafe.com/?searchState=....

### Which posting date does it use?

Hiring Cafe Jobs Scraper uses HiringCafe's posting time for each job (`postedAt`): when the employer posted it on its own career site, as HiringCafe read it, to the second. Some career sites give only the day, so their jobs are dated at midnight or noon UTC of that day. Posted in the last (`postedWithin`) is sent to HiringCafe as whole days and every row is checked again here.

### Why do I get fewer jobs than HiringCafe shows?

HiringCafe's search box counts every job that mentions your words anywhere: 126,712 for python developer on 2026-11-10, of which 1% of the newest had both words in the title. Hiring Cafe Jobs Scraper keeps the jobs whose title holds every word, and keeps a job an employer posted twice at one place once, the newest. Tick Wider match (`searchDescriptions`) to get every job the search box finds. A city keeps the jobs that name it: HiringCafe's own city search reaches 50 miles around it, so for London it also lists Reading and St Albans. A run that saves no job says why and how to loosen the search.

### How do places work?

Hiring Cafe Jobs Scraper sends each place to HiringCafe's own search and checks every job again by its places. A city or state is looked up on HiringCafe's list of places, by its other names too: Bangalore is Bengaluru there, Gurgaon is Gurugram, TX is Texas. A country finds jobs in it and remote jobs open across it; a region (EMEA, Europe, LatAm, DACH, APAC, the Nordics) finds jobs in any of its countries; Worldwide finds jobs open everywhere. Remote typed alone asks for remote jobs; pick remote in Remote or office (`workType`) for remote jobs of a place. A place HiringCafe does not know (NYC) is checked by its name on the newest jobs, so type the full name (New York).

### How do I get only jobs above a salary?

Type the least yearly pay in Minimum yearly pay (`minSalary`), such as 150000 or 150k, and its currency in Pay currency (`salaryCurrency`), USD by default. Hiring Cafe Jobs Scraper keeps the jobs whose employer published a pay range reaching it, hourly and monthly pay compared as a year's, as HiringCafe's own pay filter does, and leaves out jobs that publish no pay.

### Does it need a login, an API key or a proxy?

Hiring Cafe Jobs Scraper needs no HiringCafe login and no API key: it reads the same public search any visitor's browser reads. HiringCafe's Cloudflare answers only a browser, so the actor speaks with a browser's TLS, and when Cloudflare challenges the run's own address it moves to Apify's residential proxy by itself, a fresh address at each challenge, at no extra cost to you. You need only an Apify account.

### Does it work on Apify's free plan?

Hiring Cafe Jobs Scraper works on Apify's free plan, which pays $0.0011 a job plus the $0.003 run start at the default 512 MB. The free $5 monthly credit pays for about 4,400 jobs in runs of 100.

### How often should I run it?

Running Hiring Cafe Jobs Scraper once a day keeps a job feed fresh: set Posted in the last (`postedWithin`) to 24 hours and Number of jobs (`maxJobs`) to 0 to get every job of the day for your titles and places. Set it up under Schedules in Apify Console, and match rows on `jobId` to skip jobs you already have.

### How do I get every job of one company?

Type the company's name, as HiringCafe writes it, in Only these companies (`companies`), such as OpenAI or Stripe, or paste its HiringCafe company page link, and set Number of jobs (`maxJobs`) to 0. HiringCafe also lists companies it relates to the one you typed (Stripe brings Paystack); Hiring Cafe Jobs Scraper keeps the company you typed and names the others in its message, so you can add them.

### How do I check a list of job links?

Paste HiringCafe job links or 16-character job IDs into Job links to check (`jobUrls`), one per line, instead of searching. Hiring Cafe Jobs Scraper reads each job's page: an open job comes back with all its fields (its description too with Full details, `includeDetails`), a job HiringCafe marks expired as closed, and a job it no longer has as not found.

### How do I call it from the API, Python, JavaScript, n8n or an AI agent?

Hiring Cafe Jobs Scraper runs from the Apify API, Python, JavaScript, n8n, Make or an AI agent over MCP. Each way uses your Apify token (Apify Console, Settings, API & Integrations) and takes the input as JSON keyed by the field names, such as `searchTerms` and `maxJobs`.

**API.** One call runs the actor and returns its rows (Apify waits up to 300 seconds; for runs of thousands of jobs, use a client below):

```bash
curl -X POST "https://api.apify.com/v2/acts/anshumanatrey~hiringcafe-jobs-search/run-sync-get-dataset-items" \
  -H "Authorization: Bearer <YOUR_APIFY_TOKEN>" \
  -H "Content-Type: application/json" \
  -d '{"searchTerms": ["data analyst"], "location": ["London"]}'
```

**Python** (`pip install apify-client`):

```python
from apify_client import ApifyClient

client = ApifyClient("<YOUR_APIFY_TOKEN>")
run = client.actor("anshumanatrey/hiringcafe-jobs-search").call(run_input={"searchTerms": ["data analyst"]})
for row in client.dataset(run.default_dataset_id).iterate_items():  # apify-client 3+; on 2.x use run["defaultDatasetId"]
    print(row["title"], row["company"], row["location"], row["salary"], row["applyUrl"])
```

**JavaScript** (`npm install apify-client`):

```js
import { ApifyClient } from 'apify-client';

const client = new ApifyClient({ token: '<YOUR_APIFY_TOKEN>' });
const run = await client.actor('anshumanatrey/hiringcafe-jobs-search').call({ searchTerms: ['data analyst'] });
const { items } = await client.dataset(run.defaultDatasetId).listItems();
for (const row of items) console.log(row.title, row.company, row.location, row.salary, row.applyUrl);
```

**n8n and Make.** In n8n, add the Apify node, pick Run an Actor and get dataset, choose this actor and paste the input JSON: the rows come out as n8n items. In Make, the Apify app's Run an Actor and Get Dataset Items modules do the same.

**AI agents (MCP).** Add `https://mcp.apify.com?tools=anshumanatrey/hiringcafe-jobs-search` to your MCP client and sign in with Apify, or send `Authorization: Bearer <YOUR_APIFY_TOKEN>`. The agent gets this actor as a tool and sees every input field by its JSON key.

### Is it legal to use?

Hiring Cafe Jobs Scraper reads public job postings, the pages any visitor sees without logging in. It is not affiliated with HiringCafe. You are responsible for how you use the data, including HiringCafe's terms and the privacy laws that apply to you.

## Limitations

- HiringCafe shows the newest 10,000 employers of one search, about 33,000 jobs: for the whole site that is its newest 12 hours. Narrow a broad search by place, period or words to reach older jobs.
- An employer's own list is read up to 1,000 of its jobs in one search.
- Pay is published on about 1 job in 7 (16 of 100 on the form as it opens); `salary` is empty for the rest.
- Years of experience come from HiringCafe's reading of each ad and are stated on about half the jobs (46 to 60 in 100); with Experience (`experienceYears`) set, a job that states none is left out.
- A few career sites give HiringCafe no place for a job (8 of 100 jobs on the form as it opens, all from one employer); those rows have no `location`, and a place search leaves them out.
- One employer can post the same job on two of its career sites (T. Rowe Price on 2026-11-10); the run keeps it once, the newest.
- HiringCafe keeps no closed jobs in its search, and a job it removed reads as not found when its link is checked.
- HiringCafe's Cloudflare blocks one address for a minute or more after about 80 calls 2 seconds apart. A run on Apify moves to a residential address at the first block; without a proxy it waits a block out (three times at most) and goes on 10 seconds a call, and a fourth block ends the reading with the jobs read so far saved.

## Who maintains it?

Built and maintained by **Anshuman Atrey** ([@AnshumanAtrey](https://github.com/AnshumanAtrey)), who publishes a portfolio of data and OSINT actors on Apify Store. For a feature request or a bug, message [LinkedIn](https://linkedin.com/in/anshumanatrey) (fastest), open an issue on the GitHub repo, or write through [atrey.dev](https://atrey.dev).

## Sibling actors

| Actor | What it searches |
|---|---|
| [Greenhouse Jobs Scraper](https://apify.com/anshumanatrey/greenhouse-jobs-search) | Jobs from every company on Greenhouse, searched live |
| [Lever Jobs Scraper](https://apify.com/anshumanatrey/lever-jobs-search) | Jobs from 2,300+ companies on Lever (jobs.lever.co), searched live |
| [Workday Jobs Scraper](https://apify.com/anshumanatrey/workday-job-search) | Jobs from every company on Workday (myworkdayjobs.com), searched live |
| [Ashby Jobs Scraper](https://apify.com/anshumanatrey/ashby-jobs-search) | Jobs from every company on Ashby (jobs.ashbyhq.com), searched live |
| [SmartRecruiters Jobs Scraper](https://apify.com/anshumanatrey/smartrecruiters-jobs-search) | Jobs from 2,900+ companies on SmartRecruiters, searched live |
| [Workable Jobs Scraper](https://apify.com/anshumanatrey/workable-job-search) | Jobs from every company on Workable, in one search |
| [Cornerstone Jobs Scraper](https://apify.com/anshumanatrey/cornerstone-jobs-search) | Jobs from every company on Cornerstone (csod.com), searched live |
| [Deel Jobs Scraper](https://apify.com/anshumanatrey/deel-jobs-search) | Jobs from every company on Deel ATS (jobs.deel.com), with pay |

For the people behind a company: [LinkedIn Profile Finder](https://apify.com/anshumanatrey/linkedin-harvester) turns an email into a public LinkedIn profile.

## Documentation

- Apify Store: https://apify.com/anshumanatrey/hiringcafe-jobs-search
- GitHub repo: https://github.com/AnshumanAtrey/hiringcafe-jobs-search (MIT license, see [LICENSE](LICENSE))
- The engine behind it: https://github.com/AnshumanAtrey/ats-jobs-engine

## Last updated

2026-11-10 (version 1.0)
