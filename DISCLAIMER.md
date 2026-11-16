# ⚠️ Disclaimer & Liability Limitation

**Use at your own risk.** The code, workflows, and scripts in this repository (`n8n-hubspot-custom-object-schema-drift-detector`) are provided for educational and architectural demonstration purposes.

## No Liability

The author and dhRobin Systems accept no responsibility or liability for any direct, indirect, incidental, or consequential damages that result from using, misusing, or deploying these scripts. That includes, without limitation:

- schema changes that were not detected, were detected late, or were reported with the wrong severity;
- alerts that were sent, missed, delayed, duplicated or routed to the wrong people or channels;
- decisions to restore, delete, modify or recreate custom objects, properties, options, required flags or associations in response to a finding, including any loss of CRM data that results;
- integration, reporting or automation failures caused by schema changes, whether or not the workflow reported them;
- schema metadata, option values or user identifiers exposed in Slack, webhooks, template files or n8n execution data;
- API quota consumption, rate limiting or account restrictions imposed by HubSpot or Slack.

## No Warranty

All software, n8n JSON blueprints, JavaScript modules and prompts are provided "AS IS", without warranty of any kind, express or implied. This includes, but is not limited to, warranties of merchantability, fitness for a particular purpose, and non-infringement.

The comparison rules, severity levels and thresholds are heuristics. An audit result of `pass` means the parts of your portal described in the template matched it at the time of the run. It is not a certification that your data model is correct, complete or compliant. HubSpot API responses, endpoints, field names, scopes and settings URLs change over time, and I make no warranty that they match what this workflow expects.

## Production Testing Required

Always test thoroughly in an isolated staging environment, such as a HubSpot developer test account or sandbox, with `SANDBOX_MODE=true`, `DRY_RUN=true` and `SEND_SLACK_ALERTS=false` enabled, before you connect live HubSpot or Slack credentials.

Before relying on the audit:

- review every entry in your expected template, and keep it under version control with reviewed changes;
- confirm the token belongs to the intended portal and has the read scopes for every audited object;
- run the audit in dry-run mode and confirm that each reported finding is real;
- send reports to a test Slack channel first;
- unpin every node you expect to run live.

Treat every drift finding as a prompt for a person to investigate, not as an instruction to change or restore a schema. Confirm the cause, the owner and the impact on existing records and integrations before acting on it.

## Third-Party APIs & Compliance

You alone are responsible for complying with the terms of service, rate limits, data privacy regulations (GDPR/CCPA), and security policies of HubSpot, Slack and any connected services. That includes:

- granting only the read scopes the audit needs, and no write scopes;
- securing every access token, template credential and webhook URL;
- keeping personal or confidential data, such as names encoded in option values, out of reports and channels, or restricting access to them;
- having a documented purpose before reporting which user changed a property;
- controlling who can read the expected template and the audit output;
- reviewing every schema change made in response to an alert.

## License

Released under the MIT License. Copyright (c) 2026 DH Robin (dhRobin Systems). See [LICENSE](LICENSE).

---

Full text: DISCLAIMER.md · Licensed under the MIT License. License: MIT © 2026 dhRobin Systems · Provided as-is, see the disclaimer.
