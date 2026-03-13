# Product Setup

This domain defines the first-run setup of PAOS: the minimum configuration the CEO must complete before the empire becomes usable.

## Documents

| Document | Purpose | Status |
| --- | --- | --- |
| [Onboarding Baseline](onboarding-baseline.md) | First-run setup flow, initial identity, AI path, and first entry experience | Planned |

## Setup View

```mermaid
flowchart LR
    Root[Empire Root]
    Identity[CEO + Empire + COO]
    AI[Initial AI Path]
    Entry[COO Control Panel]

    Root --> Identity
    Identity --> AI
    AI --> Entry
```
