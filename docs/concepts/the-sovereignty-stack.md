---
sidebar_position: 39
title: "The Sovereignty Stack"
---

# The Sovereignty Stack

*Own your future. Every layer of your digital life has a default version controlled by someone who is not you. Here is the full map.*

---

## You Should Own Your Own Super Intelligence

Start with the simple version: you should own your AI. Not rent it. Not subscribe to it. Own it.

You should not be dependent on OpenAI. Or Anthropic. Or Google. Or Meta. Or any single provider for the intelligence that powers your thinking, your business, your life. Because the moment you are dependent, you are controlled. They set the price. They set the policy. They decide what you can and cannot do with the tool that has become central to how you operate.

But owning your AI is not just about the model. It is about every layer of the stack that enables your AI to function. The hardware it runs on. The network it communicates through. The operating system it sits inside. The data it draws from. The identity you use to access it. Every layer has a default version controlled by someone who is not you.

That is what the sovereignty stack maps. Every layer. Every dependency. Every point of control.

## Assume Adversarial Intent

The default version of every layer in your digital stack is controlled by entities whose interests diverge from yours. ISPs log your traffic. Operating systems phone home. AI platforms train on your prompts. Cloud providers hold your data hostage behind their login. NVIDIA has a monopoly on GPU compute through CUDA, making it so that if you want to run any serious AI workload, you are dependent on their proprietary ecosystem.

This is not paranoia. It is the business model. It goes deep. Satellite internet (Starlink) is controlled by one person. Chip fabrication is controlled by a handful of fabs. DNS resolution, CDN termination, firmware, device manufacturing. Every layer has an entity that can shut you down, surveil you, or change the terms on you.

The sovereignty stack maps every layer of your digital life from silicon to content, identifies who controls the default, and shows what the sovereign alternative looks like. Not every layer can be fully sovereign today. But you should know where you are exposed. To own your own super intelligence and own your own future, you have to understand how deep it goes.

## The Stack

### Layer 0: Silicon

**Default:** Intel and AMD chips with opaque architectures. Intel Management Engine runs a separate computer inside your CPU with full memory and network access. You cannot inspect what it does. You cannot turn it off.

**Sovereign direction:** RISC-V, an open-source instruction set architecture, is gaining ground. But even open silicon designs get fabricated at TSMC or Samsung. You can audit the design, not the die.

**If compromised:** Game over. Hardware backdoors survive everything. OS reinstalls, encryption, firmware reflashes. This is the nuclear option for a state-level adversary.

### Layer 1: Firmware

**Default:** Proprietary UEFI firmware. Intel ME and AMD PSP run below your OS with higher privilege. Closed source, always on, with independent network access.

**Sovereign direction:** Coreboot (open-source firmware). Available on System76 laptops, Purism Librem, some Framework and ThinkPad models. Libreboot goes further. ME Cleaner can partially neutralize Intel ME on some systems.

**If compromised:** Firmware-level malware persists across OS reinstalls. The attacker owns your machine before your OS even loads.

### Layer 2: Hardware

**Default:** Apple, Lenovo, Dell. All manufactured in China or Vietnam. Supply chain attacks are documented.

**Sovereign direction:** Purism Librem (made in California, coreboot, hardware kill switches). System76 (US-based, open firmware). Framework (modular, repairable, community coreboot). For phones: Google Pixel hardware running GrapheneOS is the best available option for a sovereign mobile device.

### Layer 3: Operating System

**Default:** Windows (telemetry, forced updates, Microsoft account required). macOS (closed source, Apple controls what runs). iOS/Android with Google Play Services (pervasive tracking).

**Sovereign direction:** Desktop Linux (Debian, Fedora, NixOS). Qubes OS for compartmentalized security. GrapheneOS for mobile (hardened Android, Pixel-only). Tails OS for high-risk situations (routes everything through Tor, leaves no trace).

**Difficulty:** Medium. Linux is mature. GrapheneOS is a weekend project. The barrier is app compatibility, not technical capability.

### Layer 4: Networking

**Default:** Your ISP sees all unencrypted traffic. Your DNS provider sees every domain you visit. Cloudflare terminates TLS for a massive percentage of the web and sees all traffic in plaintext.

