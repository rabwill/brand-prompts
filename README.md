# Brand Image Prompts (Test Repo)

A small test repository of image-generation prompts and brand style guidance for the fictional brand **Kestrel & Co.** (ceramic mugs and coffee gear).

Used to test a Microsoft 365 Copilot connector that ingests GitHub repository files.

## Structure

- `prompts/` - one markdown file per prompt, with YAML front matter
- `brand-guidelines/` - style rules the connector can also ingest

## Front matter fields

| Field | Example | Notes |
|---|---|---|
| `title` | Product hero shot, autumn | Searchable |
| `model` | designer-image-v2 | Queryable |
| `aspect_ratio` | 16:9 | |
| `style_tags` | [warm, minimal] | Searchable |
| `use_case` | hero, social, banner | |
| `approved` | true / false | Connector should only ingest `true` |
| `last_reviewed` | 2026-09-01 | |

## YAML gotcha

Always quote aspect ratios (`aspect_ratio: "16:9"`). Unquoted, YAML reads `16:9` as a number (969), not text.

## Testing tip

`prompts/draft-neon-cyberpunk-mug.md` is marked `approved: false`. It should NOT appear in Copilot results if your filter works.
