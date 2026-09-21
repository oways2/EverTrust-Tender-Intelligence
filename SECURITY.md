# Security Policy

## Reporting a vulnerability

Please do not disclose security vulnerabilities publicly. Report suspected issues privately to the repository owner through GitHub.

## Secrets

Never commit:
- database credentials
- API keys
- notification tokens
- authentication passwords
- CRON_SECRET values
- OAuth credentials

Use Vercel Environment Variables for production secrets.

## Data handling

The application is intended to process public procurement notices. Original source documents remain authoritative and should be verified before any commercial action.
