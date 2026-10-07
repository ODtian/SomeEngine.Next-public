# SomeEngine.Next

**C# game engine technology by YOJO — in development.**

SomeEngine.Next brings entity systems, graphics contracts, render-graph execution, asset ownership, and structured jobs into a modular C# foundation for real-time applications.

This repository is the public development snapshot of YOJO's SomeEngine.Next project. Source, architectural notes, samples, and tests describe the current engineering work; the product continues to evolve.

[Product website](https://studio.yojo.lol/engine.html) · [Technical overview](https://studio.yojo.lol/technology.html) · [Contact YOJO](mailto:hello@yojo.lol)

## Explore the source

| Area | Entry points |
| --- | --- |
| Entity systems | `src/SomeEngine.ECS`, `src/SomeEngine.ECS.Systems`, `src/SomeEngine.ECS.Serialization` |
| Graphics | `src/SomeEngine.Graphics`, `src/SomeEngine.Graphics.Direct3D12`, `src/SomeEngine.Graphics.Vulkan` |
| Render graph | `src/SomeEngine.RenderGraph`, `src/SomeEngine.RenderGraph.Diagnostics` |
| Rendering | `src/SomeEngine.Render`, `src/SomeEngine.Render.Cluster` |
| Assets | `src/SomeEngine.Assets`, `src/SomeEngine.Assets.Importers` |
| Jobs | `src/SomeEngine.Job`, `src/SomeEngine.Job.Contracts` |
| Samples and evidence | `samples/`, `tests/`, `benchmarks/` |

Start with [the project context](CONTEXT.md), [render boundaries](wiki/architecture/Render-Boundaries.md), [render graph](wiki/architecture/Render-Graph.md), and [ECS architecture](wiki/architecture/ECS-Architecture.md). The folders reflect areas of development; product scope and maturity are documented in the architectural notes.

## Development setup

Use the .NET SDK selected by [`global.json`](global.json). Clone recursively to obtain the declared external source dependencies:

```sh
git clone --recurse-submodules https://github.com/ODtian/SomeEngine.Next-public.git
cd SomeEngine.Next-public
dotnet build SomeEngine.slnx -c Release
dotnet test SomeEngine.slnx -c Release
```

Platform-specific graphics tests have their own requirements. `SomeEngine.slnx` is the ordinary product build and test entry point; `SomeEngine.Harness.slnx` is an optional development surface.

## Evaluation and licensing

For product evaluation, commercial use, integration, or licensing terms, contact **hello@yojo.lol**. Third-party components retain their respective licenses and notices.

## YOJO

YOJO develops high-performance C# game engine technology and client frameworks. Business contact: 556 Whispering Trl, Middletown, DE 19709, United States.
