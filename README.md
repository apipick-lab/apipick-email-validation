# apipick-email-validation

A [Claude Code](https://claude.ai/claude-code) skill that validates email addresses using the [apipick](https://www.apipick.com) Email Validator API.

## What it does

Given an email address, this skill performs:

- **Syntax check** — validates format against RFC rules
- **MX record lookup** — confirms the domain can receive email
- **Disposable detection** — flags known throwaway email services
- **Normalization** — returns the canonical lowercase form

An email is considered `valid` only when both syntax and MX checks pass.

## Requirements

An apipick API key is required. Get 100 free credits at [apipick.com](https://www.apipick.com).

## Installation

Install via Claude Code:

```bash
claude skills install https://github.com/apipick-lab/apipick-email-validation
```

## Usage

Once installed, just ask Claude naturally:

- *"Validate the email address user@example.com"*
- *"Is this a real email: test@tempmail.com?"*
- *"Check if john.doe@company.org can receive emails"*

Claude will call the apipick API and report whether the email is valid, deliverable, and if it's from a disposable service.

## API Reference

| Field | Value |
|-------|-------|
| Endpoint | `POST https://www.apipick.com/api/check-email` |
| Auth | `x-api-key` header |
| Cost | 1 credit per request |

See [`references/api_reference.md`](references/api_reference.md) for full documentation.

## Links

- [apipick.com](https://www.apipick.com) — API platform
- [Email Validator](https://www.apipick.com/check-email) — product page
- [Get API Key](https://www.apipick.com/dashboard/api-keys)
