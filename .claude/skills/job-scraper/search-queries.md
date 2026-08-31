# Search Queries for Job Scraper

## Installed portal CLIs (primary for `/scrape`)

`/scrape` discovers every portal skill under `.agents/skills/*/SKILL.md` and runs its CLI first. Shipped country-agnostic CLIs include `linkedin-search` and `freehire-search`; Danish demos and any skill you add with `/add-portal` are included the same way. You do **not** need a matching `site:` line below for those CLIs to run.

The `site:` query templates in this file are the **WebSearch fallback** — for portals without a CLI, company career pages, or when a CLI fails.

**Language scope:** English native, Spanish intermediate. Danish portal skills (jobindex, jobnet, jobdanmark, jobbank) are **enabled**. A posting that requires Danish (or Malay, or any other undeclared language) as a job condition fails the Language Gate.

## Search Sites

Primary:
- **jobs.exxonmobil.com** - ExxonMobil careers (Malaysia / KLTC geoscience)
- **linkedin.com/jobs** - LinkedIn; covered by `linkedin-search` CLI (`-l "Kuala Lumpur, Malaysia"` or `-l "Brisbane, Queensland, Australia"`)
- **seek.com.au** - Australian operator and service-company geoscience
- **freehire.me** - tech-adjacent only; weak for geoscience, keep as a secondary CLI
- **jobindex.dk / jobnet.dk / jobdanmark.dk / jobbank.dk** - Danish portals (enabled); use `geolog`, `geofysiker`, `olie`, `reservoir`, `geoscientist`

Secondary (company career pages via Google):
- Direct Google searches with `site:` filters for Santos, ExxonMobil, Woodside, Shell, PETRONAS, Hess, ConocoPhillips

## Query Categories

### Priority 1: Development geoscience on producing assets

These match the strongest career direction.

```
site:jobs.exxonmobil.com Geoscientist "Kuala Lumpur"
site:linkedin.com/jobs "Development Geologist" Kuala Lumpur
site:linkedin.com/jobs "Geoscientist" "Kuala Lumpur" development
site:seek.com.au "Development Geologist" Brisbane OR Adelaide
"reservoir characterization" geologist "Kuala Lumpur"
```

### Priority 2: Cooper Basin / operations geology / geosteering

```
site:linkedin.com/jobs geosteering OR "wellsite geologist" OR "operations geologist" Australia
site:linkedin.com/jobs "Cooper Basin" geologist
site:seek.com.au geomechanics geologist Brisbane
site:jobs.exxonmobil.com "Petroleum Engineer" "Kuala Lumpur"
```

### Priority 3: Adjacent subsurface (reservoir, production, geomechanics)

```
site:linkedin.com/jobs "Reservoir Engineer" "Kuala Lumpur" geoscience
site:jobs.exxonmobil.com "Reservoir Engineer" "Kuala Lumpur"
site:linkedin.com/jobs geomechanics "Kuala Lumpur" OR Brisbane
```

### Priority 4: Broader technical / digital subsurface

```
site:linkedin.com/jobs "subsurface" Python Petrel Australia
site:linkedin.com/jobs "development geologist" Petrel
```

## Location Filter

- **Ideal:** Kuala Lumpur (ExxonMobil KLTC / geoscience support to global producing assets); Brisbane
- **Acceptable:** Other Malaysia ExxonMobil sites; Adelaide; Perth (operator geoscience)
- **Borderline:** Singapore or Bangalore geoscience hubs (relocation stretch)
- **Too far / skip:** Purely IT / network / cyber roles in KL even if they are ExxonMobil; roles that require Malay as a job condition
- **Denmark (Jobindex / Jobnet / Jobdanmark / Jobbank):** FLAG relocation — user asked to include these portals; do not silently drop Danish listings, but mark Denmark as a relocation stretch vs Brisbane / Kuala Lumpur

Relocation from Brisbane to Kuala Lumpur is **accepted**, not a deal-breaker.

## Language Filter

English native, Spanish intermediate. Apply `04-job-evaluation.md` Language Gate. A posting that requires Malay (or any undeclared language) as a job condition is excluded.

## Date Filter

Only include jobs posted within the last 14 days, or with an application deadline that has not yet passed. If a posting date cannot be determined, include it but flag as "date unknown".

## Adapting Queries

If the user specifies a focus area, select queries from the matching category and also generate 2-3 custom queries for that focus.
