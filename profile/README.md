![Logo](https://avatars.githubusercontent.com/u/264260364?s=200&v=4)

# The Karpfen Toolkit 🐟

Karpfen is a **model-driven state machine execution framework** built around three domain-specific languages and a lightweight runtime server.

| Layer | What it does |
|---|---|
| **KMeta** (`.kmeta`) | Defines type hierarchies — classes, properties, composition (`has`), and references (`knows`) |
| **KModel** (`.kmodel`) | Instantiates a concrete world model from a KMeta metamodel |
| **KStates** (`.kstates`) | Attaches hierarchical statecharts to model objects; supports `ENTRY`/`DO` phases, prioritised transitions, `NOT LOOPING` guards, Python-embedded `EVAL` expressions, and reusable `MACRO` definitions |
| **karpfen-runtime** | Stateless Kotlin/Ktor HTTP server that hosts execution environments in-memory; exposes a REST API and a WebSocket push channel for live object-change and domain-event notifications |

**Highlighted features:**
- Multiple independent execution environments per server instance, each with its own model and statemachine set
- Hierarchical states with proper state-stack semantics and per-level ENTRY/DO execution
- Fine-grained WebSocket subscriptions: observe individual model object properties or entire event domains
- Tick-based execution loop with configurable delay and optional execution tracing

**Further reading:**

*Runtime*
- [Getting Started](https://github.com/karpfenproject/karpfen-runtime/blob/main/guides/GETTING_STARTED.md) — prerequisites, configuration, end-to-end workflow
- [HTTP API Endpoints](https://github.com/karpfenproject/karpfen-runtime/blob/main/guides/HTTP_API_ENDPOINTS.md) — full REST + WebSocket API reference
- [Statemachine Execution Semantics](https://github.com/karpfenproject/karpfen-runtime/blob/main/guides/STATEMACHINE_EXECUTION_SEMANTICS.md) — tick loop, transition priority, event model
- [Quick Reference](https://github.com/karpfenproject/karpfen-runtime/blob/main/guides/QUICK_REFERENCE.md) — commands, endpoints, and troubleshooting at a glance

*DSL grammars*
- [KMeta Grammar Guide](https://github.com/karpfenproject/karpfen-dsl-tools/blob/main/guides/kmeta_grammar_guide.md)
- [KModel Grammar Guide](https://github.com/karpfenproject/karpfen-dsl-tools/blob/main/guides/kmodel_grammar_guide.md)
- [KStates Grammar Guide](https://github.com/karpfenproject/karpfen-dsl-tools/blob/main/guides/kstates_grammar_guide.md)

## ⭐ Demos ⭐

You find a demo for a simulation of a cyber-physical setting using multiple concurrent statecharts and a world model here [Turtle Robot Demo](https://github.com/karpfenproject/robot-model-js-client-demo)

## License

Licensed under the Apache License, Version 2.0. See `LICENSE` for details.
