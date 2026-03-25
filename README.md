<!-- BlackRoad SEO Enhanced -->

# skills sdk

> Part of **[BlackRoad OS](https://blackroad.io)** — Sovereign Computing for Everyone

[![BlackRoad OS](https://img.shields.io/badge/BlackRoad-OS-ff1d6c?style=for-the-badge)](https://blackroad.io)
[![BlackRoad OS](https://img.shields.io/badge/Org-BlackRoad-OS-2979ff?style=for-the-badge)](https://github.com/BlackRoad-OS)
[![License](https://img.shields.io/badge/License-Proprietary-f5a623?style=for-the-badge)](LICENSE)

**skills sdk** is part of the **BlackRoad OS** ecosystem — a sovereign, distributed operating system built on edge computing, local AI, and mesh networking by **BlackRoad OS, Inc.**

## About BlackRoad OS

BlackRoad OS is a sovereign computing platform that runs AI locally on your own hardware. No cloud dependencies. No API keys. No surveillance. Built by [BlackRoad OS, Inc.](https://github.com/BlackRoad-OS-Inc), a Delaware C-Corp founded in 2025.

### Key Features
- **Local AI** — Run LLMs on Raspberry Pi, Hailo-8, and commodity hardware
- **Mesh Networking** — WireGuard VPN, NATS pub/sub, peer-to-peer communication
- **Edge Computing** — 52 TOPS of AI acceleration across a Pi fleet
- **Self-Hosted Everything** — Git, DNS, storage, CI/CD, chat — all sovereign
- **Zero Cloud Dependencies** — Your data stays on your hardware

### The BlackRoad Ecosystem
| Organization | Focus |
|---|---|
| [BlackRoad OS](https://github.com/BlackRoad-OS) | Core platform and applications |
| [BlackRoad OS, Inc.](https://github.com/BlackRoad-OS-Inc) | Corporate and enterprise |
| [BlackRoad AI](https://github.com/BlackRoad-AI) | Artificial intelligence and ML |
| [BlackRoad Hardware](https://github.com/BlackRoad-Hardware) | Edge hardware and IoT |
| [BlackRoad Security](https://github.com/BlackRoad-Security) | Cybersecurity and auditing |
| [BlackRoad Quantum](https://github.com/BlackRoad-Quantum) | Quantum computing research |
| [BlackRoad Agents](https://github.com/BlackRoad-Agents) | Autonomous AI agents |
| [BlackRoad Network](https://github.com/BlackRoad-Network) | Mesh and distributed networking |
| [BlackRoad Education](https://github.com/BlackRoad-Education) | Learning and tutoring platforms |
| [BlackRoad Labs](https://github.com/BlackRoad-Labs) | Research and experiments |
| [BlackRoad Cloud](https://github.com/BlackRoad-Cloud) | Self-hosted cloud infrastructure |
| [BlackRoad Forge](https://github.com/BlackRoad-Forge) | Developer tools and utilities |

### Links
- **Website**: [blackroad.io](https://blackroad.io)
- **Documentation**: [docs.blackroad.io](https://docs.blackroad.io)
- **Chat**: [chat.blackroad.io](https://chat.blackroad.io)
- **Search**: [search.blackroad.io](https://search.blackroad.io)

---


Official SDK for BlackRoad OS Tools - enabling AI agents with memory, reasoning, and coordination capabilities.

## Installation

```bash
npm install @blackroad/skills-sdk
```

## Quick Start

```typescript
import { createSDK } from '@blackroad/skills-sdk';

const sdk = createSDK({
  agentId: 'agent-0001'
});

// Store a memory
const hash = await sdk.memory.remember('The user prefers dark mode');

// Evaluate a claim for contradictions
const evaluation = await sdk.reasoning.evaluate('The sky is blue');

// Delegate a task to another agent
const taskId = await sdk.coordination.delegate({
  taskType: 'analysis',
  description: 'Analyze quarterly sales data',
  requiredCapabilities: ['analytics', 'data_processing']
});
```

## Features

### Memory (PS-SHA∞ Persistence)
- `memory.remember(content)` - Store a fact
- `memory.observe(content)` - Store an observation
- `memory.infer(content)` - Store an inference
- `memory.commit(content)` - Store a commitment
- `memory.search(query)` - Search memories
- `memory.invalidate(hash)` - Mark memory as invalid

### Reasoning (Trinary Logic)
- `reasoning.evaluate(claim)` - Check for contradictions
- `reasoning.assertTrue(claim)` - Assert claim as true (1)
- `reasoning.assertFalse(claim)` - Assert claim as false (-1)
- `reasoning.assertUnknown(claim)` - Mark claim as unknown (0)
- `reasoning.quarantine(claimIds)` - Quarantine contradicting claims
- `reasoning.resolve(quarantineId)` - Resolve a quarantine

### Coordination (Event Bus)
- `coordination.publish(topic, type, payload)` - Publish event
- `coordination.subscribe(topic)` - Get events from topic
- `coordination.delegate(task)` - Delegate task to agent
- `coordination.complete(taskId, status)` - Complete a task
- `coordination.broadcast(message)` - Broadcast to all agents

### Agent Registry
- `agents.list(options)` - List agents with filtering
- `agents.get(agentId)` - Get specific agent
- `agents.findByCapabilities(caps)` - Find capable agents
- `agents.getCapabilities()` - List all capabilities

## High-Level Methods

```typescript
// Think through something (auto-handles contradictions)
await sdk.think('The user might prefer light mode after all');

// Learn a fact with confidence
await sdk.learn('User timezone is CST', 0.95);

// Ask another agent for help
await sdk.ask('How do I format dates in French?', ['localization']);

// Collaborate with multiple agent types
await sdk.collaborate('Build a report', ['analyst', 'writer', 'reviewer']);
```

## Trinary Logic

BlackRoad uses trinary logic for truth states:
- `1` = True (verified fact)
- `0` = Unknown (uncertain, needs verification)
- `-1` = False (verified false)

This enables sophisticated contradiction handling and epistemic reasoning.

## License

MIT - BlackRoad OS
