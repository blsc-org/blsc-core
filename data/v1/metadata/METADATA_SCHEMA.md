# BLSC Metadata Schema (v1)

This document defines the required and optional fields for metadata used in the Bulgarian Language & Script Corpus (BLSC).

The official validation schema is located at:
/data/v1/metadata/schema.json
### Required fields
- `document_id`
- `title`
- `source`
- `license`
- `language` (always "Bulgarian")
- `genre`
- `domain`

### Optional fields
- `author`
- `year`
- `tokens`
- `sentences`
- `notes`

The schema follows **JSON Schema Draft 2020-12** and guarantees consistent metadata across all dataset modules.
