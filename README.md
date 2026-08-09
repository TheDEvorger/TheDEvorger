<div align="center">

<img src="Alekrythae.png" alt="Ałek’ryŧhæ" width="100%">

# Ałek’ryŧhæ

### A shared software ecosystem powered by Ałek’ryŧhæ Core and `.alek` applications

**One Core. Many `.alek` applications.**

Built with technologies including **C#**, **.NET**, **WebView2**, **React**, **TypeScript**, **HTML**, **CSS**, **JavaScript**, **SQLite**, and **JSON**.

</div>

---

## About

**Ałek’ryŧhæ** is an independent software ecosystem built around a shared Windows runtime named **Ałek’ryŧhæ Core** and applications distributed in the custom **`.alek` application format**.

Ałek’ryŧhæ Core provides the common runtime environment required to open, host, manage, and execute compatible `.alek` applications.

Each `.alek` application defines its own:

* Product purpose
* Interface
* Application logic
* Data model
* Resources
* Configuration
* Features
* Visual identity
* Application-specific behaviour

The Core and `.alek` applications are separate components, but compatible `.alek` applications are designed to run through Ałek’ryŧhæ Core rather than as unrelated standalone executables.

The ecosystem is designed around:

* Shared runtime infrastructure
* Product-specific application behaviour
* Local-first data ownership
* Consistent system services
* Strong visual identity
* Modular application distribution
* Long-term compatibility and maintainability

---

## Core and Application Model

The ecosystem consists of two primary layers:

```text
Ałek’ryŧhæ Ecosystem
       │
       ├── Ałek’ryŧhæ Core
       │   ├── Application Runtime
       │   ├── .alek Package Loader
       │   ├── Window and Interface Hosting
       │   ├── File and Data Services
       │   ├── Media Services
       │   ├── Security and Validation
       │   ├── Shared System Integration
       │   ├── Application Lifecycle
       │   └── Compatibility Services
       │
       └── .alek Applications
           ├── Application Definition
           ├── Interface
           ├── Product Logic
           ├── Data Model
           ├── Resources
           ├── Application Configuration
           ├── Product-Specific Features
           └── Visual Identity
```

Ałek’ryŧhæ Core provides the shared technical foundation.

The `.alek` application provides the actual product experience.

This model allows applications to remain distinct without duplicating the entire runtime, window system, storage foundation, media infrastructure, and integration layer inside every product.

---

## Ałek’ryŧhæ Core

**Ałek’ryŧhæ Core** is the central Windows runtime of the ecosystem.

Its responsibilities may include:

* Discovering and opening `.alek` applications
* Validating application packages
* Managing application lifecycle
* Hosting application interfaces
* Providing shared window behaviour
* Providing local file and data services
* Managing application-specific storage locations
* Providing media and resource services
* Managing compatibility between Core and application versions
* Providing shared security controls
* Supporting updates and migrations
* Exposing approved runtime services to applications
* Maintaining separation between installed applications
* Providing common desktop integration

The Core does not make every application identical.

It supplies the common foundation while allowing each `.alek` application to define its own interface, systems, data structures, workflows, and identity.

---

## The `.alek` Application Format

A `.alek` file is an application package designed to be opened and executed through Ałek’ryŧhæ Core.

Depending on the application, a `.alek` package may contain or reference:

* Application metadata
* Application identity
* Version information
* Core compatibility requirements
* Interface definitions
* Application logic
* Local modules
* SQLite database structures
* JSON configuration or exchange data
* Images
* Icons
* Audio
* Fonts where legally distributable
* Themes
* Scripts
* Documentation
* Migration information
* Product-specific resources

A `.alek` application is not merely a document or project file.

It represents an installable or loadable application unit within the Ałek’ryŧhæ ecosystem.

---

## Application Architecture

Each `.alek` application is structured according to the needs of its product while operating through the shared Core runtime.

