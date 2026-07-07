<div align="center">

<img src="Alekrythae.png" alt="Alekrythae" width="100%">

# Ałek’ryŧhæ Core

### The shared runtime and service foundation behind `.alek` applications

**One Core. Many applications. Shared tools, services, and possibilities.**

Built with **C#**, **.NET**, **WPF**, and **Microsoft Edge WebView2**.

</div>

---

## About

**Ałek’ryŧhæ Core** is a modular, local-first Windows runtime designed to open, host, and support applications distributed in the custom `.alek` format.

Instead of packaging the same desktop infrastructure separately for every application, Core provides a reusable foundation for application hosting, window management, local storage, media access, and communication between JavaScript and C#.

Each `.alek` application can focus on its own interface, data, and product-specific behavior while Core handles the reusable infrastructure beneath it.

```text
Ałek’ryŧhæ Core
       │
       ├── Slideshow.alek
       ├── Pomodoro.alek
       ├── FaeraTh.alek
       └── MeggyTheDMMaster.alek
```

---

## Current Release

```text
Ałek’ryŧhæ Core v0.0.0
```

`v0.0.0` is the first public release of the current Core line.

The Windows release package is distributed as:

```text
Alekrythae-Core-v0.0.0-Windows-x64.zip
```

---

## Current Capabilities

Ałek’ryŧhæ Core v0.0.0 currently provides:

- `.alek` application hosting
- Windows `.alek` file association
- WPF and WebView2 desktop integration
- JavaScript-to-C# communication bridge
- Local JSON and text-file operations
- Controlled application-folder access
- Local image, audio, and external-media access
- `Picture` and `Music` folder discovery
- Natural filename ordering
- Ordered music playlist support
- MP3, M4A, WAV, OGG, and MP4 media support
- Multiple `.alek` application windows
- Single Core process with inter-process communication
- System-tray integration
- Full-screen application mode
- Local-first operation
- Clean uninstall support

---

## Application Model

Core and `.alek` applications remain separate.

```text
.alek Application
       │
       ▼
Ałek’ryŧhæ Core
       │
       ├── WPF Window Host
       ├── WebView2 Runtime
       ├── JavaScript ↔ C# Bridge
       ├── Local File Services
       ├── Media Services
       ├── Window Management
       └── Application Lifecycle
```

The Core supplies the reusable runtime.

Each `.alek` application supplies its own:

- User interface
- Styling
- Product-specific logic
- Local data structure
- Media and resources

This allows multiple applications to use the same desktop foundation without embedding their data directly into the Core.

---

## Single-File and Modular Applications

A `.alek` application may remain completely self-contained.

```text
Application.alek
```

The interface, styling, and application logic may all be stored inside the same `.alek` file.

External JavaScript files are not required.

Developers may also choose a modular structure when an application becomes larger or when responsibilities need to be separated.

```text
Application.alek
├── modules/
│   ├── storage.js
│   ├── calendar.js
│   └── media-controller.js
│
└── workers/
    ├── search-worker.js
    └── index-worker.js
```

In this optional model:

- The `.alek` application remains the main application-level controller.
- JavaScript modules may handle focused responsibilities.
- Background workers may perform heavier tasks without blocking the interface.
- Core may provide lifecycle management, permissions, storage, and shared services.

The same feature may still be implemented directly inside the `.alek` file when modular JavaScript files are unnecessary.

```text
Core runs the environment.
.alek controls the application.
Optional modules perform delegated tasks.
```

---

## Optional JavaScript Helpers

Future `.alek` applications may optionally delegate specific responsibilities to external JavaScript helpers.

Possible examples include:

- Search and filtering
- Data transformation
- Calendar calculations
- Media control
- Backup preparation
- Large JSON indexing
- Report generation
- Background processing

Example:

```text
MeggyTheDMMaster.alek
       │
       ├── character-manager.js
       ├── map-manager.js
       ├── calendar.js
       └── search-worker.js
```

This modular structure is optional.

A developer may choose either:

```text
Self-contained application
Application.alek
```

or:

```text
Modular application
Application.alek + optional JavaScript modules
```

Core is intended to support both approaches without forcing every application into the same structure.

---

## Design Philosophy

Ałek’ryŧhæ Core is intended to act as the common tool and service layer behind `.alek` applications.

A feature belongs in Core when it solves a reusable problem shared by multiple applications.

Application-specific behavior should remain inside the corresponding `.alek` application or its optional modules.

For example:

- Media discovery can belong to Core.
- A slideshow transition effect belongs to Slideshow.
- Local file persistence can belong to Core.
- A Pomodoro timing rule belongs to Pomodoro.
- Worker lifecycle management may belong to Core.
- A character-search algorithm belongs to MeggyTheDMMaster.

This separation allows Core to grow without turning every application into a copy of the same infrastructure.

---

## Media Conventions

Slideshow-style applications can use the following folders beside their `.alek` files:

```text
Picture/
Music/
```

### Picture

Supported image formats:

```text
.png
.jpg
.jpeg
.webp
.gif
```

### Music

Supported audio and media formats:

```text
.mp3
.m4a
.wav
.ogg
.mp4
```

For `.mp4` files, compatible applications use the audio track.

