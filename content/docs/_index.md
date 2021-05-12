---
title: Introduction to Fluvio
menu: Overview
section: Docs
description: tiled view with a top banner
---

- Fluvio is a distributed streaming platform
- Built for real-time use-cases
- Written in Rust
- Users use it by Producing and Consuming
- There are Topics and Partitions
  - There may be many partitions per topic and partitions may live on different SPUs
  
We have:

- Connect:
  - At the core, data is sent to and from Fluvio
  - This is known as producing and consuming
  - We have language APIs for producing and consuming
  - Produce records to a particular topic, keys determine partition
  
- Enrich
  - Filter and transform data in-cluster without needing external tools
  - SmartStreams use WASM
  
- Interfaces
  - We have a CLI to take care of setup and management
  - We have language clients for interacting with Fluvio from other languages

- Architecture
  - Cluster vs Client
  - Cluster has SC and SPUs
  - SC coordinates cluster, e.g. provisioning pods in K8s
  - SPUs stream and store data
