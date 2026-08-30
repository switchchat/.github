<p align="center">
  <img src="https://avatars.githubusercontent.com/u/262821873?v=4" alt="Nova" width="120">
</p>

# Nova

**Cactus x Google DeepMind Hackathon project for hybrid on-device and cloud AI assistance.**

Nova explores when an assistant should use a fast, private on-device FunctionGemma model and when it should fall back to Gemini for broader reasoning. It is a hackathon prototype and project record, not an employer or operating company.

## What We Built

- A hybrid routing strategy balancing correctness, latency, and local-model usage
- An Electron desktop overlay for voice, screen, and tool-assisted workflows
- A browser activity monitor with local categorization and cloud fallback
- Tool integrations for desktop actions and external services

## Demo Walkthrough

1. Start the local Cactus runtime and Nova backend.
2. Open either the desktop overlay or browser extension.
3. Submit a voice, text, screen, or browsing-context request.
4. Route suitable tool calls through the local FunctionGemma model.
5. Fall back to Gemini when the local result is uncertain or the task is broader.

## Architecture

```text
Desktop overlay or browser extension
               |
               v
Local Python service and hybrid router
        |                         |
        v                         v
FunctionGemma on device      Gemini fallback
        |
        v
Local tools and MCP integrations
```

## Public Repositories

| Repository | Purpose |
| --- | --- |
| [base](https://github.com/switchchat/base) | Original hybrid-routing challenge, benchmark, and submission workflow |
| [desktop](https://github.com/switchchat/desktop) | Electron desktop assistant and hybrid AI backend |
| [extension](https://github.com/switchchat/extension) | Chrome activity monitor and local analysis service |

## Project Status

Nova was built as a time-boxed hackathon collaboration. Privacy and latency statements describe the prototype design; users should review configuration and data flows before using external services.

[Explore the Nova repositories](https://github.com/orgs/switchchat/repositories)