Core applies natural filename ordering.

```text
1.mp4
2.mp4
10.mp4
```

Result:

```text
1 → 2 → 10
```

Windows-style duplicate filenames are also ordered naturally:

```text
1 (1).mp4
1 (2).mp4
1 (10).mp4
```

Result:

```text
1 (1) → 1 (2) → 1 (10)
```

---

## Local-First Operation

Core is designed to run applications locally.

Application files and data are not automatically uploaded to an external server.

Core can provide local storage, media access, and application services without requiring every `.alek` application to build the same Windows integration separately.

The Core directory and application directories do not need to be stored in the same location.

Removing Core does not automatically remove application data stored elsewhere.

---

## Long-Term Direction

The current release operates as a Windows desktop runtime.

The project is designed to remain open to future capabilities such as:

- Optional JavaScript helper modules
- Optional background workers
- Manifest-based application packages
- Application-level task orchestration
- Worker lifecycle management
- Permission-based Core services
- Localhost-based application services
- Versioned local APIs
- Server-client communication
- WebSocket-based real-time updates
- Shared background services
- Browser-accessible local applications
- Database and backup services
- Multiple clients connected to one Core instance
- Local-network integrations
- Modular service extensions

> These items describe possible future directions. They are not included in the current v0.0.0 release.

A possible future modular model may look like this:

```text
                     ┌─────────────────────┐
                     │   .alek Application │
                     │     Orchestrator    │
                     └──────────┬──────────┘
                                │
              ┌─────────────────┼─────────────────┐
              │                 │                 │
       Internal Logic     JS Helper Module   Background Worker
              │                 │                 │
              └─────────────────┼─────────────────┘
                                │
                     ┌──────────▼──────────┐
                     │  Ałek’ryŧhæ Core    │
                     │ Runtime and Services│
                     └─────────────────────┘
```

A possible future service architecture may look like this:

```text
                    ┌─────────────────────┐
                    │   Desktop Client    │
                    │   WPF + WebView2    │
                    └──────────┬──────────┘
                               │
                    ┌──────────▼──────────┐
                    │  Ałek’ryŧhæ Core    │
                    │ Shared Service Host │
                    └──────────┬──────────┘
                               │
              ┌────────────────┼────────────────┐
              │                │                │
       Local HTTP API     WebSocket Hub    Storage Services
              │                │                │
       Browser Client     Other Clients    JSON / Database
```

---

## For Users

Do not download the repository source code unless you intend to inspect or build the project.

Download the Windows package from the GitHub **Releases** section:

```text
Alekrythae-Core-v0.0.0-Windows-x64.zip
```

Then:

1. Extract the ZIP completely.
2. Run `Alekrythae Core.exe`.
3. Allow Core to register the `.alek` file association.
4. Open compatible `.alek` applications.

Do not run Core directly from inside the ZIP archive.

### System Requirements

- Windows 10, 64-bit
- Windows 11, 64-bit
- Microsoft Edge WebView2 Runtime

The standard Windows release is published as self-contained. End users do not need the .NET SDK.

---

## For Developers

The repository contains the Core source code.

### Requirements

- .NET 10 SDK
- Windows 10 or Windows 11
- Internet access for the initial NuGet restore

### Build a Clean Release

Run:

```text
BUILD_CORE.cmd
```

The script creates:

```text
release/Alekrythae-Core-v0.0.0-Windows-x64.zip
```

Temporary build directories are removed after packaging.

---

## Keyboard and Window Behavior

- `F11` toggles full-screen mode.
- Double-clicking the title area can also toggle full screen.
- Normal window dragging remains available outside full-screen mode.
- Compatible `.alek` applications may provide additional shortcuts.

See [`WINDOW_BEHAVIOR.md`](WINDOW_BEHAVIOR.md) for additional details.

---

## Technology

- C#
- .NET 10
- WPF
- Windows Forms integration
- Microsoft Edge WebView2
- HTML
- CSS
- JavaScript
- JSON

---

## Repository Structure

```text
Alekrythae-Core-v0.0.0/
├── src/
│   └── Alekrythae.Core/
├── Alekrythae.sln
├── BUILD_CORE.cmd
├── CHANGELOG.md
├── LICENSE.md
├── README.md
├── SECURITY.md
├── VERSION
└── WINDOW_BEHAVIOR.md
```

---

## Security

Security information and vulnerability-reporting instructions are available in:

[`SECURITY.md`](SECURITY.md)

Future modular applications may require additional protections such as:

- Application-specific storage boundaries
- Module permission declarations
- Worker timeouts
- Module error isolation
- Core API versioning
- Package and manifest validation

---

## License

This project is proprietary, source-available software licensed under the:

**TheDEvorger Universal Proprietary Software License Version 1.0**

It is not open-source software.

Personal and non-commercial use is permitted only within the limits stated in [`LICENSE.md`](LICENSE.md).

Without prior written permission, commercial use, production use, redistribution, relicensing, unauthorized derivative distribution, and AI or machine-learning training are prohibited.

See the complete license:

[`LICENSE.md`](LICENSE.md)

---

## Author

Developed by **TheDEvorger**.

> **A modular master key for the expanding `.alek` application ecosystem.**