```text
Application.alek
       │
       ├── Manifest
       │   ├── Application Identity
       │   ├── Version
       │   ├── Core Compatibility
       │   ├── Permissions
       │   └── Entry Definition
       │
       ├── Interface
       │   ├── Layout
       │   ├── Interaction
       │   ├── Animation
       │   └── Visual System
       │
       ├── Application Logic
       │   ├── Product Features
       │   ├── Workflows
       │   ├── Commands
       │   └── Application Rules
       │
       ├── Data
       │   ├── SQLite Structures
       │   ├── Configuration
       │   ├── Local Project Data
       │   └── Migration Definitions
       │
       ├── Resources
       │   ├── Images
       │   ├── Audio
       │   ├── Icons
       │   └── Product Assets
       │
       └── Documentation
```

The exact internal structure may vary between applications.

A lightweight utility may contain only a small interface and limited application logic, while a larger `.alek` application may include multiple systems, databases, modules, media resources, and complex workflows.

All access to shared runtime capabilities must occur through services intentionally provided by Ałek’ryŧhæ Core.

---

## Application Separation

Every `.alek` application remains a distinct product within the shared ecosystem.

Applications may have separate:

* Names
* Versions
* Interfaces
* Data models
* Resources
* Settings
* Storage areas
* Documentation
* Release histories
* Compatibility requirements
* Product roadmaps

Application-specific data must not be unintentionally shared with another `.alek` application.

Shared services provided by the Core do not mean that applications share all data, settings, or internal behaviour.

Cross-application communication or shared resources should occur only through explicitly designed Core services.

---

## Development Direction

The ecosystem focuses on developing a stable Core runtime together with distinct `.alek` applications.

This includes:

* Core runtime architecture
* `.alek` package loading and validation
* Application lifecycle management
* Frontend architecture and interaction design
* Application-specific logic
* Windows desktop integration
* Local file and database systems
* Media handling and processing
* Data isolation and recovery
* Core and application compatibility
* Application packaging
* Version migration systems
* Performance-conscious animation
* Product-specific visual systems
* Long-term maintainability

---

## Projects

### Ałek’ryŧhæ Core

The shared Windows runtime used to open, host, and execute compatible `.alek` applications.

Its direction includes:

* `.alek` application loading
* Application validation
* Shared runtime services
* Window and interface hosting
* Local storage services
* Media services
* Application isolation
* Core compatibility management
* Update and migration support
* Shared Windows integration

---

### Meggy The DM Master

A `.alek` desktop application for tabletop role-playing game preparation, world management, travel, simulation, and campaign organization.

Its planned and active systems include:

* Adventure management
* Character and location systems
* Lore management
* Maps and world navigation
* Journey and exploration systems
* Time and calendar systems
* Music and ambience controls
* Local campaign storage
* Campaign-focused data organization
* Character and location cards
* Nested world structures
* World simulation systems

Meggy The DM Master is distributed as a `.alek` application and requires a compatible version of Ałek’ryŧhæ Core.

---

### Ałek’ryŧhæ Tlaengor

A `.alek` document and knowledge workspace designed for Markdown, JSON, TXT, media, notes, and structured project material.

Its direction includes:

* Multi-format document viewing
* Project navigation
* Search and filtering
* Document combination
* Structured data presentation
* Media playback
* Custom visual workspaces
* Local-first project organization

Ałek’ryŧhæ Tlaengor is distributed as a `.alek` application and requires a compatible version of Ałek’ryŧhæ Core.

---

### Mavi Ay Ekran Filtresi

A `.alek` Windows eye-comfort application focused on screen temperature, brightness, scheduling, and per-monitor control.

Its direction includes:

* Color-temperature adjustment
* Brightness and dimming controls
* Scheduled transitions
* Per-monitor settings
* Full-screen pause behaviour
* Rest reminders
* Smooth visual transitions

Mavi Ay Ekran Filtresi is distributed as a `.alek` application and requires a compatible version of Ałek’ryŧhæ Core.

---

### Ałek’ryŧhæ Slideshow

A `.alek` slideshow and local media presentation application.

Its direction includes:

