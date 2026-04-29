# Positioning

## Why not just use FastAPI?

FastAPI is excellent.

This toolkit is not trying to replace FastAPI.

It is for developers and teams that **already use the Azure Functions Python programming model** and want lightweight helpers around documentation, validation, logging, diagnostics, and project structure.

- **Use FastAPI** if you want a full web framework.
- **Use this toolkit** if you want to stay close to Azure Functions Python while improving the developer experience.

Azure Functions Python has its own programming model (v2 with decorators). Some teams choose it for tight Azure integration, consumption-based billing, or organizational standards. This toolkit helps those teams ship production-quality projects without switching frameworks.

---

## Why not just use the official Azure Functions SDK?

The official Azure Functions SDK and Core Tools are the foundation. This toolkit is not a replacement.

Instead, it adds helper layers around common project needs:

| Need | Official SDK | This toolkit |
|---|---|---|
| Function triggers and bindings | ✅ Built-in | — |
| API documentation (OpenAPI) | ❌ Not included | ✅ openapi package |
| Request/response validation | ❌ Not included | ✅ validation package |
| Structured logging with invocation context | ❌ Basic logging only | ✅ logging package |
| Pre-deployment diagnostics | ❌ Not included | ✅ doctor package |
| Project scaffolding | ⚠️ Basic `func init` only | ✅ scaffold package |
| Practical recipes and examples | ⚠️ Official quickstarts only | ✅ cookbook package |

Think of it as a **practical DX layer on top of Azure Functions Python**.

---

## How is this different from a framework?

A framework controls your application structure. This toolkit doesn't.

- Each package is **independent** — use one, some, or all.
- No custom base classes, decorators that hijack your code, or required configuration.
- Your functions stay standard Azure Functions Python functions.
- You can adopt or remove any package without rewriting your project.
