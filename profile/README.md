# Open Engineering Assembly

**From reusable building blocks to working engineering solutions.**

Open Engineering Assembly is the implementation capability of the Open Engineering ecosystem responsible for turning assembly definitions into concrete, validated, versioned, and reusable engineering solutions.

Inspired by the LEGO system, Open Engineering treats architecture and software products as assemblies of reusable building blocks rather than monolithic constructions.

An Assembly is not merely a diagram or a collection of components.

It is an identifiable, reproducible engineering composition with defined dependencies, configuration, interfaces, and lifecycle.

## What Is an Assembly?

An **Open Engineering Assembly** is a concrete implementation of an assembly definition maintained by [Open Engineering Assemblies](https://github.com/open-engineering-assemblies).

It brings together reusable building blocks into a coherent engineering solution.

An Assembly may contain:

- Bricks and models
- Capsules and capabilities
- Systems and components
- Relationships and interfaces
- Configuration and scenarios
- Specifications and architectural decisions
- Dependencies and constraints
- Generated artifacts and documentation

The essential principle is:

> Define the assembly once. Instantiate, configure, validate, and reuse it wherever needed.

## Definitions and Implementations

Open Engineering distinguishes between defining an engineering concept and implementing it.

| Definition | Implementation | Responsibility |
|---|---|---|
| [Open Engineering Bricks](https://github.com/open-engineering-bricks) | [Open Engineering Brick](https://github.com/open-engineering-brick) | Define and implement reusable building blocks |
| [Open Engineering Assemblies](https://github.com/open-engineering-assemblies) | **Open Engineering Assembly** | Define and implement compositions of building blocks |

The plural organization establishes the vocabulary, contracts, schemas, and composition rules.

The singular organization provides concrete implementations, assembly tooling, validation, and lifecycle management.

## The Assembly Model

```text
Open Engineering Assemblies
    │
    │ Defines assembly contracts
    ▼
Open Engineering Assembly
    │
    ├── Resolve building blocks
    ├── Resolve dependencies
    ├── Apply configuration
    ├── Compose components
    ├── Validate constraints
    ├── Generate artifacts
    └── Publish implementation
             │
             ▼
       Engineering Product
```

A product can itself be assembled from smaller assemblies, allowing hierarchical composition and reuse.

## Assembly Manifest

An assembly should be described using a machine-readable manifest.

The following YAML illustrates a proposed manifest structure. Its schema is illustrative rather than an already established contract.

```yaml
apiVersion: open-engineering.io/v1alpha1
kind: Assembly

metadata:
  name: example-architecture
  version: 1.0.0
  description: Example engineering assembly

spec:
  definition:
    name: architecture-assembly
    version: 1.0.0

  components:
    - name: developer-bench
      kind: system
      model: devbench.glb

    - name: testing-pod
      kind: container
      model: testing-pod.glb

  relationships:
    - source: developer-bench
      target: testing-pod
      type: connects-to

  configuration:
    scenario: secure
    protocol: HTTPS

  validation:
    enabled: true

  outputs:
    - type: architecture-model
    - type: visualization
    - type: documentation
```

The manifest describes the intended composition, not the implementation details of every individual component.

## Assembly Lifecycle

An Assembly follows a reproducible engineering lifecycle.

```text
Definition
    ↓
Instantiation
    ↓
Dependency Resolution
    ↓
Configuration
    ↓
Composition
    ↓
Validation
    ↓
Artifact Generation
    ↓
Publication
    ↓
Consumption
    ↓
Observation and Evolution
```

Each stage should be independently inspectable and, wherever practical, automated.

### 1. Instantiate

Create a concrete assembly from a versioned definition.

### 2. Resolve

Locate the required bricks, models, capsules, systems, and dependent assemblies.

### 3. Configure

Apply product-specific settings, environments, and scenarios without modifying reusable definitions.

### 4. Compose

Connect components according to declared relationships, interfaces, and constraints.

### 5. Validate

Verify structural consistency, dependency compatibility, interface contracts, and relevant engineering specifications.

### 6. Publish

Produce versioned artifacts with traceable inputs, provenance, and integrity information.

### 7. Reuse

Make the resulting assembly available for consumption by other assemblies, products, and engineering tools.

## Products Built from Assemblies

### Open Engineering Architecture

[Open Engineering Architecture](https://github.com/open-engineering-architecture) can be implemented as an assembly of architectural capabilities.

Its components may include:

- Systems and relationships
- Architecture Decision Records
- Specifications
- Scenarios
- Assessments
- Missions
- Visualizations
- Models and digital twins

Architecture therefore becomes something that can be assembled, configured, analyzed, and explored rather than only documented.

### Agility Game

[Agility Game](https://github.com/agility-game) can use the same assembly principles to create an interactive business simulation.

Its components may include:

- Game board and spaces
- Players and characters
- Rules and missions
- Events and scenarios
- Simulations and interactions
- Scoring and feedback
- Visual and interactive representations

The products are different, but their assembly mechanisms can be shared.

## Assemblies of Assemblies

Assemblies support hierarchical composition.

```text
Product
  │
  ├── Assembly A
  │     ├── Brick 1
  │     ├── Brick 2
  │     └── Assembly B
  │           ├── Brick 3
  │           └── Brick 4
  │
  └── Assembly C
        ├── Capsule
        ├── System
        └── Model
```

This enables large engineering solutions to emerge from smaller, independently reusable compositions.

An Assembly can be a component of another Assembly without losing its own identity, version, or provenance.

## Engineering Principles

Open Engineering Assembly follows several fundamental principles.

1. **Composition over duplication** — Reuse existing building blocks before introducing new ones.
2. **Definitions before implementations** — Separate what an assembly means from how it is instantiated.
3. **Explicit dependencies** — Declare and resolve required components and versions.
4. **Reproducibility** — The same inputs and configuration should produce equivalent results.
5. **Traceability** — Preserve relationships between definitions, implementations, decisions, and artifacts.
6. **Validation by design** — Treat consistency, compatibility, and compliance as assembly responsibilities.
7. **Hierarchical composition** — Allow assemblies to contain other assemblies.
8. **Product independence** — Keep assembly mechanisms reusable across different engineering products.
9. **Versioned evolution** — Enable assemblies to evolve without silently breaking consumers.
10. **Existing gravity** — Audit and reuse established capabilities before creating new implementations.

## Automation and Integration

Assembly implementations should be suitable for automated processing through GitHub Actions and other engineering workflows.

Potential integrations include:

- GitHub repositories, Actions, and Releases
- Open Engineering Model and GLB artifacts
- LDraw-based brick models
- LikeC4 architecture models
- Babylon.js visualizations
- Kubernetes and GitOps tooling
- Open Engineering Capsules and Composers
- Artifact registries and provenance systems

The intended workflow is:

```text
Assembly Manifest
       ↓
GitHub Workflow
       ↓
Assembly Resolver
       ↓
Assembly Composer
       ↓
Validation
       ↓
Generated Artifacts
       ↓
GitHub Release / Registry
       ↓
Consuming Products
```

The concrete implementation and supporting tooling can evolve independently of the assembly definition.

## Related Organizations

| Organization | Responsibility |
|---|---|
| [Open Engineering Bricks](https://github.com/open-engineering-bricks) | Reusable building-block definitions |
| [Open Engineering Brick](https://github.com/open-engineering-brick) | Individual building-block implementations |
| [Open Engineering Assemblies](https://github.com/open-engineering-assemblies) | Assembly definitions, contracts, and composition rules |
| **Open Engineering Assembly** | Concrete assembly implementations and lifecycle |
| [Open Engineering Architecture](https://github.com/open-engineering-architecture) | Architectural product and system knowledge |
| [Open Engineering Model](https://github.com/open-engineering-model) | Reusable 3D engineering models and artifacts |

## Vision

Traditional engineering often starts by building a solution from scratch.

Open Engineering starts by identifying what already exists, understanding how it fits together, and assembling a solution from reusable parts.

The result is a shift:

**From building systems to assembling systems.**

**From isolated implementations to reusable compositions.**

**From static architecture to living engineering products.**

---

**Open Engineering Assembly**

*Define with Assemblies. Implement with Assembly. Build with Bricks. Create with confidence.*

[Assembly Definitions](https://github.com/open-engineering-assemblies) · [Architecture](https://github.com/open-engineering-architecture) · [Bricks](https://github.com/open-engineering-bricks)
