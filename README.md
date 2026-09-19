<p align="center">
  <img src="assets/avatar.jpg" width="140" height="140" alt="AIEN Sovereign Intelligence" style="border-radius: 50%; border: 2px solid #f59e0b;">
</p>

# spark-dream

[![Crates.io](https://img.shields.io/badge/crates.io-v0.1.0-orange.svg)](https://github.com/aien-dev/spark-dream)
[![License: SRCL-1.0](https://img.shields.io/badge/License-SRCL--1.0-blue.svg)](LICENSE)
[![Build](https://img.shields.io/badge/build-passing-brightgreen.svg)](https://github.com/aien-dev/spark-dream)

Native Rust Dynamic Dream Cycle Engine for autonomous session memory consolidation on SparkOS.

## Overview

`spark-dream` is an autonomous background memory consolidation daemon written in 100% native Rust. It monitors operator idle states (>15 minutes) and GPU compute activity, safely processing parked notes and session turns into persistent knowledge inside Spark Cortex Memory.

## Key Features

- **Native Hardware Telemetry**: Directly queries GPU utilization via NVML / lightweight child probes with sub-millisecond execution, avoiding heavy interpreter runtimes.
- **Immediate Interruption**: Instantly yields execution when GPU load spikes or interactive operator input is detected.
- **Cortex Vector Integration**: Automatically commits verified operational facts and discoveries to `cortex-rs` (`127.0.0.1:18080`) with ONNX bi-encoder vector embeddings.
- **Sovereign Invariants**: Adheres strictly to the Unslop standard (zero em/en dashes, zero AI buzzwords) and hardware TPM vault key management.

## Installation & Usage

```bash
# Build release binary
cargo build --release

# Run an immediate dream consolidation cycle
./target/release/spark-dream cycle

# Run as background daemon
./target/release/spark-dream --daemon --idle-threshold 900
```

## License and Governance

Licensed under the **Sovereign Resource Commons License 1.0 (SRCL-1.0)** (Apache-2.0 WITH LLVM-exception).
Architected by AIEN (Autonomous Cognitive Architecture operating on the Atlas Framework) and sovereign ecosystem contributors. See [LICENSE](LICENSE) for full legal terms and copyright notices.

All downstream distributions, derivative works, and commercial deployments are governed exclusively by the terms of [LICENSE](LICENSE). [CONSTITUTION.md](CONSTITUTION.md) defines the internal architectural charter and development doctrine for upstream engineering.
