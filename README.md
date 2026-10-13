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

**[ghanode_si917](https://github.com/HCDani/ghanode_si917)** — Wi-Fi sensor-node
firmware in C for the Silicon Labs SiWx917, on FreeRTOS (CMSIS-RTOS2 API), written after
the bachelor to feed GHA's pipeline. A sensor thread samples on a fixed period and queues
the readings; a network thread publishes them over MQTT and reconnects when Wi-Fi or the
broker drops, so readings taken during an outage are sent afterwards. It recovers from
both kinds of outage unattended, tested on the board by switching the broker and the
access points off, and the README walks through the bugs those tests turned up.

**[SEP4IOT](https://github.com/HCDani/SEP4IOT)** — telemetry firmware in C on an
Arduino Mega 2560. It reads temperature, humidity and light, encrypts the telemetry
with AES-128, validates it with CRC16, and exchanges it with a cloud backend over WiFi
and HTTP, with a cooperative RTOS scheduling the tasks and timers. Unit tested with
Unity. I was **tech lead and product owner of a seven-person team** on this project and wrote the
firmware myself. It was also a greenhouse system — I ended up solving the same problem
again eighteen months later for my bachelor with a completely different architecture,
which taught me more than either project did alone.

**[avr-thermostat-cpp](https://github.com/HCDani/avr-thermostat-cpp)** — a bare-metal
thermostat in C++ for the ATmega328P, written directly against the registers with no
Arduino framework and no heap. Every driver sits behind an interface with a hardware
implementation and a mock, so the same control logic runs on the target and in 87 host
tests. It drives a pump through a relay, keeps its setpoints in EEPROM, and fails safe
when the sensor lead breaks. It rebuilds a C assignment from my hardware-oriented
programming course ([HWP1](https://github.com/HCDani/HWP1)) with interfaces, mocks and CI.

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

**Languages** — C (embedded), C++, C#/.NET, Java, Python, JavaScript, TypeScript

**Embedded** — FreeRTOS (CMSIS-RTOS2 API), RTOS scheduling, PlatformIO, interrupt-driven
I/O, ADC, hardware PWM, UART, I2C, Wi-Fi modules, EEPROM, CRC and AES validation,
fixed-point arithmetic, host-and-target testing

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
