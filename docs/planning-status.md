# Planning Status

This file tracks which planning areas are stable enough to document and which areas still need design work before implementation starts.

## Completed Planning Areas

| Section | Status | Notes |
| --- | --- | --- |
| Operating model | Planned | CEO/COO relationship and AI identity model are defined. |
| Role hierarchy | Planned | Built-in backbone, titles, branching, and depth ladder are defined. |
| Memory model | Planned | Memory layers, logs boundary, and memory commit path are defined. |
| Session continuity | Planned | Context overflow is handled through structured handoff and automatic rollover. |
| Working state schema | Planned | The session state and handoff records are typed and traceable. |
| Memory governance | Planned | Read/write rules, overrides, and authority flow are defined. |
| Memory retention | Planned | Superseding, archive behavior, and purge rules are defined. |

## Still Needed

| Section | Why It Matters |
| --- | --- |
| Log model | Needed to define event retention, transcript rules, audit boundaries, and deletion behavior. |
| Global permission model | Needed to define inheritance from empire caps down to roles, tools, network, and external files. |
| Onboarding baseline | Needed to define the first-run setup flow for workspace, providers, names, and security posture. |
| Custom agent creation model | Needed to define how the user creates new agents, assigns parents, titles, links, and permissions. |
| Workspace and sandbox model | Needed to define local boundaries, filesystem rules, tool execution, and internet access. |
| Tech architecture | Needed to finalize stack, storage choices, key handling, packaging, and cross-platform delivery. |
| Provider architecture | Needed to define how OpenAI, Ollama, Gemini, Claude, and future providers plug in. |
| UI/UX structure | Needed to define control panel, org chart, approvals, memory inspector, and audit views. |
| Roadmap and ADR package | Needed to turn planning into buildable implementation phases and decision records. |

## Visual Status

```mermaid
flowchart LR
    subgraph Stable["Planned Foundation"]
        OM[Operating Model]
        RH[Role Hierarchy]
        MM[Memory Model]
        SC[Session Continuity]
        WS[Working State Schema]
        MG[Memory Governance]
        MR[Memory Retention]
    end

    subgraph Open["Still To Plan"]
        LM[Log Model]
        PM[Permission Model]
        OB[Onboarding]
        CA[Custom Agents]
        SB[Sandbox]
        TA[Tech Architecture]
        PA[Provider Architecture]
        UX[UI and UX]
        RD[Roadmap + ADRs]
    end
```

## Immediate Next Recommendation

The next document to design should be the **log model**. The current memory decisions already depend on logs being a separate audited system, so that boundary should be formalized before the broader permission model and implementation architecture.
