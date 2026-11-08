# Changelog

All notable changes to the EA Repository Landscape are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and this project uses [Semantic Versioning](https://semver.org/). The Landscape and the Foundation are released under the same version number.

## [2.0] - Unreleased

First release of the Landscape as a separate Archi model (Archi 5.10, coArchi), complementing the EA Repository Foundation.

### Added
- Model structure without ArchiMate elements: element folders aligned with the Foundation (same names, same documentation).
- View folders:
  - 1 Architecture Requirements: 1.1 Strategic, 1.2 Segment, 1.3 Capability Requirements.
  - 2 Architecture Landscape: 2.1 Strategic, 2.2 Segment, 2.3 Capability Architectures.
  - 3 Solution Landscape: 3.1 Strategic, 3.2 Segment, 3.3 Capability SBBs.
- View properties: TOGAF Artifact, ADM Phase, ArchiMate Viewpoint, Architecture State, Concerns Addressed.
- Read Me view, including the Version Control and Lifecycle section (branch types, lifecycle of planned content).
- Version control model: main holds all approved architecture content (Baseline, approved Transition and Target Architectures); working branches (`baseline/`, `change/`, `initiative/`) hold proposals and are merged at approval through a pull request.
- Use of the Lifecycle Status and Change Reference properties defined in the Foundation.
- Pull request template (`.github/pull_request_template.md`).
- Distribution as an Archi model template (`.architemplate`).
