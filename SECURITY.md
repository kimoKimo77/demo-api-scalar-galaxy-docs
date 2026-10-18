# Security Policy

## Scope

This repository contains Scalar documentation configuration, MDX pages, and an OpenAPI description for the fictional Scalar Galaxy demo. It is not, by itself, an API server or an identity provider.

## Important authentication distinction

The `security` declarations in `docs/api-reference/openapi.yaml` describe authentication schemes to API documentation and client tooling. They do **not** enforce authentication or authorization on a running service. The demo server must independently validate credentials, enforce authorization for each operation, and apply rate limits and input validation. Do not treat a public documentation page or an OpenAPI security declaration as a security boundary.

## Reporting a vulnerability

Please do not publish credentials, access tokens, private keys, or exploitable details in a public issue. Contact the repository maintainer privately through GitHub to coordinate a report. Include the affected path, impact, and steps to reproduce, while avoiding real user data.

## Secret handling

- Never commit real API keys, bearer tokens, passwords, signing keys, or production environment files.
- Use GitHub Actions secrets or the deployment platform's secret manager for deployment credentials; grant workflows only the permissions they require.
- If a credential is exposed, revoke or rotate it immediately. Removing it from the latest commit alone does not invalidate it.
- Use synthetic credentials and fictional data in examples and tests.
