# EA Repository Landscape

Archi template for the **Architecture Landscape** of an Architecture Repository based on the **TOGAF® Standard, 10th Edition**, modeled in **ArchiMate® 3.2**.

It provides the structure that holds the architecture of an enterprise: Architecture Requirements, Architecture Landscape and Solution Landscape, at strategic, segment and capability level. It contains **no example content** and is designed to be used together with the companion **[EA Repository Foundation](../../../ea-repository-foundation)** template, which holds the reference metamodel and the TOGAF artifact guides.

> **Version:** 2.0 &nbsp;·&nbsp; **Tool:** [Archi](https://www.archimatetool.com) 5.x &nbsp;·&nbsp; **Collaboration:** coArchi plugin

---

## What's inside

### Element folders
- One subfolder per ArchiMate 3.2 element type in every layer folder, ordered *active structure / behavior / passive structure*.
- Same folder names and documentation as in the Foundation template.
- An element is modeled once, whatever the architecture state it belongs to: an unchanged application is the same element in the Baseline and in the Target.

### View folders

| Folder | Subfolders | Content |
|---|---|---|
| **1 Architecture Requirements** | 1.1 Strategic · 1.2 Segment · 1.3 Capability Requirements | Requirements realization views and requirements catalogs |
| **2 Architecture Landscape** | 2.1 Strategic · 2.2 Segment · 2.3 Capability Architectures | Architecture views produced along the TOGAF ADM |
| **3 Solution Landscape** | 3.1 Strategic · 3.2 Segment · 3.3 Capability SBBs | Solution Building Blocks realizing the architecture |

Each artifact view is built following the corresponding guide of the Foundation template (*Reference Library › TOGAF Artifact Guides*).

### Read Me view
Explains the structure, the properties, the conventions and the version control rules of the model.

---

## Architecture states and version control

Baseline, Transition and Target architectures are **not** separated in folders:

- Every view in *2 Architecture Landscape* and *3 Solution Landscape* carries the property **`Architecture State`** = `Baseline`, `Transition` or `Target`.
- Branch **`main`** holds the validated Baseline Architecture.
- One branch **`target/<initiative>`** is created per ADM cycle or initiative; it holds the Transition and Target Architectures under development.
- When the initiative is implemented, the branch is merged into `main`: the Target becomes the new Baseline.
- Tags mark validated releases (e.g. `baseline-2026-10`).

## View properties

| Property | Values |
|---|---|
| `TOGAF Artifact` | Name of the TOGAF artifact delivered by the view |
| `ADM Phase` | ADM phase of the artifact |
| `ArchiMate Viewpoint` | Viewpoint used |
| `Architecture State` | Baseline, Transition or Target |

---

## Getting started

### Use it as a template
1. Download the `.architemplate` file from the latest [Release](../../releases).
2. In Archi: **File › New › New Model from Template…** and select the downloaded file.
3. Rename the model (`<Organization> - <Project name> - Landscape`) and replace the placeholders in the model *Purpose* and properties (`Organization`, `Project`, `Model Owner`).
4. Publish the new model to its own (private) repository with **Collaboration › Add Model to Remote Repository…**.
5. Read the **Read Me** view in the model.

### Work on the template itself
1. Install the **coArchi** (Collaboration) plugin in Archi.
2. **Collaboration › Import Remote Model to Workspace…** with the URL of this repository.
3. Use a GitHub Personal Access Token as password.

---

## Conventions

- All names, documentation and notes are written in English.
- View layout: within each layer, active structure on the left, behavior in the center, passive structure on the right; Motivation on the right.
- Element names: singular, Title Case. Relationship names are left empty unless they add meaning.
- Every element carries a documentation text.
- Only ArchiMate 3.2 compliant relationships; run the Archi Validator before each release.
- The Business Model Canvas is produced with the Archi Canvas feature (*New › Canvas from Template › Business Model Canvas*).

## Versioning

The Landscape and Foundation templates are released together and share the same version number. See [CHANGELOG](CHANGELOG.md) for the history of changes.

---

## License

This work is licensed under the [Creative Commons Attribution 4.0 International License (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/). You may share and adapt it, including for commercial purposes, provided you give appropriate credit.

**Third-party content.** Some folder descriptions are taken from the *ArchiMate® 3.2 Specification* and the *TOGAF® Standard, 10th Edition*, © The Open Group. They are reproduced for reference with their source and are **not** covered by the CC BY 4.0 license.

ArchiMate® and TOGAF® are registered trademarks of The Open Group. This project is not affiliated with or endorsed by The Open Group.

## Author

Olivier Sabbe – Enterprise Architect
