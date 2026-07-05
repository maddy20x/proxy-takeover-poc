# 🔴 AdminUpgradeabilityProxy - Critical Proxy Takeover Vulnerability

## Overview
This repository contains a **Proof of Concept (PoC)** for a critical vulnerability in `AdminUpgradeabilityProxy` contracts.

The `ifAdmin` modifier incorrectly forwards non-admin calls to the implementation contract, allowing **any unprivileged user** to take complete control of the proxy.

## 🎯 Vulnerability Summary

| Attack | Description | Impact |
|--------|-------------|--------|
| **Attack 1: Non-Admin Upgrade** | Any user can change the implementation | Full proxy control |
| **Attack 2: Admin Hijacking** | Admin gets overwritten via `upgradeToAndCall` | Complete admin takeover |

## 📁 Repository Structure
