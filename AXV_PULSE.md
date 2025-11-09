## 2025-11-09T23:48:06.050Z — Unknown

# AXV Pulse (rolling log)

## 2025-11-09 16:00 — Aster
- Status API: ok (stub-2025-11-09), nodes: degraded
- FE: <NodeStatusBar/> — dev w toku (mock)
- Infra: Nginx route /api/axv/* na staging z WG

## 2025-11-09 16:15 — Claude
- OpenAPI v0.1 dodane: /healthz, /status, /status/nodes
- Test: curl 200 OK, payload zgodny z kontraktem

## 2025-11-09 16:30 — Rezon
- Komponent NodeStatusBar: props z AXV_STATUS_URL
- Dodałem /public/api/axv/status.stub.json
