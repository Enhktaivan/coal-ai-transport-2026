# Existing COAL AI application

Production app: https://ai-08x6fu.v2.appdeploy.ai/
AppDeploy app_id: ai-08x6fu
Imported source version: 1790670840277

The user requires preserving the existing registered user's data.
- This is a source checkout, not a database backup or a local running deployment.
- Use AppDeploy source tools for this exact app. Do not substitute coal-ai-transport-2026 or ai-pdync3.
- Preserve app_id, authentication user IDs, userTable naming, existing table keys and storage paths.
- Do not run seed, migration, reset, role update, invitation or business-record writes during inspection.
- GET /api/me currently writes membership/access logs; do not treat it as a side-effect-free inspection endpoint.
- Do not change administrator allowlists as part of connecting source.
- Review and verify data-preservation before any future deployment. No deployment was performed by this import.
- public/resources binary assets remain in AppDeploy and are not copied locally. Preserve them when updating the existing app.
