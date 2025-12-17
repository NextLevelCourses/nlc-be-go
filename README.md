
# nlc-be-go — index-services

Minimal README for the small Go service in this repository.

## What this is

This repository contains a tiny HTTP index service written with the Fiber web framework.
The service listens on port 7000 and responds to GET / with a short welcome message.

## Module

module: `github.com/NextLevelCourses/nlc-be-go/index-services`

Go version: `1.24.4` (from `go.mod`)

## Prerequisites

- Go toolchain installed (Go 1.24.x recommended).

## Build

From the repository root you can build the index service:

```bash
cd index-services
go build -o nlc-index .
```

Or run directly with:

```bash
cd index-services
go run main.go
```

## Run

After building:

```bash
./index-services/nlc-index  # if run from repo root
# or
./nlc-index                # if run from index-services/
```

The service listens by default on port `7000`.

## Quick test

With the service running (port 7000):

```bash
curl -i http://localhost:7000/

# Expected body:
# Hello welcome index service!
```

## Files of interest

- `index-services/main.go` — main service implementation (uses `github.com/gofiber/fiber/v2`).
- `index-services/go.mod` — module and dependency list.

## Notes

- No environment variables are required for the simple index endpoint.
- If you plan to containerize or add configuration, include instructions here.

---

If you'd like, I can add a minimal Makefile, a Dockerfile, or CI job to build and test this service.
