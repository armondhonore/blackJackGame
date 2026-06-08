# Nexlayer — blackJackGame

<!-- nexlayer:meta version=1 analyzed=2026-06-08T23:41:35Z repo=https://github.com/armondhonore/blackJackGame branch=main -->

> **For AI agents (Claude Code, Cursor, Gemini CLI, Copilot):**
> This file is the **project context** for this Nexlayer deployment — tech stack, env vars, secrets, live URL.
> For full platform detail (nexlayer.yaml schema, Dockerfile rules, CI/CD, task recipes) read **`nexlayer.skills`** in this repo.
>
> **Critical rules (full detail in `nexlayer.skills`):**
> - Inter-pod refs: `${podName:port}` only — never `localhost` or bare hostnames
> - Docker Hub images: prefix with `mirror.gcr.io/library/` — bare tags fail on the cluster
> - Secrets: set in the Nexlayer dashboard — never commit to `nexlayer.yaml` or Dockerfile
>
> **This file:** `agent-managed` sections update automatically. `user-editable` sections (Local Development Setup, Nexlayer Deployment Plan, Build Notes) are yours — preserved across re-analysis.

## Project Summary
<!-- nexlayer:section agent-managed=project_summary -->
A client-side Blackjack card game implementation utilizing HTML, CSS, and JavaScript for game logic and user interface.
<!-- nexlayer:end -->

## Technology Stack
<!-- nexlayer:section agent-managed=tech_stack -->
| Name | Kind | Version | Detected From |
|------|------|---------|---------------|
| HTML5 | language | 5 | index.html |
| CSS3 | language | 3 | css/ |
| JavaScript | language | ES6+ | js/ |
| Nginx | infra | latest | pod_topology |
<!-- nexlayer:end -->

## Repository Structure
<!-- nexlayer:section agent-managed=structure_map -->
- index.html — Main entry point and UI structure
- css/ — Stylesheets for game layout and aesthetics
- js/ — Game logic, deck management, and state handling
- images/ — Card and UI assets
<!-- nexlayer:end -->

## External Services Required
<!-- nexlayer:section agent-managed=external_deps -->
_No external services detected._
<!-- nexlayer:end -->

## Local Development Setup
<!-- nexlayer:section user-editable=local_setup -->
### Prerequisites

- Any modern web browser

### Steps

1. `git clone https://github.com/armondhonore/blackJackGame` — Clone the repository
2. `open index.html` — Open the HTML file in a browser to play

<!-- nexlayer:end -->

## Nexlayer Setup
<!-- nexlayer:section agent-managed=nexlayer_setup -->
### nexlayer.yaml

```yaml
application:
  name: pure-crane-blackjackgame
  pods:
    - name: app
      image: "# filled by pipeline"
      path: /
      servicePorts:
        - 80
      vars: {}
```

<!-- nexlayer:end -->

## Nexlayer Deployment Plan
<!-- nexlayer:section user-editable=deployment_plan -->
### Pod Topology

| Pod | Image | Port | Role |
|-----|-------|------|------|
| web-server | mirror.gcr.io/library/nginx:stable-alpine | 80 | web |

### Deployment notes

- The application is entirely static (frontend-only), requiring only a web server to serve the files.
- No backend or database pod is required as game state is handled in the client's browser memory.

<!-- nexlayer:end -->

## Build Notes
<!-- nexlayer:section user-editable=build_notes -->
<!-- Add notes for future builds here — preserved across re-analysis -->
<!-- nexlayer:end -->

## Nexlayer Configuration
<!-- nexlayer:section agent-managed=nexlayer_config -->
**Last deployed:** 2026-06-08T23:41:56Z  
**Live URL:** https://awesome-moose-pure-crane-blackjackgame.cloud.nexlayer.ai  
**Runtime:** docs · **Port:** 80  
**Deploy branch:** main  

```yaml
application:
  name: pure-crane-blackjackgame
  pods:
    - name: app
      image: "# filled by pipeline"
      path: /
      servicePorts:
        - 80
      vars: {}
```
<!-- nexlayer:end -->

## Build History
<!-- nexlayer:section agent-managed=build_history -->
| Date | Status | Notes |
|------|--------|-------|
| 2026-06-08T23:41:35Z | analyzed | initial repo analysis |
| 2026-06-08T23:41:56Z | success | deployed https://awesome-moose-pure-crane-blackjackgame.cloud.nexlayer.ai |
<!-- nexlayer:end -->
