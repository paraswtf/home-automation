# Project Context

Read [README.md](README.md) for full project context including architecture, tech stack, WebSocket protocol, database schema, ESP32 boot flow, and design decisions.

## Quick Reference

- **Dashboard**: `dashboard/` — Next.js 16, tRPC v11, Prisma/MongoDB, NextAuth v5, WebSocket server (port 4001)
- **Firmware**: `firmware/` — ESP32 Arduino (PlatformIO), WebSocket client, NVS storage
- **Monorepo**: npm workspaces — run `npm run dev` / `npm run ws` from root
- **Server is authoritative** for relay states; ESP32 syncs from server
- **Online status**: on-demand via `pingDevice` (no `lastSeenAt` in DB)
