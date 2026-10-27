# Space News — Weekly Briefing

A static GitHub Pages site for the Hermes Weekly Space News project.

## How reports appear

The existing Hermes job saves Markdown reports locally in the Obsidian vault at `Space News\YYYY-MM-DD.md` and sends them to Telegram. This website does not yet have access to those local files. To publish each edition, copy the report `.md` file into `reports/` and add an entry to `reports/index.json`:

```json
{
  "reports": [
    {
      "date": "YYYY-MM-DD",
      "title": "Weekly Space News — YYYY-MM-DD",
      "summary": "A short summary of this week's main developments.",
      "file": "YYYY-MM-DD.md"
    }
  ]
}
```

Keep newest editions first. The `file` value must match a Markdown filename in `reports/`.

## Next step: connect Hermes

Update the Hermes Weekly Space News job to publish each finished report to this repository, including the Markdown report and the index JSON. Until that is configured, the site is a live-ready shell and reports remain in the local vault/Telegram.
