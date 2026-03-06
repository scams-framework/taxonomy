# SC&MS™
## Scam Classification & Mapping System

> A structured taxonomy for classifying scam techniques from first contact to financial extraction.

## What SC&MS Is

SC&MS maps scam operations across six stages. It is built around the victim's experience, not just the scammer's infrastructure.

- **Access**: vectors used to initiate first contact with a potential victim
- **Bait**: lures, offers, and alerts used to entice a victim's engagement
- **Coercion**: pressure and control tactics used to compel action or maintain compliance
- **Deception**: fabricated or manipulated artifacts used to mislead victims and make the scam believable
- **Exploiting Trust**: borrowed or cultivated trust used to lower a victim's skepticism
- **Financial Gain**: methods used to extract money, assets, or other value from victims

SC&MS provides a common language for researchers, fraud teams, and investigators working on consumer scams.

## Why It Exists

Consumers lost $12.5 billion to scams in 2024, and reported losses capture only part of the problem.

Defenders, researchers, and institutions still describe scam activity using inconsistent terms. SC&MS was created to fix that.

## What Makes It Different

SC&MS is built around the victim's experience, not just the scammer's infrastructure or operational workflow.

It is consumer scam-specific, technique-level, and machine-readable.

## Current Status

- **Version**: 0.3
- **License**: CC BY-ND 4.0 for version <1.0

Current taxonomy counts from [index.yaml](index.yaml):

- **6 stages**
- **93 techniques**
- **63 subtechniques**
- **156 total items**

Stage totals:

- **Access**: 19 techniques, 6 subtechniques, 25 total
- **Bait**: 22 techniques, 19 subtechniques, 41 total
- **Coercion**: 8 techniques, 13 subtechniques, 21 total
- **Deception**: 17 techniques, 10 subtechniques, 27 total
- **Exploiting Trust**: 13 techniques, 7 subtechniques, 20 total
- **Financial Gain**: 14 techniques, 8 subtechniques, 22 total

## Repository Layout

```text
taxonomy/
├── index.yaml
├── README.md
├── CHANGELOG.md
├── LICENSE
├── LICENSING-COMMITMENT.md
├── access/
├── bait/
├── coercion/
├── deception/
├── exploiting-trust/
└── financial-gain/
```

## Data Model

Each technique or subtechnique is defined in its own YAML file.

Example:

```yaml
spec_version: '0.3'
id: B003
name: Late fee notice
stage: Bait
stage_id: B000
created: '2025-09-01'
modified: '2026-03-07'
description: >
  A notice that a bill or payment is overdue and that a late fee
  will be charged if not paid promptly.
tags:
  - notice
  - late-fee
subtechniques:
  - B003.001
```

Core fields:

- `id`: unique identifier for the technique or subtechnique
- `name`: canonical name
- `stage`: lifecycle stage name
- `stage_id`: lifecycle stage identifier
- `description`: short definition
- `tags`: supporting keywords for grouping and search
- `parent`: parent technique ID for subtechniques
- `subtechniques`: child IDs for parent techniques
- `created`: date the technique was introduced into the taxonomy
- `modified`: date the technique content was last changed

For the initial public release, `created` dates reflect the start of the tracked taxonomy corpus rather than exact proposal dates for individual techniques. Techniques added after v0.3 use their actual introduction date.

## How to Use It

SC&MS can support several kinds of work:

- **Research**: map scam cases, compare campaigns, and identify recurring techniques
- **Fraud operations**: normalize case handling and reporting language
- **Tooling**: build explorers, tagging systems, and analytics that use the taxonomy
- **Threat intelligence**: structure scam techniques for internal sharing and analysis
- **Law enforcement**: compare scam patterns using a consistent vocabulary

SC&MS is best used as a multi-stage classification model. A single scam can involve techniques from multiple stages.

## Governance

SC&MS is maintained by **Satnam Singh Narang** through a curator-led process. External contributions are closed.

## Licensing

Version <1.0 is licensed under [CC BY-ND 4.0](LICENSE). Satnam Singh Narang commits to relicense the framework under **CC BY 4.0** upon release of version 1.0, or automatically on **December 31, 2027**, whichever comes first. See [LICENSING-COMMITMENT.md](LICENSING-COMMITMENT.md) for details.

## Citation

If you use SC&MS in research or operational work, please cite:

```text
Narang, S. S. (2026). SC&MS: Scam Classification & Mapping System (Version 0.3) [Data set]. https://scams.dev
```

BibTeX:

```bibtex
@misc{scms2026,
  author = {Narang, Satnam Singh},
  title = {SC\&MS: Scam Classification \& Mapping System},
  year = {2026},
  version = {0.3},
  url = {https://scams.dev},
  note = {A taxonomy for classifying scam techniques}
}
```

## Version History

**Version 0.3** (March 2026)
- Initial public release
- ABCDEF lifecycle established

## Links

- **Website**: https://scams.dev
- **GitHub**: https://github.com/scams-framework/taxonomy

---

SC&MS™ and SC&MS Framework™ are trademarks of Satnam Singh Narang.
