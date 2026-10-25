# Awesome Digital Content Provenance [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of top SaaS products, enterprise APIs, and open-source tools for **Digital Content Provenance**, **C2PA Content Credentials**, **Deepfake Detection**, **Digital Watermarking**, and **Media Authenticity Verification**.

---

## Overview

In the era of generative AI, synthetic media, and deepfakes, establishing the origin, edit history, and authenticity of digital assets has become mission-critical for creators, publishers, journalism organizations, and enterprise platforms. 

This repository tracks the leading **commercial SaaS platforms** and **open-source developer tools** designed to attach, verify, track, and inspect cryptographic provenance across images, video, audio, and documents.

### Key Categories & Keywords
- **C2PA Standard & Manifests**: Standards-based metadata binding led by the [Coalition for Content Provenance and Authenticity](https://c2pa.org/).
- **Content Credentials**: Cryptographic seals and provenance manifests pioneered by the [Content Authenticity Initiative (CAI)](https://contentauthenticity.org/).
- **Synthetic Media & Deepfake Detection**: Multi-modal AI models analyzing pixel/spectral artifacts.
- **Durable & Invisible Watermarking**: Soft-binding watermarks linking media back to tamper-evident provenance data.
- **Decentralized Media Verification**: Blockchain and distributed ledger tracking for immutable media timestamps and ownership.

---

## Table of Contents

- [SaaS & Hosted Platforms](#saas--hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [Architecture & Implementation Blueprint](#architecture--implementation-blueprint)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

---

## SaaS & Hosted Platforms

The following table provides an overview of commercial platforms offering managed infrastructure, enterprise detection APIs, and capture verification.

| Product / Platform | Primary Focus | Pricing Model | Free Tier & Limits | Website |
| :--- | :--- | :--- | :--- | :--- |
| **Adobe Content Authenticity / Content Credentials** | C2PA creation, inspection, and identity binding across Creative Cloud | Included in Adobe CC / Freemium web utilities | **Free**: Web inspect tool and Chrome extension are free; included at no extra cost in Adobe Creative Cloud and Firefly | [contentauthenticity.org](https://contentauthenticity.org/) |
| **C2PA Verify** | Official reference web manifest verifier | Free / Open Public Utility | **Free**: Unlimited public manifest validation and asset inspection | [contentcredentials.org/verify](https://contentcredentials.org/verify) |
| **Reality Defender** | Multi-modal enterprise deepfake & synthetic media detection (audio, video, image, text) | Subscription / Usage-based (starts ~$399/mo) | **Free Trial**: Available upon request / trial tier typically limited to ~50 scans/month | [realitydefender.com](https://www.realitydefender.com/) |
| **Hive AI** | Automated AI content moderation & AI-generated media classification APIs | Usage-based API pricing (~$6 / 1k images; ~$6 / 1k video frames) | **Free Credits**: Free developer trial credits upon initial API signup | [thehive.ai](https://thehive.ai/) |
| **Truepic** | Hardware-secured media capture, camera provenance, and visual inspection | B2B / Volume-based enterprise pricing (starts ~$1,000/mo) | **No Free Tier**: Demo and pilot test inspections available on request | [truepic.com](https://truepic.com/) |
| **Attestiv** | Document & visual media fraud prevention with forensic tamper detection | Enterprise custom quotes (based on annual document/claim volume) | **No Free Tier**: Product demo and customized ROI analysis available | [attestiv.com](https://attestiv.com/) |
| **Sensity AI** | Deepfake monitoring, synthetic media threat intelligence & verification APIs | Enterprise custom quotation (entry tiers from ~$29/mo) | **No Free Tier**: Demo and customized API sandbox trials available on request | [sensity.ai](https://sensity.ai/) |
| **Optic (AI or Not)** | AI-generated image/audio detection and digital asset provenance verification | Enterprise API & tiered web scan subscriptions | **Freemium**: Limited free web checks on *AI or Not*; custom quotes for high-volume API access | [optic.xyz](https://optic.xyz/) |
| **Numbers Protocol** | Decentralized media provenance network and blockchain asset verification | Token-based transaction gas / Enterprise API subscription | **Freemium Developer Tier**: Free developer API credits with paid upgrades and $NUM utility tokens | [numbersprotocol.io](https://www.numbersprotocol.io/) |
| **GetReal Security** | Enterprise synthetic media detection and forensic provenance analysis | Enterprise custom quotes | **No Free Tier**: Private demonstrations available | [getrealsecurity.com](https://www.getrealsecurity.com/) |

---

## Open-Source GitHub Projects

Official implementations, SDKs, and developer utilities for building standards-compliant C2PA and digital provenance pipelines.

| Project | Language / Ecosystem | Description | Repository |
| :--- | :--- | :--- | :--- |
| **c2pa-rs** | Rust | Official C2PA reference implementation. High-performance library for reading, validating, and generating C2PA manifests. | [`contentauth/c2pa-rs`](https://github.com/contentauth/c2pa-rs) |
| **c2patool** | Rust / CLI | Official command-line utility to inspect, create, and embed C2PA manifests into media files. Essential for CI/CD pipelines. | [`contentauth/c2patool`](https://github.com/contentauth/c2patool) |
| **c2pa-python** | Python | Official Python bindings for `c2pa-rs`, enabling direct integration into ML/AI pipelines, FastAPI services, and scripts. | [`contentauth/c2pa-python`](https://github.com/contentauth/c2pa-python) |
| **c2pa-js** | JavaScript / TypeScript | Client-side and Node.js SDKs for reading and displaying Content Credentials directly in browsers. | [`contentauth/c2pa-js`](https://github.com/contentauth/c2pa-js) |
| **c2pa-cpp** | C++ | C++ wrapper around `c2pa-rs` designed for embedded systems, camera firmware, and native desktop applications. | [`contentauth/c2pa-cpp`](https://github.com/contentauth/c2pa-cpp) |
| **TrustMark** | Python | Durable, invisible watermarking library designed to bind media assets to C2PA manifests even through re-compression and cropping. | [`adobe/trustmark`](https://github.com/adobe/trustmark) |
| **provcheck** | TypeScript / Web | Client-side, privacy-first offline C2PA Content Credentials verifier without uploading media to third-party servers. | [`provcheck`](https://provcheck.ai/) |
| **Watermark** | TypeScript / WebAssembly | Local-first browser workbench for forensic metadata inspection, C2PA manifest extraction, and neural watermark analysis. | [`kylosarc/watermark`](https://github.com/kylosarc/watermark) |
| **Numbers Protocol Suite** | Python / JS | Open-source tools, capture libraries, and smart contracts for decentralized asset history and provenance anchoring. | [`numbersprotocol`](https://github.com/numbersprotocol) |
| **Content Authenticity Org** | Multi-language | Complete ecosystem repository containing mobile libraries (iOS/Swift, Android), documentation, and test vectors. | [`contentauth`](https://github.com/contentauth) |

---

## Architecture & Implementation Blueprint

When engineering an end-to-end digital content provenance pipeline:

1. **Ingest & Capture**: Secure hardware-level capture (e.g. Truepic lens SDK) or cryptographic manifest generation using [`c2pa-rs`](https://github.com/contentauth/c2pa-rs) / [`c2pa-python`](https://github.com/contentauth/c2pa-python).
2. **Resilience & Durable Binding**: Embed soft bindings using invisible watermarking like [`adobe/trustmark`](https://github.com/adobe/trustmark) so metadata survives social media re-encoding and stripping.
3. **Verification & Forensics**: Inspect incoming files in-browser via [`c2pa-js`](https://github.com/contentauth/c2pa-js) or through privacy-preserving tools like [`provcheck`](https://provcheck.ai/).
4. **Threat Detection**: Route unverified or suspicious media through deepfake and synthetic detection engines such as [Reality Defender](https://www.realitydefender.com/) or [Hive AI](https://thehive.ai/).

---

## How to Contribute

Contributions are welcome! Please follow these guidelines:

1. Fork the repository.
2. Ensure entries are factual, active, and relevant to digital content authenticity, C2PA, or deepfake detection.
3. If adding a SaaS product, please include details on pricing structure and free tier availability.
4. Submit a Pull Request with a clear description of the project.

---

## Disclaimer

This repository is a community-curated directory for informational and educational purposes. Inclusion does not imply endorsement. Content authenticity verification and synthetic media detection models are probabilistic; always combine technical signals with contextual analysis and human judgment.
