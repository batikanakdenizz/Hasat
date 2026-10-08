# HASAT

HASAT is a web-based decision-support system that helps olive growers in Türkiye choose a harvest window for their orchards. The grower enters the orchard location, olive variety and a production goal (prioritising phenolic content, oil accumulation or a balance of both); the system combines weather, satellite and variety information with a machine-learning model to estimate ripening progression and suggest a harvest window that fits that goal.

SE 4910 / SE 4920 Senior Project, Software Engineering, Yaşar University.

## Team

- Batıkan Akdeniz
- Başar Özkaşlı
- Yasir Özer
- Zeynep Yıldız

## Repository structure

```
Hasat/
├── docs/              Project documents (proposal, statement of work, reports)
├── CONTRIBUTING.md    Team agreement for branches, commits and pull requests
└── README.md
```

The structure of the application code (backend, frontend, machine-learning components) will be decided in a technical meeting and documented here.

## Workflow

Project management is done in Jira (project key `HST`). Every change in this repository is linked to a Jira issue:

- one branch per issue: `story/HST-<n>`, `task/HST-<n>`, `bug/HST-<n>`
- commits: `<type>(HST-<n>): <description>` ([Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/))
- changes reach `main` only through a reviewed Pull Request

Read [CONTRIBUTING.md](CONTRIBUTING.md) before your first commit.