**Sovereign direction:**
- **DNS:** Self-hosted Pi-hole or AdGuard Home. Privacy DNS like Quad9 or DNS0 (Swiss/EU non-profits).
- **VPN:** Self-hosted WireGuard on a VPS. Or Mullvad (no-account, cash-payment).
- **Mesh:** Headscale (self-hosted Tailscale). Yggdrasil (encrypted overlay network).
- **ISP bypass:** There is no sovereign ISP. Starlink is a different dependency, not sovereignty. Encrypt everything that traverses the ISP.

### Layer 5: Data Storage

**Default:** Google Drive, iCloud, Dropbox. The provider holds the keys. Subject to government subpoenas, ToS changes, and account lockouts.

**Sovereign direction:** Nextcloud (self-hosted). Syncthing (peer-to-peer, no central server). Local NAS with encrypted drives. Restic or BorgBackup for encrypted backups. The rule: data encrypted on your device before it leaves.

### Layer 6: Identity

**Default:** "Sign in with Google." Your identity is a row in their database. They can disable it.

**Sovereign direction:** YubiKey hardware security keys (private key never leaves the device). Vaultwarden (self-hosted password manager). KeePassXC (fully local). Decentralized Identity (W3C DIDs) is maturing but not yet mainstream.

**If compromised:** Identity compromise cascades across every linked service. This is why hardware keys matter.

### Layer 7: Communication

**Default:** Gmail (Google reads your mail). iMessage (Apple holds keys for iCloud backup). Zoom (compliance with government requests).

**Sovereign direction:**
- **Email:** ProtonMail (E2E encrypted, Swiss). Tuta (encrypts subject lines too). Self-hosted email is technically possible but deliverability is a nightmare because Gmail and Microsoft control the email ecosystem.
- **Messaging:** Signal (E2E, open protocol). Matrix/Element (federated, self-hostable, used by the EU and the UN). SimpleX (no user IDs at all).
- **Video:** Jitsi Meet (open-source, self-hostable).

### Layer 8: AI / LLM

This layer did not exist five years ago. It is now one of the most critical.

