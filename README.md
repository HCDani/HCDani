# Hock Dániel

Software engineer, BEng in Software Technology from VIA University College. Based in
Horsens, Denmark.

I work closest to the machine: embedded firmware, backends, data pipelines, and the
infrastructure that holds them together. I've built the web and mobile front ends for
most of my projects too, and app development is something I'd happily do more of.

**I'm looking for a graduate software engineering role** in Denmark or elsewhere in
Scandinavia, ideally in embedded/IoT, backend or platform work.

## What I've built

**[GHA](https://github.com/HCDani/GHA)** — my bachelor project, and the thing I'd point
at first. Sensor nodes publish readings over MQTT; Logstash validates and normalises
them into OpenSearch, routing anything malformed to a separate error index instead of
dropping it; a React frontend shows each user their greenhouses with embedded Grafana
panels, behind Keycloak SSO and an nginx reverse proxy. Ten containers under Docker
Compose on a private server. Two CI workflows gate it, one of which builds the whole
stack and runs integration tests against the live pipeline. Built with one teammate,
where I was tech lead.

**[SEP4IOT](https://github.com/HCDani/SEP4IOT)** — telemetry firmware in C on an
Arduino Mega 2560. It reads temperature, humidity and light, encrypts the telemetry
with AES-128, validates it with CRC16, and exchanges it with a cloud backend over WiFi
and HTTP, with a cooperative RTOS scheduling the tasks and timers. Unit tested with
Unity. I was **tech lead of a seven-person team** on this project and wrote the
firmware myself. It was also a greenhouse system — I ended up solving the same problem
again eighteen months later for my bachelor with a completely different architecture,
which taught me more than either project did alone.

**[HWP1](https://github.com/HCDani/HWP1)** — hardware-oriented programming in C:
drivers for sensors, a display and a servo, written against the datasheets.

**[DeliriumApp](https://github.com/HCDani/DeliriumApp)** — an internship at VIA
University College building an offline-capable reference app for nurses caring for
delirium patients, with a real client. I was tech lead. I built the WordPress
content platform and the JavaScript behind the CAM and B-CAM screening tools, and
set up the initial React
Native structure before handing the mobile work to a teammate. The prototype was
presented at the International Council of Nurses 2025 conference, where I supported the
practitioner leading the session.

**[ViaEventAssociation](https://github.com/HCDani/ViaEventAssociation)** — a solo C#
event-handling system for organising events on campus, built with domain-driven design
on an onion architecture, using the builder, REPR and unit-of-work patterns, with a
unit test suite behind it.

**[ChatRMI](https://github.com/HCDani/ChatRMI)** — a JavaFX chat application where the
client reaches the server through a single interface with two implementations: Java RMI
and raw TCP sockets. The server runs both at once and pushes new messages to every
client over UDP multicast, so it never needs to know which transport a given client
arrived on.

**[Assignment4-Kingdom](https://github.com/HCDani/Assignment4-Kingdom)** — a
multithreaded Java simulation of a treasury: producer–consumer between the miner and
the transporters over a monitor, and readers–writers on the treasure room with a
`ReentrantReadWriteLock`.

## Tools I've worked with

**Languages** — C (embedded), C#/.NET, Java, Python, JavaScript, TypeScript

**Embedded** — PlatformIO, RTOS scheduling, interrupt-driven I/O, UART, WiFi modules,
CRC and AES validation, on-board testing

**Infrastructure** — Docker and Docker Compose, nginx, GitHub Actions, Azure, Keycloak

**Data** — MQTT (Mosquitto), Logstash, OpenSearch, Grafana, PostgreSQL, SQLite,
PocketBase

**Testing** — unit, integration and on-board; Jest, pytest, JUnit

**Ways of working** — Scrum, Kanban, UP, TDD, DDD

## How I work with AI

I use coding agents daily and have specific opinions about where they help and where
they don't. The short version: they're fast, they're confidently wrong about anything
they can't see — your database schema, your runtime, a niche query language — and the
job is knowing which kind of failure you're looking at. I'm happy to go into detail in
an interview.

## Contact

- Email: hockdanield@gmail.com
- LinkedIn: [hock-daniel](https://www.linkedin.com/in/hock-daniel/)
- Languages: Hungarian (native), English (professional working proficiency), Danish
  (basic)
