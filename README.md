# Support SI Admin — IT Documentation Portal

A searchable support portal that brings technical documentation, operating guidance, tutorials and reusable prompts together for IT administrators.

Administrators can find an operating procedure, understand an application, follow a tutorial or locate a reusable prompt without navigating several disconnected documentation sources. Platform documentation stays connected to its maintained source files.

## Users

| Role | Use |
|---|---|
| IT administrator | Search documentation, consult troubleshooting material and follow operating guidance. |
| Documentation maintainer | Update source content and keep support resources organized. |

## Main features

- **Global search.** Find relevant sections across FAQ, platform documentation, tutorials and prompts.
- **Technical and user documentation.** Navigate long-form content with section anchors and a table of contents.
- **Runtime content synchronization.** Reflect changes to maintained documentation sources without duplicating their text manually.
- **Agent guidance.** Consult organized guidance for AI-assisted project work.
- **Tutorials.** Follow step-by-step guidance and open related reusable requests.
- **Prompt library.** Browse categorized prompts, inspect a selected entry and copy its text.

## Typical workflow

1. Search for a question or choose a documentation category.
2. Open the relevant section or tutorial.
3. Follow its navigation to related guidance or a reusable prompt.
4. Return to the support portal as the underlying documentation evolves.

## Project structure

```text
support-si-admin-public-version/
├── backend/
│   ├── app/
│   │   ├── docs/
│   │   ├── support_content/
│   │   └── main.py
│   ├── tests/
│   ├── pyproject.toml
│   ├── README.md
│   └── requirements.txt
├── deploy/
│   ├── docker/
│   ├── scripts/
│   ├── systemd/
│   └── README.md
├── docs/
│   ├── decisions/
│   │   └── README.md
│   ├── design/
│   │   ├── decisions.md
│   │   ├── requirements.md
│   │   └── verification.md
│   ├── issue/
│   └── support-content/
│       ├── module-001/
│       ├── prompts/
│       └── tutoriels/
├── frontend/
│   ├── scripts/
│   ├── src/
│   │   ├── api/
│   │   ├── app/
│   │   ├── components/
│   │   ├── content/
│   │   ├── hooks/
│   │   ├── pages/
│   │   ├── styles/
│   │   ├── test/
│   │   └── utils/
│   ├── tests/
│   ├── package.json
│   └── README.md
├── issues/
│   ├── epics/
│   ├── features/
│   ├── tasks/
│   └── README.md
├── ARCHITECTURE.md
└── README.md
```

[Complete directory structure](docs/design/structure.md)

| Area | Responsibility |
|---|---|
| Web interface | React, Mantine and Vite documentation navigation, search and prompt browsing. |
| Content API | FastAPI loading and validation of runtime documentation and structured support content. |
| Source documentation | Maintained Markdown files read from configured, read-only locations. |
| Support catalogues | Versioned sections, tutorials and reusable prompt entries. |
| Presentation layer | Markdown rendering, headings, anchors and accessible reading components. |

## Technology

React, JavaScript, Mantine, Vite, Python, FastAPI, Markdown and Docker.

## Engineering

- [Architecture](ARCHITECTURE.md)
- [Product requirements](docs/design/requirements.md)
- [Design decisions](docs/design/decisions.md)
- [Verification strategy](docs/design/verification.md)

The portal provides documentation and guidance; it does not execute remote administration commands.

---

Source code, operational configuration and project-specific data are withheld for confidentiality.
