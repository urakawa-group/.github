# Urakawa Group

Welcome to the GitHub organization of the **Urakawa Group at TU Delft**.

This organization hosts the software and digital infrastructure that keeps our laboratory running: operating and monitoring experimental setups, and processing the data they produce.

## Software

### Laboratory software
The main focus of this organization. Software for operating, monitoring and supporting laboratory equipment and experimental setups, and for turning raw instrument output into usable data.

- **Control:** equipment interfaces and control applications for experimental setups.
- **Monitoring:** dashboards, logging and alarms that watch a running setup.
- **Data processing:** instrument output parsers, data conversion, data cleaning and general-purpose data processing tools.

### Web and infrastructure
The group website, integrations and automation that connect the other tools.

> [!NOTE]
> **What about research code?** Models, simulations and analysis code from individual research projects usually stay in their authors' own repositories for now. If such code becomes shared and maintained by the group, it can move here under a `research-` prefix (see [Possible future prefixes](#possible-future-prefixes)).

## Repository naming

> [!IMPORTANT]
> Every repository name follows **one pattern**, so that its purpose is clear from the name alone and related repositories sort next to each other:
>
> ```
> <area>-<category>-<name>[-<part>]
> ```

| element | meaning | examples |
|---|---|---|
| `area` | where the software lives | `lab`, `web` |
| `category` | what kind of software it is within that area | `control`, `monitoring`, `data`, `site`, `hooks` |
| `name` | the actual name of the project or setup | `parser`, `setup1` |
| `part` | optional; one repository of a project that needs several | `gc-helper` |

> [!NOTE]
> **Reading a name, by example**
>
> ```
> lab  -  data  -  parser
>  │       │        │
>  │       │        └── name:     the parser project
>  │       └─────────── category: handles measured data
>  └─────────────────── area:     laboratory software
> ```

### Prefixes in use

| prefix | what it is for | example |
|---|---|---|
| `lab-control-` | software that operates equipment or a setup: instrument drivers, control applications, sequence and recipe runners | `lab-control-setup1` |
| `lab-monitoring-` | software that watches a setup without controlling it: live dashboards, data loggers, alarms and notifications | `lab-monitoring-setup1` |
| `lab-data-` | software that handles measured data after the fact: instrument file parsers, conversion, cleaning, processing | `lab-data-parser` |
| `web-site-` | the group website and other public pages | `web-site-group` |
| `web-hooks-` | integrations and automation between services: webhooks, bots, scheduled jobs, notifications | `web-hooks-teams` |

> [!TIP]
> None of these fit? Propose a new prefix in the same `<area>-<category>-` form **before** creating the repository, and add it to this table.

### Possible future prefixes

Not in use yet. If shared research code moves into the organization later, these are the suggested prefixes:

| prefix | what it would be for | example |
|---|---|---|
| `research-modeling-` | scientific models: kinetics, thermodynamics, reactor models, fitting of physical models | `research-modeling-kinetics` |
| `research-analysis-` | analysis and evaluation workflows of research data, figures and reproducible notebooks | `research-analysis-drifts` |
| `research-simulation-` | numerical simulations and computational studies (e.g. CFD, DFT workflows) | `research-simulation-reactor` |

### Projects with several repositories

When one project needs more than one repository, all of them start with the project's base name, and each additional repository appends its part. That way they always sort together:

```
lab-control-setup1              the main control software of setup 1
lab-control-setup1-gc-helper    a helper for the GC attached to setup 1
lab-control-setup1-dashboard    a dashboard that belongs to the same setup
```

### General rules

| ✅ do | ❌ don't |
|---|---|
| `lab-data-parser` | `Lab_Data_Parser`, `lab data parser` |
| `lab-monitoring-setup1` | `lab-mon-s1` |
| `lab-data-parser` | `phd-parser-jsommer` |

- Lowercase letters, digits and hyphens only; no spaces, underscores or capitals.
- Full words rather than abbreviations, except for established names of a technique or instrument (`gc`, `ms`, `xrd`, `drifts`).
- Python packages inside a repository use the same name with underscores (`lab-data-parser` installs `lab_data_parser`).

> [!WARNING]
> **No personal names, initials or degree programmes** (`phd`, `msc`) in repository names. Repositories belong to the group and outlive any single project or person.

## Contributing

We welcome contributions from group members and collaborators.

Please consult the README and contribution guidelines of the relevant repository before making changes. Use issues and pull requests to discuss improvements, review code and maintain a traceable development history.

## Access and contact

To get access to the organization or to a repository, contact **Julius Sommer** or **Manoj Coppens**.

> [!NOTE]
> For questions about a particular project, please contact its maintainers or open an issue in the corresponding repository.