* Large image collections
* Ordered image playback
* Music playlists
* Soft audio transitions
* Keyboard navigation
* Local image and media folders
* Full-screen presentation

Ałek’ryŧhæ Slideshow is distributed as a `.alek` application and requires a compatible version of Ałek’ryŧhæ Core.

---

### Ałek’ryŧhæ Pomodoro

A `.alek` productivity application with a cosmic visual identity and configurable work-rest cycles.

Its direction includes:

* Focus and break sessions
* Configurable timing
* Visual state transitions
* Animated atmospheric backgrounds
* Session tracking
* Local preferences

Ałek’ryŧhæ Pomodoro is distributed as a `.alek` application and requires a compatible version of Ałek’ryŧhæ Core.

---

## Design Principles

### One Core, Many Applications

Ałek’ryŧhæ Core provides the shared runtime foundation, while each `.alek` application remains a distinct product.

### Product-Specific Behaviour

Applications define their own purpose, workflows, logic, data structures, resources, and visual identity.

### Shared Infrastructure

Common technical requirements should be handled by the Core where practical rather than independently duplicated inside every application.

### Application Isolation

Each `.alek` application should maintain its own storage, configuration, resources, and runtime state unless sharing is explicitly intended.

### Local-First

Applications are designed to keep user projects and data under the user’s control whenever possible.

### Predictable Storage

Application data should be stored in clear, recoverable, and application-specific locations.

### Visual Identity

Interface design, animation, atmosphere, and branding are treated as functional parts of each product.

### Data Safety

Local persistence, predictable file structures, backups, migrations, and recoverability are considered during development.

### Compatibility

Core versions and `.alek` application versions must declare and respect compatibility requirements.

### Performance Awareness

Desktop integration, animation, media, memory use, database access, and GPU cost are handled with practical performance limits in mind.

---

## Technology

Technologies used across Ałek’ryŧhæ Core and `.alek` applications may include:

* C#
* .NET
* Microsoft Edge WebView2
* React
* TypeScript
* JavaScript
* HTML
* CSS
* SQLite
* JSON
* Windows desktop APIs
* Local media services
* Local file services
* Custom `.alek` package services

Not every `.alek` application uses every technology listed above.

Some technologies may be implemented directly by the Core and exposed to applications through approved runtime services.

---

## Repository Structure

The Core repository may follow a structure such as:

```text
Alekrythae-Core/
├── src/
│   ├── runtime/
│   ├── application-host/
│   ├── package-loader/
│   ├── storage/
│   ├── media/
│   ├── security/
│   └── platform/
├── resources/
├── docs/
├── scripts/
├── tests/
├── README.md
├── LICENSE.md
└── VERSION
```

A `.alek` application repository may follow a structure such as:

```text
Application/
├── application/
│   ├── manifest/
│   ├── interface/
│   ├── logic/
│   ├── data/
│   └── resources/
├── docs/
├── scripts/
├── tests/
├── README.md
├── LICENSE.md
├── VERSION
└── Application.alek
```

The exact development structure may vary according to the needs of the application.

The published `.alek` package does not need to expose the same directory structure used during development.

---

## Releases

Ałek’ryŧhæ Core and `.alek` applications are versioned separately.

Core releases may include:

* Windows runtime builds
* Portable Core packages
* Installers
* Runtime resources
* Documentation
* Changelogs
* Migration tools
* Integrity hashes

Application releases may include:

* `.alek` application packages
* Application documentation
* Changelogs
* Compatibility information
* Optional resource packages
* Integrity hashes

A `.alek` application release should clearly state:

* Its application version
* Its minimum supported Core version
* Its tested Core version
* Any known compatibility limitations
* Any required migration instructions

Users should download official builds and `.alek` packages from the relevant project’s **Releases** section rather than downloading repository source archives.

A source archive is not necessarily a ready-to-run `.alek` application package.

---

## Installation and Use

The general installation model is:

