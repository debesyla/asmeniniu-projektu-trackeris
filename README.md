# Launchpad

A small local dashboard for tracking personal projects, tasks, and backlog ideas from a single `projects.json` file.

## How it works

- `index.html` renders the full UI (styles + script in one file).
- `projects.json` is the data source for projects and backlog items.
- The app fetches `projects.json` at runtime and renders cards and counters.

## Run locally

Use a local web server (opening `index.html` directly will block JSON fetch in many browsers):

```bash
python3 -m http.server 8000
```

Then open:

- http://localhost:8000

## Update data

Edit `projects.json` and refresh the page.

Each project supports:

- `name`
- `description`
- `status` (`active` or `graveyard`)
- `agent`
- `progress` (0-100)
- `url`
- `updated` (ISO datetime)
- `todos`, `issues`, `ideas`, `research` (arrays)

Backlog items support:

- `title`
- `type` (`idea` or `research`)
- `created` (ISO datetime)
