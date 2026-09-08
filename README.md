# BJJ FPS Limiter

[![Build](https://github.com/NightZoom-BJJ/BJJ-FPS-Limiter/actions/workflows/build.yml/badge.svg)](https://github.com/NightZoom-BJJ/BJJ-FPS-Limiter/actions/workflows/build.yml)
[![Latest release](https://img.shields.io/github/v/release/NightZoom-BJJ/BJJ-FPS-Limiter)](https://github.com/NightZoom-BJJ/BJJ-FPS-Limiter/releases/latest)
[![License: GPL v3](https://img.shields.io/badge/license-GPLv3-blue)](LICENSE)

**A bjj_dev product** · built for the **NightZoom** racing server

Locks your game to a smooth **60 FPS**. A simple add-on for [ReShade](https://reshade.me) with
one button - turn it on to cap, turn it off to unlock.

<!-- TODO: re-shoot docs/overlay.png against the v3 overlay (bjj_dev logo + new credit line);
     the existing capture still shows the old NightZoom-branded window. -->

## Why 60?

GTA's physics is tied to your frame rate - cars handle differently at different FPS. Capping
everyone to the same 60 keeps racing fair, which is why the cap is a fixed 60 and not a slider.

## ⚠️ Please read first

Made for the **NightZoom** racing server, where it's allowed. On **other servers, use it at your
own risk** - every server sets its own rules, and some anticheats may flag add-ons that load into
the game. If you're unsure about a server, ask its staff first.

It needs the **add-on-enabled** build of ReShade - and the download includes it, so you're
covered even if you've never used ReShade. Graphics packs like NVE and QuantV already include
ReShade too.

## How to install

Download **`BJJ-FPS-Limiter…zip`** from the
[**Releases page**](https://github.com/NightZoom-BJJ/BJJ-FPS-Limiter/releases/latest), extract it,
and open the included **`Install Guide.html`** - it walks you through the whole setup, including the
one-time FiveM "ReShade was blocked" fix. The zip bundles ReShade, so it's all you need.

### Upgrading from the old NightZoom FPS Limiter

The add-on file was renamed in v3.0.0, so **delete the old `NZ-FPS-Limiter.addon64`** from your
`plugins` folder when you drop the new one in. ReShade loads *every* `.addon64` it finds, so
leaving both behind means two limiters each pacing the same frame - which caps you at roughly
**30 FPS**, not 60. Your on/off choice carries over automatically.

## Is it safe? What does it do?

This add-on is **open source**, so anyone can read exactly what it does. It only:

- caps your frame rate to 60 FPS,
- remembers your on/off choice,
- shows the logo, Discord link, and a link to the code.

It has **no ads, no tracking, no internet connection** (the only time it opens your browser is
when *you* click the Discord or GitHub buttons), and it doesn't touch your game's files.

The full source code is right here in this repo, and there's a **View Source on GitHub** button
inside the add-on too.

## Support

Found a bug, or something won't install?
**[Open an issue](https://github.com/NightZoom-BJJ/BJJ-FPS-Limiter/issues/new/choose)** - bug
reports and questions are both handled on GitHub, so answers stay searchable for the next person
who hits the same thing.

If the overlay never shows up, attach your **`ReShade.log`** to the issue. It sits next to ReShade
itself (in the same folder as the `.dll` you installed - for FiveM that's
`%LOCALAPPDATA%\FiveM\FiveM.app\plugins`), and the add-on writes to it, so it usually says exactly
what went wrong.

Not on the NightZoom server yet? The Discord is at <https://discord.gg/nightzoom> - that's the
place to get onto the server, not the place to report add-on bugs.

## Credits

- Maintained by **bjj_dev**
- Originally created by **Nipeno**, who wrote the limiter this is built on
- Testers: **Beanz**, **Cenkov**, **PhatWraith**, **krispy lzz**, **Wraith**, **hachiro**

## For developers

Want to build it yourself or see how it works? See **[BUILDING.md](BUILDING.md)**.
Contributions welcome - start with **[CONTRIBUTING.md](CONTRIBUTING.md)**.

## License

Free and open source under **GPLv3** - see [LICENSE](LICENSE). You can use, study, and modify it,
but any shared version must stay open source too.

This is a modified version of Nipeno's NightZoom FPS Limiter (v2.5.0), rebranded and maintained by
bjj_dev. The original copyright notice is kept in [`src/main.cpp`](src/main.cpp) alongside a summary
of what was changed, as GPLv3 requires.
