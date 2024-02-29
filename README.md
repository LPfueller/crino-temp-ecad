# Crino Temp Hardware (RevA.1.0)

Crino offers precise characterisations of lithium ion cells for quality control in battery manufacturing and research using the *crino instrument*. Every crino instrument consists of several *crino boards* with actuators and sensors that are connected to a central control system (currently a *Raspberry Pi*). This control system is performing all measurements and also provides a user interface to interact with the system. This repository consists of Kicad development and production files for the *temp board*, which can be used to perform accurate temperature measurements.

## Project directory structure

- **docs**: Contains additional documentation of the project.
- **ci**: Contains tools to automatically review the project and generate the fabrication data.
- **hardware**: Contains the KiCad project files.

## Local Development Experience

**Prerequisites**:

- Install [KiCad](https://kicad.org/download/)
- Install [Git](https://git-scm.com/downloads), if you are new to git, [here](https://rogerdudler.github.io/git-guide/index.html) is a short intro.
- Install [Docker](https://docs.docker.com/docker-for-windows/install/), it will help us to automate testing and generate production files.

**How to start**:

First, create a *crino-repos* folder in your workspace, which will contain all crino related git repositories. Navigate to the *crino-repos* folder, clone this project and crino KiCad parts library project
- `git clone --recursive https://github.com/crinolab/crino-temp-ecad.git`
- `git clone --recursive https://github.com/crinolab/crino-kicad-lib.git` 

Open KiCad, navigate to global library path and add symbols from `<your path>crino-repos/crino-kicad-lib/kicad/symbols_v5/`, `<your path>crino-repos/crino-kicad-lib/crino/symbols/` and `<your path>crino-repos/crino-kicad-lib/digikey/digikey-symbols/`. Do the same with the footprints. Now you should be able to open this KiCad project without errors and missing components.
  
> Before you start making changes, please read the [development workflow](./docs/development-workflow.md) for Crino Power Board.
  
## Appendix: How to create nice looking documentation

- Checkout this [page](https://ghost.org/changelog/markdown/) to learn more about writing nice looking documentation in markdown.

- Use [diagrams.net](https://diagrams.net) to create diagrams and save them as editable PNGs which can be embedded in markdown.
