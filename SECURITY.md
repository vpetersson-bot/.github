# Security Policy

This document describes how to report a security vulnerability in an sbomify project and what happens after you do. It is the default policy for the [sbomify GitHub org](https://github.com/sbomify) and applies to every repository that does not publish its own, as well as to the hosted platform at [app.sbomify.com](https://app.sbomify.com).

**Our canonical security contact record is [`security.txt`](https://trust.sbomify.com/.well-known/security.txt), published on the [sbomify trust center](https://trust.sbomify.com) per [RFC 9116](https://www.rfc-editor.org/rfc/rfc9116).** Where this document and `security.txt` ever disagree about how to reach us, `security.txt` is authoritative.

- [Reporting a Vulnerability](#reporting-a-vulnerability)
- [What Happens Next](#what-happens-next)
- [Disclosure Policy](#disclosure-policy)

## Reporting a Vulnerability

The sbomify team takes all security vulnerabilities seriously. Thank you for improving the security of our software. We appreciate your effort and your responsible disclosure, and we will make every effort to acknowledge your contribution.

**Report security vulnerabilities by emailing the sbomify security team at [security@sbomify.com](mailto:security@sbomify.com).**

Please tell us which repository or service is affected, what you found, how to reproduce it, what you believe the impact is, and include any proof of concept you have. Timestamps in UTC help us line your report up against our own logs.

That address is the one published in the `Contact` field of [`security.txt`](https://trust.sbomify.com/.well-known/security.txt). **To encrypt your report, use the OpenPGP key its `Encryption` field points to** — we deliberately do not repeat the key URL here, so that there is one place to change it.

Please report vulnerabilities in third-party modules to the person or team maintaining the module.

## What Happens Next

sbomify is a small team. We would rather describe how we actually work than publish a response clock we cannot hold to.

- We acknowledge every report, and we tell you the outcome — including when we conclude that what you found is not a vulnerability.
- We triage on whether an issue is being exploited and whether it is reachable from the Internet, rather than on score alone. That judgement sets the remediation deadline under our internal vulnerability management policy, which we share with customers and assessors on request.
- An actively exploited vulnerability is handled as a security incident rather than as a routine ticket, with the escalation that implies.
- We will keep you informed of progress towards a fix and an advisory, and we may come back to you for more information or guidance.

Reporting in good faith is never held against the person reporting, including where the finding turns out to be nothing.

## Disclosure Policy

When we receive a security report, one person takes ownership of it and coordinates the fix and the release:

- Confirm the problem and determine which versions and deployments are affected.
- Audit the surrounding code for similar problems.
- Prepare the fix. For [app.sbomify.com](https://app.sbomify.com) a fix reaches you when we deploy it; for anything you run or install yourself it ships in a new release of the affected project.
- Publish an advisory on the [sbomify trust center](https://trust.sbomify.com/advisories/) once a fix is available. We publish through sbomify's own security advisory feature rather than GitHub's, and our public API serves each published advisory as a CSAF 2.0 document as well as JSON.

Please give us a reasonable opportunity to fix an issue before disclosing it publicly. We will credit you in the advisory unless you would rather we did not.

sbomify does not currently run a paid bug bounty programme.
