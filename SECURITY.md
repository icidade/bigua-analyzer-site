# Security Policy

## Supported Versions

| Version | Supported |
| ------- | --------- |
| latest (main) | ✅ |

## Reporting a Vulnerability

If you discover a security vulnerability in this project, please **do not** open a public GitHub issue.

Instead, report it privately via one of the following channels:

1. **GitHub Private Security Advisory** — use the [Report a vulnerability](../../security/advisories/new) button on the Security tab of this repository.
2. **Email** — send details to the maintainer listed in the repository profile.

Please include:
- A description of the vulnerability and its potential impact
- Steps to reproduce or proof-of-concept (if applicable)
- Any suggested mitigations

You can expect an initial response within **72 hours** and a resolution or status update within **14 days**.

## Security Measures in Place

- **Content-Security-Policy** meta tag: restricts resource loading to prevent XSS and data injection.
- **X-Content-Type-Options: nosniff**: prevents MIME-type sniffing.
- **Referrer-Policy: strict-origin-when-cross-origin**: limits referrer information sent to third parties.
- **frame-ancestors 'none'**: prevents the site from being embedded in iframes (clickjacking protection).
- **form-action 'none'**: blocks unexpected form submissions.
- **No external dependencies**: the site is pure HTML/CSS with no third-party scripts or CDN resources, minimising the supply-chain attack surface.
- **Dependabot**: enabled for GitHub Actions to keep CI dependencies up to date.

## Branch Protection

The `main` branch is protected. All changes must be submitted via a pull request and pass CI checks before merging.
