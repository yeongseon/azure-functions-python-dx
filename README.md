# Azure Functions Python DX

> A DX toolkit for Azure Functions Python: OpenAPI, validation, logging, diagnostics, scaffolding, and recipes.

Azure Functions Python is powerful, but once you move beyond simple examples, the developer experience can feel fragmented.

**This is not a framework.**
**This is a missing DX layer around Azure Functions Python.**

---

## Why this exists

In real projects, developers solve the same problems repeatedly:

- How do I generate OpenAPI / Swagger docs for HTTP-triggered functions?
- How do I validate request bodies, query parameters, and responses?
- How do I make logs easier to search in Application Insights?
- How do I check common configuration issues before deployment?
- How should I structure a production-style project?
- Where can I find practical examples beyond the official quickstarts?

This toolkit organizes those missing pieces into small, focused open-source projects.

---

## Tools

### Core DX

| Tool | Purpose | Status |
|---|---|---|
| [azure-functions-openapi-python](https://github.com/yeongseon/azure-functions-openapi-python) | Generate OpenAPI / Swagger docs for HTTP triggers | Usable |
| [azure-functions-doctor-python](https://github.com/yeongseon/azure-functions-doctor-python) | Run pre-deployment diagnostics | Usable |
| [azure-functions-validation-python](https://github.com/yeongseon/azure-functions-validation-python) | Request and response validation | Usable |
| [azure-functions-logging-python](https://github.com/yeongseon/azure-functions-logging-python) | Invocation-aware structured logging | Usable |

### Project Bootstrap

| Tool | Purpose | Status |
|---|---|---|
| [azure-functions-scaffold-python](https://github.com/yeongseon/azure-functions-scaffold-python) | Scaffold production-style projects | Early |
| [azure-functions-cookbook-python](https://github.com/yeongseon/azure-functions-cookbook-python) | Recipes, examples, and integration patterns | Early |

### Experimental / Advanced

| Tool | Purpose | Status |
|---|---|---|
| [azure-functions-db-python](https://github.com/yeongseon/azure-functions-db-python) | DB helper and pseudo-trigger patterns | Experimental |
| [azure-functions-langgraph-python](https://github.com/yeongseon/azure-functions-langgraph-python) | LangGraph integration patterns | Experimental |

---

## How the tools fit together

```text
Scaffold → Validation → OpenAPI → Logging → Doctor → Deploy
```

**Start with OpenAPI + Validation + Logging.** The rest is optional.

---

## Where to start

**Building HTTP APIs?**
→ [openapi](https://github.com/yeongseon/azure-functions-openapi-python) + [validation](https://github.com/yeongseon/azure-functions-validation-python) + [logging](https://github.com/yeongseon/azure-functions-logging-python)

**Preparing for deployment?**
→ [doctor](https://github.com/yeongseon/azure-functions-doctor-python) + [scaffold](https://github.com/yeongseon/azure-functions-scaffold-python)

**Exploring advanced workflows?**
→ [db](https://github.com/yeongseon/azure-functions-db-python) + [langgraph](https://github.com/yeongseon/azure-functions-langgraph-python)

---

## Example use cases

### 1. Build a documented HTTP API

Use **openapi** + **validation** + **logging** for:
OpenAPI / Swagger UI, typed request validation, consistent error responses, invocation-aware logs.

### 2. Check your project before deployment

Use **doctor** for:
Python version checks, dependency checks, host.json checks, common misconfiguration detection, CI-friendly diagnostics.

### 3. Start a new project faster

Use **scaffold** + **cookbook** for:
project templates, recommended folder structure, practical examples, reusable patterns.

### 4. Explore advanced serverless patterns

Use **db** + **langgraph** for:
DB-oriented workflow experiments, pseudo-trigger patterns, LangGraph workflow hosting patterns.

---

## Project status

Some packages are already usable for real projects. Others are experimental and still being shaped.

| Status | Meaning |
|---|---|
| **Usable** | Stable enough for real projects and feedback |
| **Early** | Usable but evolving |
| **Experimental** | Pattern exploration, expect changes |

---

## Design principles

1. **Stay close to Azure Functions** — enhance, don't replace the programming model.
2. **Small focused packages** — adopt only the parts you need.
3. **Production-style examples** — reflect real project needs, not just hello-world.
4. **CI/CD friendly** — works with GitHub Actions, Azure Developer CLI, Azure CLI.
5. **Clear boundaries** — experimental packages are clearly marked.

---

## Roadmap

See [ROADMAP.md](./ROADMAP.md) for the full roadmap.

---

## FAQ

See [docs/positioning.md](./docs/positioning.md) for:
- Why not just use FastAPI?
- Why not just use the official Azure Functions SDK?

---

## Related official resources

- [Azure Functions documentation](https://learn.microsoft.com/azure/azure-functions/)
- [Azure Functions Python developer guide](https://learn.microsoft.com/azure/azure-functions/functions-reference-python)
- [Azure Functions Core Tools](https://github.com/Azure/azure-functions-core-tools)
- [Azure Functions Python library](https://github.com/Azure/azure-functions-python-library)

---

## Contributing

See [CONTRIBUTING.md](./CONTRIBUTING.md).

If you are using Azure Functions Python and have a recurring pain point, please [open an issue](https://github.com/yeongseon/azure-functions-python-dx/issues/new).

---

## License

[MIT](./LICENSE)
