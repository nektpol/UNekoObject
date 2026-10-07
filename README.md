# UNekoObject

**Modular gameplay systems for Unreal Engine.**

UNekoObject is a collection of reusable, self-contained systems built for **Unreal Engine**, with a focus on modular architecture, clear responsibilities, and practical game development.

The idea behind the project is simple:

> **Build systems that solve a problem without becoming the problem.**

Each system is developed as an independent Unreal Engine module, with clear boundaries and minimal coupling to the rest of the project. This makes the systems easier to understand, reuse, extend, and eventually move into another project.

## What is this?

UNekoObject is both a **collection of Unreal Engine systems** and an ongoing exploration of system design.

Instead of building everything directly into a game-specific codebase, the project looks at how common gameplay and technical systems can be designed as independent modules.

Examples include:

* Time management
* Game state management
* Event systems
* Save/load systems
* Gameplay utilities
* Other reusable gameplay and technical systems

Each system is developed independently and added to the repository as the project grows.

## The Philosophy

A system should know **what it is responsible for** — and, perhaps more importantly, what it is **not** responsible for.

UNekoObject focuses on:

### Modular Design

Each system lives in its own module and should be usable without requiring the entire project around it.

### Clear Responsibilities

Systems should have a well-defined purpose rather than slowly turning into a convenient place for unrelated functionality.

### Low Coupling

A system should depend on as little of the rest of the game as reasonably possible.

### Explicit Communication

When systems need to communicate, that communication should happen through clear interfaces, APIs, delegates, events, or other intentional boundaries.

### Reusability

A useful system shouldn't have to be rewritten every time a new project starts.

### Practical Architecture

Architecture exists to solve problems, not to win arguments on a whiteboard.

There will be trade-offs. There will be compromises. And sometimes the simplest solution is the best one.

The goal is not to build the most sophisticated architecture possible.

The goal is to build something that remains **understandable and maintainable when the project gets bigger.**

## Repository Structure

Each system is organized as an independent Unreal Engine module.

```text
UNekoObject/
│
├── Source/
│   ├── TimeManager/
│   │   ├── Public/
│   │   └── Private/
│   │
│   ├── ...
│
├── Content/
├── Config/
│
└── README.md
```

Each module can have its own documentation explaining:

* What problem it solves
* Its responsibilities
* Its architecture
* Public interfaces
* How to integrate it
* Design decisions
* Known limitations
* Possible future improvements

## Systems

### Time Manager

A centralized game-wide time management system.

It provides a single place to manage concepts such as:

* Time progression
* Pausing
* Time scaling
* Different time states
* Communication with systems that depend on game time

The goal is to prevent individual gameplay systems from implementing their own interpretation of game time.

More systems will be added over time.

## Unreal Engine

UNekoObject is primarily developed using **C++ for Unreal Engine**, with Blueprint integration where appropriate.

The project is intended to demonstrate not only how individual systems can be implemented, but also how they can be structured as reusable Unreal Engine modules.

## Why does this exist?

Because building a feature is only half the problem.

The other half is deciding **where that feature belongs, what it should know, and how the rest of the game should interact with it.**

A system that works perfectly in isolation can still become painful to maintain if its architecture creates unnecessary dependencies.

UNekoObject explores that part of development.

Not just:

> "How do I build this?"

But also:

> "What should this actually be?"

> "Who should own this responsibility?"

> "What should this system know?"

> "How do other systems interact with it?"

> "Can I take this system to another project without taking the entire game with it?"

## Development Series

UNekoObject is also the companion repository for a series about **Unreal Engine system design and implementation**.

The series focuses on the reasoning behind the systems as much as the implementation itself.

The goal is to show the process from:

**Problem → Requirements → Responsibilities → Architecture → Implementation → Integration → Refinement**

rather than jumping directly into code.

The repository will evolve alongside the series, so some systems may be refactored as better solutions are discovered.

And honestly, that's intentional.

Architecture isn't something you get right once and then frame on the wall.

---

## Status

🚧 **Work in Progress**

UNekoObject is actively evolving.

New systems, documentation, examples, and improvements will be added over time.

---

**UNekoObject — Build systems, not dependencies.**

