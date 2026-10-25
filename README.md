# EchoTrap: Secure AI Gateway and Interception Analysis

AI chat apps send user prompts to remote APIs, and that traffic is often trusted blindly. EchoTrap shows how it can be intercepted with **DNS spoofing + a man-in-the-middle proxy**, then defends it with a **mutual-TLS (mTLS) API gateway**. Everything runs safely on a single machine.

## What It Demonstrates

- **The attack:** prompts are stolen and replies are forged.
- **The defense:** the same attack is refused at the TLS handshake, before any data is exchanged.

## Components

- Vulnerable chat web app
- Local interception proxy
- DNS spoofing simulation (via the system hosts file)
- Private certificate authority
- mTLS gateway

## Goals

- Demonstrate MITM and DNS spoofing on AI API traffic in a controlled environment.
- Show how unauthenticated transport exposes prompts and allows forged responses.
- Build a secure gateway that enforces mTLS.
- Prove the hardened system blocks the attack at the handshake.
- Document the architecture, threat model, and defense.

## Scope

Local, single-machine demo focused on the transport-layer weakness and its mTLS fix. Out of scope: production certificate management (revocation, hardware key storage) and network attacks beyond the modeled DNS redirection.

## Web Interface

Three screens:

1. **Secured chat:** communicates over mTLS.
2. **Unprotected chat:** shows a prompt intercepted and a reply tampered with.
3. **Attack blocked:** shown when the gateway refuses an untrusted server.

## Team (Group 7)

| Name | Roll No. |
|---|---|
| Muhammad Mazan | 23L-3022 |
| Vania Ejaz | 23L-3037 |
| Ayka Imran | 23L-3051 |

**Instructor:** Sarah Abid Khan
FAST-NUCES (National University of Computer and Emerging Sciences), Lahore

