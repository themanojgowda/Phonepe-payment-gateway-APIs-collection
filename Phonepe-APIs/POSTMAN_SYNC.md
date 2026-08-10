# Postman Sync Workflow

Use this at each restart to keep workspace files in sync with your latest Postman changes.

## Steps

1. In Postman, export the collection as v2.1 JSON.
2. Save it over:
   - phonepe-tsp-webhooks.collection.json
3. Export each environment and save over:
   - phonepe-tsp-sandbox.environment.json
   - phonepe-tsp-production.environment.json
4. Ask Copilot: sync tsp from latest collection.

## Why this is needed

Copilot does not have direct live access to your Postman desktop app state.
So changes made only inside the app must be exported once to files before local sync can happen.

## What Copilot will do after export

- Diff the new collection/environment files
- Regenerate files under tsp/
- Keep naming and scripts aligned
- Preserve your current repository structure
