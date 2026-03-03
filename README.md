# Augno OpenAPI Specification

This repository contains the [OpenAPI specification](https://www.openapis.org/) for the [Augno API](https://docs.augno.com).

The spec files are automatically synced from Augno's internal API on every release. Each update is tagged with a version and published as a [GitHub Release](https://github.com/Augno/openapi-spec/releases).

## Directory Structure

### `/latest/` — Generally Available (GA) Specifications

The latest generally available (GA) release, containing OpenAPI specifications for Augno's stable API endpoints.

Use these files to generate SDKs or client libraries against Augno's production API.

### `/preview/` — Preview Release

The latest public preview release. Use these files for early access to upcoming API features before GA release.

To learn more about public preview and other release phases, see [Augno's release phases](https://docs.augno.com/release-phases).

## Usage

Download the spec directly via raw URL:

```
# Preview
https://raw.githubusercontent.com/Augno/openapi-spec/main/preview/openapi.json

# GA (coming soon)
https://raw.githubusercontent.com/Augno/openapi-spec/main/latest/openapi.json
```

Or clone the repo:

```bash
git clone https://github.com/Augno/openapi-spec.git
```

Pin to a specific version using [release tags](https://github.com/Augno/openapi-spec/releases):

```bash
git checkout 1.0.forge-preview.1-rev.3
```

## Versioning

Each spec update creates a GitHub Release with a tag in the format `{api_version}-rev.{N}`:

- **API version** is extracted from the spec's `info.version` field (e.g., `1.0.forge-preview.1`)
- **Revision** is a per-version counter that increments with each sync (e.g., `-rev.1`, `-rev.2`)
- When the API version changes, the revision counter resets to 1

## License

[MIT](LICENSE)
