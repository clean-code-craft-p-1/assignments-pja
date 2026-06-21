# Course transcripts

This page covers the concepts covered in the exercises

## Purpose

Build habits for productivity and reliability.

```mermaid
graph LR
    subgraph Productivity
        A1["Quick releases"]
        A2["More features"]
        A3["Smaller teams"]
        A4["Deadlines"]
        A[Productivity]
        A1 --> A
        A2 --> A
        A3 --> A
        A4 --> A
    end

    subgraph Reliability
        B1["Test coverage"]
        B2["Linters"]
        B3["Modularity"]
        B4["Graceful degradation"]
        B[Reliability]
        B1 --> B
        B2 --> B
        B3 --> B
        B4 --> B
    end

    C["Productivity AND Reliability"]
    A --> C
    B --> C
```

## Cycle of value

The cycle of value is a cycle of writing code, testing it, and then refactoring it to improve its quality.
This cycle keeps the code healthy and easy to maintain.
It's like brushing your teeth - do it every day to keep your teeth healthy.

```mermaid
graph TD
    M["Modularity"] --> T["FIRST tests"]
    T --> F["Frequent releases"]
    F --> C["Continuous improvement<br>Shift left"]
    C --> X["Control complexity"]
    X --> M
```

## Tests

Follow the FIRST principles for writing tests:

| Principle | Enables | Benefits |
|-----------|---------|----------|
| Fast      | Frequent execution | Find issues early |
| Independent| Isolation of tests | Easier failure diagnosis |
| Repeatable | Consistent results | Stable tests, low maintenance |
| Self-validating| Automatic pass/fail | Reduced manual effort - single Pass/Fail result |
| Thorough   | Coverage with strong asserts | Passing tests ensure customer satisfaction |

## Ecosystem

| Purpose        | Examples - Java         | Examples - C# |
| -------------- | ----------------------- |---------------|
| Development (JDK) | Temurin OpenJDK      | .Net SDK      |
| Language       | Java 21 or 25           | C# 13 or 15   |
| Development (IDE) | VS Code, Eclipse     | Visual Studio, VS Code |
| Build          | Maven or Gradle         | dotnet        |
| Framework      | Spring Boot             | ASP.Net       |
| Testing        | JUnit 5 + Mockito       | xUnit         |
| Packaging      | Docker                  | Docker        |
| Deployment     | Kubernetes              | Kubernetes    |

## LLM Ecosystem

Recognize:

1. Your prompt
1. Its context
1. Model

## Modularity

Modularity is the practice of breaking down code into smaller pieces. This makes it easier to understand, test, and maintain.

However, cutting code arbitrarily can lead to confusion. [Naming by purpose](naming.md) is the easiest way to validate if you're on the right path. Explore this, and more ways to reduce cognitive load.

Other principles that help in a beneficial cut:

### Separate by lifecycle

Keep stable code separate from evolving code.
The feature to "display the summary" can change by user-preference.
Hence, separate it from "reading the data", which goes by a standard / agreed interface.

### Name by purpose

Names for files, classes, or functions should be self-evident.
A good name conveys purpose - without digging further into their code or comments.
This saves time when reading code.

### Avoid side effects

Side effects are changes to state - display, storage, network, etc.
They bring dependency. Isolate your logic into pure functions that return a value without changing the state.
Keep dependencies separate.

### Inject dependencies

When it isn't possible to isolate with pure functions, inject dependencies.
Pass in the dependencies as parameters, rather than hardcoding them.
This makes it easy to mock the dependencies in tests, and to swap them out in production.

### Boundary under test

What you prove: "It functions as expected". What is "it"?

- The logic?
- With its dependencies?
- In one configuration?
- In one caller?

## AI generation - intuition

Use-cases:

- AI for Code-generation, understanding legacy code
- AI for end-user functionality (e.g., summarization, chat-bot)
- AI for automation (e.g., voice agents, meetings)