1. Install or obtain Ałek’ryŧhæ Core.
2. Download a compatible `.alek` application.
3. Open the `.alek` application through Ałek’ryŧhæ Core.
4. Allow the Core to validate and prepare the application.
5. Store application data in the location assigned to that application.

A `.alek` application should not require the user to install an unrelated standalone copy of the shared runtime.

Applications requiring a newer Core version should report the compatibility requirement clearly rather than failing silently.

---

## Compatibility

Core compatibility is part of the `.alek` application model.

Applications may define:

* Minimum Core version
* Maximum tested Core version
* Required Core capabilities
* Required runtime services
* Package format version
* Data schema version
* Migration version

The Core may reject, warn about, or restrict an application package that is:

* Damaged
* Incomplete
* Incompatible
* Modified without authorization
* Missing required metadata
* Using unsupported runtime capabilities
* Failing validation

Compatibility checks are intended to protect user data, application integrity, and runtime stability.

---

## Data and Storage

Ałek’ryŧhæ applications are designed around local and application-specific data storage.

Depending on the application, data may include:

* SQLite databases
* Local project files
* User-imported images
* User-imported audio
* Application settings
* Cache files
* Backup files
* Exported documents
* JSON configuration or exchange files
* Application-specific resources

The Core may provide shared storage services, but each application remains responsible for defining its own data structures and application-level rules.

User-created content should remain separate from the original `.alek` application package whenever practical.

Updating an application should not overwrite user-created projects or data.

---

## Security

Ałek’ryŧhæ Core may perform validation and security checks before opening a `.alek` application.

Security-related systems may include:

* Package integrity validation
* Manifest validation
* Compatibility checks
* Restricted runtime capabilities
* Application-specific storage separation
* Resource path validation
* Permission controls
* Update verification
* Recovery and backup support

A `.alek` application must not bypass Core security controls or access capabilities that have not been intentionally provided to it.

Users should obtain Core builds and `.alek` applications only from official sources.

---

## Documentation

Project-specific information is maintained inside the relevant repository or release package.

Depending on the Core or application, documentation may include:

* Installation instructions
* Core usage instructions
* Application manuals
* Keyboard shortcuts
* Data structure notes
* `.alek` package specifications
* Compatibility information
* Build instructions
* Security information
* Migration instructions
* Changelogs
* Language-specific guides

---

## License

Ałek’ryŧhæ Core, `.alek` applications, application packages, source code, binaries, resources, documentation, and associated materials are proprietary and source-available where expressly published.

They are licensed under the:

**TheDEvorger Universal Proprietary Software License Version 1.3**

They are not open-source software, free software, or public-domain material.

Personal and non-commercial use is permitted only within the limits stated in the applicable `LICENSE.md` file.

Unless separately authorized in writing, the following are prohibited:

* Commercial use
* Professional use
* Organizational use
* Production use
* Redistribution
* Rehosting
* Relicensing
* Unauthorized derivative distribution
* Unauthorized modified distributions
* Creation of unofficial Core builds
* Creation of unofficial `.alek` application loaders
* Creation of competing or substitute runtime systems through copied protected material
* Unauthorized conversion of `.alek` applications into standalone products
* AI or machine-learning training
* Dataset creation
* Automated extraction
* Unauthorized hosting or service deployment

Third-party materials remain governed by their own licenses.

The applicable `LICENSE.md` file controls where this summary differs from the complete license text.

---

## Official Distribution

Official Ałek’ryŧhæ materials may include:

* Ałek’ryŧhæ Core releases
* `.alek` application packages
* Documentation
* Changelogs
* Update packages
* Integrity hashes
* Application resources
* Migration tools

Unofficial mirrors, modified packages, converted applications, repackaged Core builds, and third-party download sources are not authorized unless expressly approved in writing.

---

## Maintainer

Developed and maintained under the **TheDEvorger** identity.

Licensing and legal contact:

**[TheDEvorger.alekrythae.dev@gmail.com](mailto:TheDEvorger.alekrythae.dev@gmail.com)**

---

> **One Core. Many `.alek` applications. One evolving software ecosystem.**
