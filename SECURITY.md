# Security Policy

## Supported Versions

This repository is a guide for displaying a local Grafana dashboard as a Windows desktop wallpaper using Lively Wallpaper.

Only the latest version of the guide is supported.

| Version | Supported |
| ------- | --------- |
| Latest release / `main` | Yes |
| Older versions | No |

## Security Scope

This project does not ship a backend service, authentication system, agent, exporter, or network-facing application. The main security risk comes from how Grafana is configured and exposed by the user.

Security reports are useful if they involve:

- Instructions in this repository that could accidentally expose Grafana to the public internet.
- Unsafe Grafana configuration examples.
- Recommendations that could leak dashboards, metrics, hostnames, internal URLs, API keys, tokens, or other sensitive data.
- Malicious or compromised links, screenshots, assets, or external references.
- Documentation that encourages unsafe permissions or weak access control.

## Important Grafana Warning

The guide shows how to enable anonymous access in Grafana so a dashboard can be loaded automatically by Lively Wallpaper.

Anonymous access should only be used in a trusted local environment, such as:

- `localhost`
- a private home LAN
- a locked-down internal network

Do not expose a Grafana instance with anonymous access to the public internet.

If Grafana is reachable from outside your trusted network, use proper authentication, firewall rules, reverse proxy restrictions, VPN access, or another access-control layer. A wallpaper setup is not a reason to remove authentication from a public monitoring system.

## Not Considered Vulnerabilities

The following are not considered vulnerabilities in this repository:

- Someone viewing a dashboard that the user intentionally configured as anonymously accessible.
- Lively Wallpaper loading the dashboard URL as configured by the user.
- Grafana security issues that belong to the upstream Grafana project.
- Browser, WebView, or Windows behavior controlled by Lively Wallpaper or the operating system.
- Local users on the same Windows account viewing the wallpaper.
- A dashboard exposing sensitive metrics because the user chose to display them.

## Reporting a Vulnerability

Please do not include secrets, tokens, private dashboards, internal hostnames, or sensitive screenshots in a public issue.

Preferred reporting method:

1. Use GitHub private vulnerability reporting if it is enabled for this repository.
2. If private reporting is not available, open a GitHub issue with a minimal description and no sensitive details.

Include:

- A clear explanation of the security issue.
- The affected section of the guide.
- Why the current instruction is unsafe.
- A safer suggested replacement, if possible.

## Expected Response

Security reports will be reviewed on a best-effort basis.

If the report is valid, the documentation will be updated to reduce the risk of unsafe Grafana exposure or accidental disclosure of sensitive monitoring data.

## Security Responsibility

Users are responsible for securing their own Grafana instance, dashboards, data sources, network exposure, firewall rules, and authentication settings.

This repository provides setup guidance only. It does not make Grafana, Lively Wallpaper, Windows, or any exposed dashboard secure by itself.
