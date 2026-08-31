# OpenWeather Collection

Collection of Bruno API tests for OpenWeather-style endpoints.

Prerequisites

- Node.js and npm
- Bruno CLI (`@usebruno/cli`) — installed with `npm install -g @usebruno/cli`

Quick start (local)

1. Install Bruno CLI if needed:

```bash
npm install -g @usebruno/cli
```

2. Provide your OpenWeather API key locally:

```bash
export OPENWEATHER_API_KEY=your_real_key_here
```

3. Run the full collection from the repo root:

```bash
bru run . --env environment-variables
```

Run a folder or single request for faster feedback:

```bash
bru run weather-stations-api --env environment-variables
bru run weather-stations-api/crud-tests/01-register-station.yml --env environment-variables
```

CI (GitHub Actions)

This repository includes CI workflows:

- GitHub Actions workflow: `.github/workflows/openweather-api-tests.yml` (runs Bruno tests).
- Azure Pipelines: `azure-pipelines.yml` (optional lint step).

Make sure to add `OPENWEATHER_API_KEY` as a repository secret for GitHub Actions.

Pushing workflow files to GitHub may require a PAT with the `workflow` scope when using an OAuth token. Alternatively push via SSH which does not require the `workflow` scope.

Troubleshooting

If Bruno reports `Invalid URL: {{baseUrl}}/...`, ensure `environments/environment-variables.yml` exists and that `OPENWEATHER_API_KEY` is set in your environment. This collection's environment file reads the key using `value: "{{env.OPENWEATHER_API_KEY}}"`.
