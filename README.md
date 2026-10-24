# COAL AI — Нүүрс тээврийн удирдлага

Source snapshot of the existing application: https://ai-08x6fu.v2.appdeploy.ai/

## Provenance

- AppDeploy application ID: `ai-08x6fu`
- Imported source version: `1790670840277`
- Export date: 2026-10-24
- This repository is a source copy. It does not automatically deploy to production.

## Contents

- `src/main.ts`, `src/styles.css`: Vite/TypeScript frontend.
- `backend/index.ts`: AppDeploy backend routes, authentication, AI and database access.
- `public/resources/`: the two existing application image assets.
- `appdeploy.auth-login.json`: Google login presentation configuration.
- `tests/tests.txt`: existing platform test scenarios.

## Runtime requirements

The application uses `@appdeploy/client` and `@appdeploy/sdk`, supplied by the AppDeploy environment. The exported package.json is preserved as deployed. A standalone checkout is not a complete local backend: do not assume `npm run dev` provides authentication, AI, database or storage services. Use the existing AppDeploy application for full-runtime validation. A portable local development adapter can be added separately.

## Data preservation

No registered-user records, attachments, database exports, login tokens or secret values are included. The two images are existing application artwork, not user attachments.

The backend stores records under keys such as `vehicles:<userId>` and `trips:<userId>`. Preserve authentication IDs, table keys, storage paths and the existing AppDeploy app ID when making future updates. Moving code to GitHub does not migrate the database.

Do not execute seed/reset or migration routines while reviewing. `/api/me` has membership/access-log side effects even though it is a GET endpoint. Administrator configuration is part of the original source and has not been changed.

## Development workflow

1. Make source changes in a branch and review the diff.
2. Validate in an isolated environment using synthetic data.
3. Review data preservation and authentication before updating the existing AppDeploy app.
4. Do not create a replacement production application or change the database as part of source synchronization.

Existing demo data and incomplete features are preserved in this initial import; this commit does not claim to repair the application.
