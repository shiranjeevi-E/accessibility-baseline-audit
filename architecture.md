# Repository Architecture

```text
accessibility-baseline-audit/
├── client/
│   ├── public/
│   ├── src/
│   │   └── main.js
│   └── package.json
├── server/
│   ├── src/
│   │   └── index.js
│   └── package.json
├── docs/
│   ├── audit-report.md
│   ├── accessibility-issues.csv
│   ├── architecture.md
│   └── screenshots/
├── tests/
│   └── accessibility/
│       └── README.md
├── .gitignore
└── README.md
```

## Components
- **Client:** Browser-facing interface. The starter page explains the purpose of the audit foundation.
- **Server:** Minimal Node.js HTTP server proving that a backend entry point exists.
- **Docs:** Audit method, evidence register, issue tracker and architecture notes.
- **Tests:** Location for accessibility checks and future automated test scripts.

## Data flow
Browser → Client application → Server API (when implemented) → Response → Client.

The current starter is intentionally minimal; it does not connect to or modify the India Post website.
