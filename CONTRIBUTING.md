# Contributing to Public Records API Documentation

## Quick Start

### 1. Clone the Repository
```bash
git clone https://github.com/nishi1594/docs.git
cd docs
```

### 2. Install Mintlify CLI (Optional - for local preview)
```bash
npm install -g mintlify
```

### 3. Preview Locally
```bash
mintlify dev
```
Visit `http://localhost:3000` to see your changes.

### 4. Make Changes

Documentation files are in the `docs/` folder:
- `introduction.mdx` - Main landing page
- `authentication.mdx` - Auth guide
- `quickstart.mdx` - Getting started
- `api-reference/` - API endpoints and schemas
- `examples.mdx` - Code examples

### 5. Commit and Push
```bash
git add .
git commit -m "Add/Update: [description of changes]"
git push origin main
```

Mintlify auto-deploys on push to `main` branch.

## File Structure

```
docs/
├── docs.json          # Main config (navigation, branding)
├── mint.json          # Alternative config format
├── introduction.mdx   # Landing page
├── authentication.mdx
├── quickstart.mdx
├── api-reference/
│   ├── overview.mdx
│   ├── endpoints/
│   │   ├── evaluate.mdx
│   │   ├── evaluate-batch.mdx
│   │   ├── identity-match.mdx
│   │   └── health.mdx
│   └── schemas/
│       ├── criminal-record.mdx
│       ├── candidate-info.mdx
│       └── ...
├── examples.mdx
├── error-handling.mdx
└── assets/
    └── custom.css
```

## Adding a New Endpoint

1. Create file: `api-reference/endpoints/your-endpoint.mdx`
2. Add to `docs.json` navigation:
```json
{
  "group": "Endpoints",
  "pages": [
    "api-reference/endpoints/your-endpoint"
  ]
}
```

## Adding a New Schema

1. Create file: `api-reference/schemas/your-schema.mdx`
2. Add to `docs.json` navigation under "Schemas" group

## Writing MDX

Use Mintlify components:
- `<Endpoint>` - API endpoint documentation
- `<Param>` - Parameter documentation
- `<ResponseField>` - Response field documentation
- `<CodeGroup>` - Code examples with tabs

Example:
```mdx
---
title: Your Endpoint
---

<Endpoint method="POST" path="/your-endpoint">

Your description here.

<Param name="param1" type="string" required>
  Parameter description
</Param>

</Endpoint>
```

## Notes

- **Repository**: Currently at `nishi1594/docs` (will move to `theary-ai` org when permissions are granted)
- **Auto-deploy**: Changes to `main` branch deploy automatically
- **Preview**: Use `mintlify dev` to preview locally before pushing

## Questions?

Contact: support@theary.ai

