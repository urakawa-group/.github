# Urakawa Group

Welcome to the GitHub organization of the **Urakawa Group at TU Delft**.

This organization hosts software, tools and digital infrastructure developed and maintained by the group, supporting our laboratory operations, research activities and scientific collaboration.

## Software

### Laboratory software
Software for operating, monitoring and supporting laboratory equipment and experimental setups.

- **Control:** equipment interfaces and control applications for experimental setups.
- **Monitoring:** dashboards, logging and alarms that watch a running setup.
- **Data processing:** instrument output parsers, data conversion, data cleaning and general-purpose data processing tools.

### Research software
Scientific models, simulations, numerical methods and computational tools supporting our research.

### Web and infrastructure
The group website, integrations and automation that connect the other tools.

## Repository naming

Every repository name follows one pattern, so that its purpose is clear from the name alone and related repositories sort next to each other:

```
<area>-<category>-<name>[-<part>]
```

| element | meaning | examples |
|---|---|---|
| `area` | where the software lives | `lab`, `research`, `web` |
| `category` | what kind of software it is within that area | `control`, `monitoring`, `data`, `modeling`, `site`, `hooks` |
| `name` | the actual name of the project or setup | `parser`, `setup1` |
| `part` | optional; one repository of a project that needs several | `gc-helper` |

`lab-data-parser`, for example, is **lab** software, in the **data** category, called **parser**.

### Prefixes in use

| prefix | what it is for | example |
|---|---|---|
| `lab-control-` | software that operates equipment or a setup: instrument drivers, control applications, sequence and recipe runners | `lab-control-setup1` |
| `lab-monitoring-` | software that watches a setup without controlling it: live dashboards, data loggers, alarms and notifications | `lab-monitoring-setup1` |
| `lab-data-` | software that handles measured data after the fact: instrument file parsers, conversion, cleaning, processing | `lab-data-parser` |
| `research-modeling-` | scientific models: kinetics, thermodynamics, reactor models, fitting of physical models | `research-modeling-kinetics` |
| `research-analysis-` | analysis and evaluation workflows of research data, figures and reproducible notebooks | `research-analysis-drifts` |
| `research-simulation-` | numerical simulations and computational studies (e.g. CFD, DFT workflows) | `research-simulation-reactor` |
| `web-site-` | the group website and other public pages | `web-site-group` |
| `web-hooks-` | integrations and automation between services: webhooks, bots, scheduled jobs, notifications | `web-hooks-teams` |

If none of these fit, propose a new prefix in the same `<area>-<category>-` form before creating the repository, and add it to this table.

### Projects with several repositories

When one project needs more than one repository, all of them start with the project's base name, and each additional repository appends its part:

```
lab-control-setup1              the main control software of setup 1
lab-control-setup1-gc-helper    a helper for the GC attached to setup 1
lab-control-setup1-dashboard    a dashboard that belongs to the same setup
```

### General rules

- Lowercase letters, digits and hyphens only; no spaces, underscores or capitals.
- Full words rather than abbreviations, except for established names of a technique or instrument (`gc`, `ms`, `xrd`, `drifts`).
- No personal names, initials or degree programmes (`phd`, `msc`) in repository names. Repositories belong to the group and outlive any single project.
- Python packages inside a repository use the same name with underscores (`lab-data-parser` installs `lab_data_parser`).

## Contributing

We welcome contributions from group members and collaborators.

Please consult the README and contribution guidelines of the relevant repository before making changes. Use issues and pull requests to discuss improvements, review code and maintain a traceable development history.

## Access and contact

To get access to the organization or to a repository, contact **Julius Sommer** or **Manoj Coppens**.

For questions about a particular project, please contact its maintainers or open an issue in the corresponding repository.
