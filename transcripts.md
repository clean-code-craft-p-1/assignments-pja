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

## Ecosystem

| Purpose        | Recommendation          |
| -------------- | ----------------------- |
| JDK            | Eclipse Temurin OpenJDK |
| Language level | Java 21 or 25           |
| Build tool     | Maven or Gradle         |
| Framework      | Spring Boot             |
| Testing        | JUnit 5 + Mockito       |
| Packaging      | Docker                  |
| Deployment     | Kubernetes              |
| IDE            | VS Code, Eclipse        |

## Modularity

Modularity is the practice of breaking down code into smaller pieces. This makes it easier to understand, test, and maintain.

However, cutting code arbitrarily can lead to confusion. [Naming by purpose](naming.md) is the easiest way to validate if you're on the right path. Explore this, and more ways to reduce cognitive load.