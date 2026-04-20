<div align="center">

# ARCORIS

**Adaptive resource control, overload regulation, and workload isolation for modern distributed schedulers and execution platforms.**

Admission control · Rate control · Overload protection · Workload isolation · Fairness · Feedback-driven execution control

</div>

ARCORIS is an engineering project focused on making distributed workload execution
more predictable, safer under pressure, and easier to control in real systems.

It is built for platform engineers, operators, integrators, and contributors who need
clear control over how work enters the system, how it is scheduled, how overload is handled,
how resources are protected, and how runtime behavior remains observable under contention,
failure, and changing system conditions.

This organization is intentionally structured as a **multi-repository system**.
Each repository has a clear responsibility so that source code, public documentation,
engineering standards, community structure, design-change tracking, and runnable examples
remain easy to navigate instead of collapsing into one noisy place.

## Start Here

Use this map to choose the right entry point.

| If you want to... | Start here |
| --- | --- |
| Understand what ARCORIS is | [Core repository](https://github.com/arcoris/arcoris/blob/main/README.md) |
| Evaluate the project quickly | [Core repository](https://github.com/arcoris/arcoris/blob/main/README.md) |
| Learn the system model and core concepts | [Documentation](https://github.com/arcoris/docs/blob/main/README.md) |
| Run demos or baseline setups | [Examples](https://github.com/arcoris/examples/blob/main/README.md) |
| Integrate ARCORIS into another platform | [Documentation](https://github.com/arcoris/docs/blob/main/README.md) |
| Contribute code, docs, or design work | [Community](https://github.com/arcoris/community/blob/main/README.md) |
| Understand major proposals and accepted changes | [Enhancements](https://github.com/arcoris/enhancements/blob/main/README.md) |
| Understand ownership, roles, and coordination | [Community](https://github.com/arcoris/community/blob/main/README.md) |

## What ARCORIS Focuses On

ARCORIS is centered on **execution control in distributed environments**.

That includes:

- **admission control** for deciding whether new work should be accepted, delayed, redirected, or rejected;
- **rate control** for shaping throughput based on live system conditions instead of fixed assumptions;
- **overload protection** for preventing cascading failure and protecting the system under pressure;
- **workload isolation** for preventing one tenant, queue, class, or flow from consuming the whole system;
- **priority and fairness models** for balancing urgency, guarantees, and resource distribution;
- **feedback-driven scheduling behavior** based on observed runtime conditions;
- **observability-aware execution control** where metrics, signals, and system state are first-class inputs into decision-making;
- **failure-aware runtime behavior** where retry, timeout, cancellation, backpressure, and degradation are treated as design concerns, not afterthoughts;
- **integration and extensibility surfaces** so ARCORIS can fit into broader platform and control-plane environments.

## Use ARCORIS When

ARCORIS is most relevant when one or more of the following are true:

- workload arrival is bursty, uneven, or difficult to predict;
- resource pressure changes faster than static configuration can safely absorb;
- multiple tenants, queues, or workload classes compete for the same execution capacity;
- overload in one path can degrade unrelated work unless isolation is enforced;
- you need explicit admission, throttling, and degradation behavior instead of implicit failure;
- you need operationally visible control over rate, concurrency, fairness, and overload handling;
- you want execution behavior to respond to live system signals rather than only static policy.

## Repository Guide

This organization is structured so that each repository answers a different class of question.

### Core repository

- [Core repository](https://github.com/arcoris/arcoris/blob/main/README.md)

The main technical repository for the project itself.

Start here when you need to understand:

- what ARCORIS is at system level;
- where the main implementation lives;
- how the source tree is organized;
- what the primary runtime and component boundaries look like;
- what the current implementation focus is.

### Documentation

- [Documentation](https://github.com/arcoris/docs/blob/main/README.md)

The main public documentation entry point for users, evaluators, operators, and integrators.

Start here when you need:

- quick starts and onboarding;
- concepts and architecture overviews;
- deployment and operational guidance;
- tutorials, how-to guides, and troubleshooting;
- public reference documentation.

### Examples

- [Examples](https://github.com/arcoris/examples/blob/main/README.md)

Runnable examples, demo setups, baseline deployments, integration scenarios,
observability bundles, and failure-oriented evaluation material.

Start here when you need:

- a minimal runnable setup;
- local or dev-cluster demos;
- example integrations;
- practical evaluation scenarios.

### Enhancements

- [Enhancements](https://github.com/arcoris/enhancements/blob/main/README.md)

The design and change-management repository for significant proposals and tracked architectural work.

Start here when you need to understand:

- what major changes are being proposed;
- what has already been accepted, rejected, withdrawn, or superseded;
- how large changes are tracked from proposal to implementation.

### Community

- [Community](https://github.com/arcoris/community/blob/main/README.md)

Defines how the project community works.

Start here when you need to understand:

- ownership and roles;
- decision-making;
- coordination structures and working groups;
- contributor growth paths.

### Handbook

- [Handbook](https://github.com/arcoris/handbook/blob/main/README.md)

Defines how engineering work is expected to be done across the project.

Start here when you need:

- engineering standards;
- documentation rules;
- review and quality expectations;
- release and process conventions.

## Recommended Reading Order

If you are new to ARCORIS, this is the most effective order:

1. [Core repository](https://github.com/arcoris/arcoris/blob/main/README.md)
2. [Documentation](https://github.com/arcoris/docs/blob/main/README.md)
3. [Examples](https://github.com/arcoris/examples/blob/main/README.md)
4. [Community](https://github.com/arcoris/community/blob/main/README.md)
5. [Handbook](https://github.com/arcoris/handbook/blob/main/README.md)
6. [Enhancements](https://github.com/arcoris/enhancements/blob/main/README.md)

That order gives you:

- project understanding first;
- usage and operational context second;
- runnable material third;
- contributor and collaboration context next;
- engineering standards after that;
- major design-change history and future direction last.

## Organization Structure

This separation is intentional.

- The **core repository** contains and explains the implementation.
- The **documentation repository** is the public entry point for usage, operations, integration, and reference.
- The **examples repository** provides runnable setups and practical evaluation material.
- The **enhancements repository** tracks significant design changes and their lifecycle.
- The **community repository** explains ownership, roles, and coordination.
- The **handbook repository** defines how work is expected to be done across the project.

This keeps the project easier to navigate, easier to maintain, and easier to scale
as both the codebase and the contributor surface grow.

## Audience Guide

### For evaluators

Start with:

- [Core repository](https://github.com/arcoris/arcoris/blob/main/README.md)
- [Documentation](https://github.com/arcoris/docs/blob/main/README.md)
- [Examples](https://github.com/arcoris/examples/blob/main/README.md)

You should be able to answer quickly:

- what problem ARCORIS solves;
- what kind of systems it is designed for;
- how it relates to schedulers, queues, workers, and control planes;
- whether it can be evaluated locally or in a small cluster;
- what its main architectural assumptions are.

### For operators

Start with:

- [Documentation](https://github.com/arcoris/docs/blob/main/README.md)
- [Examples](https://github.com/arcoris/examples/blob/main/README.md)
- [Core repository](https://github.com/arcoris/arcoris/blob/main/README.md)

You will primarily care about:

- deployment models;
- operational boundaries;
- observability expectations;
- failure handling;
- sizing and capacity assumptions;
- runbooks, troubleshooting, and upgrade guidance.

### For integrators

Start with:

- [Documentation](https://github.com/arcoris/docs/blob/main/README.md)
- [Core repository](https://github.com/arcoris/arcoris/blob/main/README.md)
- [Examples](https://github.com/arcoris/examples/blob/main/README.md)

You will primarily care about:

- interface boundaries;
- extension points;
- compatibility assumptions;
- configuration surfaces;
- observability integration;
- adapter and deployment patterns.

### For contributors

Start with:

- [Community](https://github.com/arcoris/community/blob/main/README.md)
- [Handbook](https://github.com/arcoris/handbook/blob/main/README.md)
- [Core repository](https://github.com/arcoris/arcoris/blob/main/README.md)
- [Enhancements](https://github.com/arcoris/enhancements/blob/main/README.md)

Contributors should understand:

- how the project is structured;
- how ownership and review work;
- when a change fits a normal pull request;
- when a change requires a tracked enhancement;
- how tests, docs, and release-facing changes are expected to be handled.

## Security

For responsible disclosure and security handling, see:

- [Security policy](https://github.com/arcoris/arcoris/blob/main/SECURITY.md)

Do not report sensitive vulnerabilities through public issues or public pull requests.

## Contributing

For contribution defaults and organization-level expectations, see:

- [Contributing guide](https://github.com/arcoris/arcoris/blob/main/CONTRIBUTING.md)
- [Community](https://github.com/arcoris/community/blob/main/README.md)
- [Handbook](https://github.com/arcoris/handbook/blob/main/README.md)

## Project Status

ARCORIS should be evaluated based on repository content, documented scope,
available examples, and the current state of tracked changes.

For the most accurate view of significant ongoing and upcoming work, see:

- [Enhancements](https://github.com/arcoris/enhancements/blob/main/README.md)

For the most accurate public usage and operational guidance, see:

- [Documentation](https://github.com/arcoris/docs/blob/main/README.md)

## Navigation Summary

If you remember only one thing, use this map:

- **What is ARCORIS?** -> [Core repository](https://github.com/arcoris/arcoris/blob/main/README.md)
- **How do I use, run, or operate it?** -> [Documentation](https://github.com/arcoris/docs/blob/main/README.md)
- **Where are runnable demos and setups?** -> [Examples](https://github.com/arcoris/examples/blob/main/README.md)
- **How does the project community work?** -> [Community](https://github.com/arcoris/community/blob/main/README.md)
- **How do engineering standards and review rules work?** -> [Handbook](https://github.com/arcoris/handbook/blob/main/README.md)
- **Where are major proposals and accepted decisions tracked?** -> [Enhancements](https://github.com/arcoris/enhancements/blob/main/README.md)
