# Security Policy

This project ships a DLL that loads into a running game process, plus a `.bat` that edits a FiveM
config file. That deserves a real disclosure policy, so here it is.

## Supported versions

Only the [latest release](https://github.com/NightZoom-BJJ/BJJ-FPS-Limiter/releases/latest) is
supported. Fixes go into a new release rather than patches for older tags.

## Reporting a vulnerability

**Do not open a public issue for a security problem.**

Use GitHub's private vulnerability reporting:
[**Report a vulnerability**](https://github.com/NightZoom-BJJ/BJJ-FPS-Limiter/security/advisories/new).
That opens a private thread visible only to the maintainer.

Please include what an attacker could achieve, the steps to reproduce, and your Windows / FiveM /
ReShade versions.

This is a spare-time project with no maintenance schedule and **no guaranteed response time** -
reports get read when they get read. If something is being actively exploited and you have had no
reply, disclose it publicly rather than sitting on it; players are better off knowing.

## What this add-on does and doesn't do

Useful when judging whether something is a real vulnerability or expected behaviour. The add-on:

- caps the frame rate, and stores a single on/off value in ReShade's own config;
- decodes a logo that is embedded in the DLL itself — no image file is read from disk;
- opens your browser **only** when you click the Discord or GitHub button in the overlay.

It makes **no network connections**, collects **no telemetry**, and does not read or modify game
files. The one thing that writes outside its own config is the optional `Enable-ReShade.bat`, which
adds a single `ReShade5=` line to FiveM's `CitizenFX.ini` — the same line FiveM asks you to add by
hand, using the standard Windows INI API so the rest of the file is left alone.

## Things that are not vulnerabilities

- **SmartScreen / antivirus warnings.** The downloads are unsigned (code-signing certificates cost
  money this project doesn't have) and a DLL that injects into a game is inherently
  heuristic-flaggy. Build from source if you'd rather not trust the binary — see
  [BUILDING.md](BUILDING.md).
- **Getting banned on another server.** The add-on is made for NightZoom. Other servers set their
  own rules and their anticheats may flag any injected add-on. That's a policy risk, not a security
  bug.
- **Bundled ReShade issues.** Each release bundles official ReShade, unmodified. Report ReShade
  vulnerabilities to [crosire/reshade](https://github.com/crosire/reshade).
