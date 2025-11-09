---
title: Describing the "Bedrock"
subtitle: The architecture for the open exchange of scientific ideas that is accessible by developers
---

## Context and Framing

The discussion centers on **rethinking scientific publishing infrastructure**—moving beyond PDFs and disconnected supplementary materials toward **modular, interoperable, and machine-readable research objects**. Participants refer to this initiative as _Bedrock_, a metaphor for the underlying content layer of science that supports higher-level representations ("soil" as metadata, "flowers" as the presentation layer).

The group's goal is to define or prototype a **schema or standard format** that enables linking, reuse, and interoperability of granular scientific content—figures, data, methods, and even paragraphs—across tools and platforms.

## Problems in the Current System

### Disconnected Elements and Reproducibility Gaps

- Researchers cannot easily **rebuild or replicate** another scientist's work because key contextual elements (e.g., reagents, SKUs, metadata, data availability) are not structured or linkable.
- Supplementary files are _idiosyncratic, unstructured, and inaccessible_.
- Peer review focuses on narrative, not replication ("peer replication" was emphasized as the real goal).

### Authoring Pain Points

- Scientists are not incentivized to produce structured metadata; it isn't useful to them during creation.
- Without **author-friendly tools**, metadata curation will not occur.
- Late-stage publication (a year after experimentation) leads to data loss and forgotten details.

### Cultural and Structural Barriers

- Researchers fear being _scooped_ if they share granular results.
- Incentives reward polished narratives over incremental contributions.
- Big-science examples (e.g., LIGO) show structured collaboration and replication mechanisms that small-scale labs lack.

## Desirable Properties of the New Approach

### Modular and Granular Content

- The **minimum unit of contribution** could be a single experiment or even an observation ("the minimal currency of science").
- Each unit should be **typed and linkable**—a figure panel, paragraph, dataset, or method.
- Enables _peer replication_ and building cumulative knowledge graphs.

### Author-Centric Design

- Metadata entry should be embedded early in the research workflow (lab notebooks, weekly logs).
- Tools should give **immediate value** to authors (e.g., better organization, feedback, or linting-style suggestions).
- Shorter publication cycles (iterative curation) reduce cognitive load and error propagation.

### Linking and Web-Native Infrastructure

- The web's power lies in **linking**, not redisplaying.
- Embrace _messiness and heterogeneity_—interoperability over standardization.
- Support _bi-directional or resilient links_ between research objects while accepting web fragility.

### Layered Metaphor

- **Bedrock:** raw content and data.
- **Soil:** metadata and schemas enabling discovery.
- **Flowers:** presentation and visualization layers that remix and display content differently.

## Technical Architecture and Standards

### JSON, JSON-LD, and JSON Schema

- Core consensus: use **JSON as the base data format**.
- JSON Schema defines structure and typing (paragraphs, figures, links).
- JSON-LD adds **linked-data semantics**—shared vocabulary alignment across schemas (via `@context`).
- Schema.org terms and JSON-LD mappings enable translation between domain vocabularies.

### Relationship to Existing Standards

- **Pandoc AST** provides a precedent but is "hideous" and not ideal for machine processing.
- **JATS** is acknowledged as important but overly rigid and non-interoperable; the group seeks a _successor schema_ more like JSON/HDF/Zarr—modular, extensible, and linkable.
- Compatibility with **MyST, Stencila, Quarto, Curvenote**, and other document models is critical; they are viewed as "interfaces" over a shared data model.

### Linking Mechanisms

- Every element (paragraph, section, figure) should have a **persistent ID or resolvable path**.
- External references (e.g., datasets, code) would use typed links validated against schemas.
- Agreed-upon "carve-outs" for cross-references in ASTs.

### Incremental Adoption

- Consensus: don't wait for universal agreement.
- Start with **two or three collaborating projects**, publish version 0.1 of a shared schema, and test interoperability.
- Translate existing documents (e.g., JATS → JSON) to bootstrap adoption.

## Licensing and Attribution Layer

### Machine-Readable Licensing

- Licenses (e.g., CC-BY, CC-BY-NC, ND) can be **expressed and validated mechanically** within schemas.
- Linking is permissible even between incompatible licenses (not a derivative work), but **reuse and remixing** require compatibility checks.
- Future tooling could include a **license-compatibility matrix** or automated validator.

### Attribution Requirements

- Schema can embed rules and tooling to enable "if you link to this, include this attribution and license".
- Encourages early sharing by **providing attribution safety**—time-stamping and provenance metadata (a digital "flag-planting").

### Creative Commons Perspective

- CC representatives emphasized **user awareness** of license implications and limits of automated enforcement.
- Mechanized verification is feasible and desirable but must complement, not replace, human interpretation.

## Broader Philosophical Insights

- **Continuous Science:** Move from static, monolithic papers to continuous, linkable research streams.
- **Trust Circles:** Allow sharing and collaboration at intermediate stages without public release.
- **Open by Design:** Machine readability and openness should be defaults; opacity should require justification.
- **Messy Web as Feature:** Embrace diversity of tools and formats; prioritize translation and interoperability over control.
- **Schema as Conversation:** Rather than one fixed format, define shared _translation points_ between evolving community schemas.

## Next Steps and Outcomes

- Draft a **proof-of-concept schema** (version 0.0.1) defining minimal elements:

  - Paragraphs, sections, figures, datasets, and cross-references.
  - JSON Schema typing plus optional JSON-LD context.

- Prototype translation between MyST AST, Pandoc AST, and Stencila Encoda.
- Define a **mechanical validation layer** for licensing compatibility.
- Publish demonstration documents across platforms (Curvenote, Quarto Pub, eLife, etc.) to test interoperability.
- Continue collaboration toward a "Bedrock" format that underlies composable, modular, and interoperable scientific publishing.

## Key Takeaways

1. **The problem is structural:** PDFs and JATS lock science in rigid, narrative-centric silos.
2. **The opportunity is architectural:** A web-native, JSON-based schema can unlock modular reuse.
3. **The transition must be incremental:** Begin with partial interoperability among active communities (MyST, Stencila, Curvenote, JATS, etc.).
4. **Success is cultural as much as technical:** Scientists must see value in the format immediately.
5. **Licensing and attribution are enablers, not afterthoughts:** Machine-readable rights are core to open, reproducible science.

The Bedrock conversation charts a pragmatic path from today's disconnected scholarly formats toward a **composable, interoperable, and link-rich ecosystem for scientific knowledge**—grounded in JSON schemas, aligned through linked data, validated through licensing logic, and grown organically from community-driven collaboration.
