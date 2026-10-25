# Awesome-Digital-Content-Provenance
# Awesome-Digital-Content-Provenance

# Top Digital Content Provenance
**Curated List of SaaS Products & Open-Source GitHub Projects**

*Focused on Content Authenticity, C2PA, Provenance Tracking, Watermarking, Deepfake Detection & Media Verification*

**Last updated: October 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Digital Content Provenance**. These tools help creators, platforms, and consumers establish, attach, verify, and inspect the origin and history of digital media (images, video, audio, and documents), especially in the era of generative AI.

**Examples** include Adobe Content Authenticity, Truepic, Attestiv, Numbers Protocol, Sensity AI, Reality Defender, GetReal Security, Hive AI, Optic, and C2PA Verify (the category leaders).

**Open-source emphasis**: Content provenance has a strong open foundation thanks to the **C2PA** standard and the **Content Authenticity Initiative (CAI)**. Official open-source SDKs (**c2pa-rs**, **c2patool**, language bindings), watermarking tools like **TrustMark**, and community verifiers enable transparent, standards-based provenance. This section is heavily expanded.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms
- **[Adobe Content Authenticity / Content Credentials](https://contentauthenticity.org/)**  
  Adobe-led initiative and tooling for attaching and verifying Content Credentials (C2PA) across Creative Cloud applications and the wider ecosystem.

- **[Truepic](https://truepic.com/)**  
  Platform focused on authenticated capture, secure provenance, and verification of photos and videos for trust and compliance use cases.

- **[Attestiv](https://attestiv.com/)**  
  Digital media integrity and provenance platform offering authentication, verification, and fraud detection for visual content.

- **[Numbers Protocol](https://www.numbersprotocol.io/)**  
  Decentralized infrastructure for digital media provenance using blockchain and open standards to create verifiable content history.

- **[Sensity AI](https://sensity.ai/)**  
  AI-powered platform specializing in deepfake detection, synthetic media identification, and content authenticity analysis.

- **[Reality Defender](https://www.realitydefender.com/)**  
  Enterprise deepfake and synthetic media detection platform supporting multiple modalities (image, video, audio, text).

- **[GetReal Security](https://www.getrealsecurity.com/)**  
  Security-focused solution for detecting manipulated and synthetic media with provenance and forensic capabilities.

- **[Hive AI](https://thehive.ai/)**  
  AI moderation and detection platform that includes tools for identifying AI-generated and manipulated content.

- **[Optic](https://www.optic.com/)** (and similar verification services)  
  Tools and services focused on visual content authenticity and provenance verification.

- **[C2PA Verify (contentcredentials.org)](https://contentcredentials.org/verify)**  
  Official web-based verifier for inspecting Content Credentials and C2PA manifests attached to media files.

## Open-Source GitHub Projects
- **[c2pa-rs](https://github.com/contentauth/c2pa-rs)**  
  Official Rust SDK and reference implementation for the C2PA (Coalition for Content Provenance and Authenticity) specification. Core library used by most C2PA tooling.

- **[c2patool](https://github.com/contentauth/c2patool)**  
  Official command-line tool for reading, validating, creating, and embedding C2PA manifests into media files. Essential for developers and forensic workflows.

- **[c2pa-python](https://github.com/contentauth/c2pa-python)**  
  Official Python bindings for the c2pa-rs library, enabling easy integration of Content Credentials into Python applications and pipelines.

- **[c2pa-js](https://github.com/contentauth/c2pa-js)**  
  JavaScript/TypeScript libraries for reading and working with C2PA manifests in browsers and Node.js environments.

- **[c2pa-cpp](https://github.com/contentauth/c2pa-cpp)**  
  Official C++ bindings for C2PA, useful for native applications and high-performance environments.

- **[TrustMark](https://github.com/adobe/trustmark)**  
  Open-source watermarking implementation for durable Content Credentials. Supports encoding, decoding, and removing invisible watermarks that can link back to C2PA manifests.

- **[Content Authenticity Initiative (contentauth) organization](https://github.com/contentauth)**  
  Central GitHub organization hosting the full suite of official open-source C2PA SDKs, tools, mobile libraries (Swift, Android), documentation, and security testing utilities.

- **[provcheck](https://provcheck.ai/)**  
  Offline, open-source C2PA Content Credentials verifier that checks cryptographic signatures, identity attestations, and neural watermarks without uploading files.

- **[Watermark (local-first workbench)](https://github.com/kylosarc/watermark)**  
  Local-first provenance and forensic workbench for inspecting C2PA Content Credentials, metadata, and watermarks entirely in the browser.

- **[Numbers Protocol open components](https://github.com/numbersprotocol)**  
  Open-source elements and tools related to the Numbers Protocol decentralized provenance network.

### Additional Strong Open-Source Options
- Core C2PA stack: **c2pa-rs**, **c2patool**, language bindings (Python, JS, C++, Swift, Android).
- Watermarking & soft bindings: **TrustMark**.
- Verification & forensics: **provcheck**, community workbenches.
- Accepting that commercial platforms (Adobe Content Authenticity, Truepic, Reality Defender, Sensity, Hive, etc.) still lead in end-to-end capture solutions, large-scale detection models, enterprise support, and polished user experiences.

**Frameworks for building custom systems**:  
Use the official **c2pa-rs** + **c2patool** stack to create and verify Content Credentials → add **TrustMark** for durable watermarking → integrate language bindings into your applications → optionally combine with decentralized registries (e.g. Numbers Protocol). Ideal for platforms, publishers, and developers who want standards-based, transparent, and interoperable content provenance.

## How to Contribute
1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer
- This is a **community-curated** list — not exhaustive and not an endorsement.
- Content provenance and authenticity technologies are evolving rapidly. Cryptographic verification, watermark robustness, and detection accuracy have limitations. Always combine technical signals with human judgment and additional context. This list is not legal, forensic, or security advice.

---
**Made for creators, journalists, platform engineers, researchers, and open-source advocates.**

Let's keep digital content provenance transparent, standards-based, and verifiable.
