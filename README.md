# EverTrust Tender Intelligence

Standalone procurement-intelligence platform for Sudan. This repository is independent from the EverTrust corporate website.

## Core
- Next.js App Router + TypeScript
- Source registry
- Tender normalization and deduplication
- EverTrust relevance scoring
- Deadline intelligence
- Vercel Cron trigger
- Server-side secrets only

## Security
- No credentials in source control.
- Cron endpoint accepts Bearer CRON_SECRET when configured.
- Client routes never expose secrets.
- Public/authorized source access only; source terms and robots policies must be respected.
- Original tender documents remain authoritative.
- Search-engine indexing is disabled.

## Production data layer
The application is structured so a managed Postgres database can be connected through server-only environment variables. Persistence should cover sources, tenders, documents, crawl runs, matches and alerts.

## Sources
Initial registry: SudanBid, UNGM, UNHCR, UNDP, WHO, WFP, UNICEF, FAO, UNOPS, IOM and an extensible NGO/INGO registry.

## Deployment
Use a dedicated Vercel project. Configure CRON_SECRET and database/notification credentials in Vercel Environment Variables. Never commit .env files.

## Principle
The system can expand toward broad coverage of publicly accessible Sudan procurement notices; it cannot truthfully guarantee every tender on the internet because some opportunities are private, portal-restricted, offline, or distributed through non-public channels.