**Default:** OpenAI, Anthropic, Google. Your prompts go to their servers. Your code, your strategy documents, your private thoughts, all processed on infrastructure you do not control. [The lock-in is coming](/docs/concepts/the-lock-in-is-coming). [Hyperscalers are the new record labels](#hyperscalers-are-the-new-record-labels).

**Sovereign direction:**
- **Models:** Local open-source models via Ollama. Llama 3.3, Mistral, DeepSeek, Qwen2. A Mac with 32GB RAM can run 70B parameter models. The gap with frontier models is closing.
- **Harness:** OpenCode (open-source, supports 75+ providers including local models). Aider, Continue.dev, Cline. The [MVJ architecture](/docs/playbooks/practitioner/minimum-viable-jarvis) is designed so your [context lake](/docs/concepts/context-lake) works with any harness.
- **Context:** Plain markdown files on your machine. Not chat history on someone else's server. This is the whole point of the context lake architecture.

**Difficulty:** Low to medium. Ollama on a Mac takes minutes. The tradeoff: local models are still behind frontier models for complex tasks. You are trading capability for control. For many use cases, the trade is worth it. For others, use cloud models with eyes open about what you are sending.

### Layer 9: Applications

**Default:** Notion, Google Docs, Stripe, YouTube. Each one is a dependency and a data siphon.

**Sovereign direction:**
- **Knowledge:** Obsidian (plain markdown, local-first). Anytype (P2P, zero-knowledge). AppFlowy (open-source Notion alternative).
- **Payments:** BTCPay Server (self-hosted, open-source). Lightning Network for near-instant payments.
- **Hosting:** Self-hosted on your own domain. ENS + IPFS for censorship resistance. Njalla for privacy-focused domain registration.
- **Content:** Self-hosted blog. PeerTube (federated video). Nostr (censorship-resistant social, your identity is your keypair).

### Layer 10: Analytics

**Default:** Google Analytics tracks you across the web. Windows telemetry phones home. Most apps include analytics SDKs that track every click.

**Sovereign direction:** Plausible or Umami (open-source, self-hostable, cookieless). Firefox + uBlock Origin for browsing. Disable telemetry in your OS.

## Hyperscalers Are the New Record Labels

In the music industry, a 360 deal means the label takes a cut of everything. They give you distribution and a check upfront. In return, they own your masters.

Every centralized AI platform is running the same play. They give you a powerful tool. In return, they get your context, your thinking, your strategic edge. Your prompts are your masters. If they live on someone else's servers, someone else owns them.

The [Soul Harness](/docs/concepts/the-soul-harness) framework makes the distinction: a predatory harness makes you dependent over time. A liberating harness makes you more capable and more independent over time. At every layer of the stack, choose liberating.

## The Minimum Viable Sovereign Stack

You cannot sovereign everything overnight. Here is the 80/20.

**Today (1-2 hours):**
- Firefox + uBlock Origin + DNS-over-HTTPS
- Signal for sensitive messaging
- YubiKey for critical accounts
- ProtonMail for sensitive email

**This week:**
- Obsidian for knowledge management
- Syncthing for file sync
- Ollama for local AI
- Pi-hole for network-level DNS

**This month:**
- GrapheneOS on a Pixel
- Linux on your primary machine (if on Windows)
- Self-hosted WireGuard VPN
- Restic for encrypted backups

**Ongoing:**
- Coreboot-compatible hardware
- Local-first AI harness for development
- Decentralized identity and hosting

## Vitalik's Proof of Concept

In April 2026, Vitalik Buterin [published his personal sovereign AI setup](https://vitalik.eth.limo/general/2026/04/02/secure_llms.html): local LLM inference on laptop GPUs, sandboxed agents, a messaging daemon that only allows send-to-self without human confirmation, a local `world_knowledge` folder (his version of a [context lake](/docs/concepts/context-lake)) to reduce reliance on internet searches, and a multi-layer defense approach for when you must use remote models.

Two ideas from his setup are worth highlighting:

**The human + LLM two-factor.** For any risky action (sending a message, moving funds, publishing content), require confirmation from both a human and an LLM. Humans fail sometimes (absent-minded, tricked). LLMs fail sometimes (jailbroken, hallucinating). The hope is they fail in different ways. Requiring both to agree before anything irreversible happens is much safer than trusting either alone. This extends our [permission surface](/docs/concepts/the-permission-surface) concept into a true two-factor model.

**Open-weights is not open-source.** Most "open" AI models give you the trained weights but not the training code, data, or process. You can run them locally, but you cannot fully audit what was trained into them. This means hidden behaviors (backdoors, biases, triggers) could exist in models you think are safe because they are "open." True sovereignty requires awareness of this gap.

Vitalik's vision aligns with ours: "AI can actually create a future with much stronger privacy and security... the more sophisticated software would live on the user's machine and be aligned with the user, instead of being aligned with a corporation intent on extracting attention and value." That is the sovereignty stack in one sentence.

## The Sovereignty Economy

An entire economy needs to be built around this stack. Sovereign hardware. Sovereign networking. Sovereign AI. Sovereign identity. Every layer is an opportunity for builders.

The [Applied AI Society](https://appliedaisociety.org) is training sovereign builders. People who understand the stack, can operate at every layer, and can help others achieve sovereignty. Anyone who wants a sovereign future should be part of this movement. We are training the builders of the sovereign future.

The default stack is designed to extract from you. The sovereign stack is designed to liberate you. Every layer you reclaim is a layer the adversary loses.

> **Own your silicon. Own your network. Own your data. Own your identity. Own your models. Own your harness. Own your content. Own your future.**

---

## Further Reading

- [The Lock-In Is Coming](/docs/concepts/the-lock-in-is-coming): Why vendor lock-in is structurally inevitable
- [The Soul Harness](/docs/concepts/the-soul-harness): Predatory vs. liberating systems
- [Context Lake](/docs/concepts/context-lake): Your sovereign knowledge base
- [Personal Jarvis](/docs/concepts/personal-jarvis): The sovereign AI system
- [Minimum Viable Infrastructure](/docs/concepts/minimum-viable-infrastructure): The baseline requirements to participate
- [Liberation Architecture](/docs/concepts/liberation-architecture): Building systems that free people
- [Harness Engineering](/docs/concepts/harness-engineering): Why the wrapper matters as much as the model
