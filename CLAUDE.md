# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

```bash
npm run dev       # Start Vite dev server
npm run build     # TypeScript compile + Vite build
npm run lint      # ESLint with zero-warning policy
npm test          # Run Vitest tests
```

## Architecture

React + TypeScript app that generates parking exit ticket barcodes. Built with Vite and deployed to GitHub Pages.

**Core flow:** `App.tsx` displays a ticket with a barcode encoding a calculated exit code. The code updates every second and includes a 20-minute buffer window from the current time.

**Code generation** (`src/utils/calculateCode.ts`): Concatenates a constant (289) + gate value (1=entrance, 9=exit) + day-of-year + seconds-since-midnight + a user-adjustable magic number (0-9). The `Gate` enum controls entrance vs exit encoding.

**Barcode rendering**: Uses `react-barcode` to render the calculated code as a visual barcode.

## Deployment

GitHub Pages via `.github/workflows/deploy.yml`. The Vite base path is `/hiperdino-parking-opener`.
