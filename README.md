# Grafana Dashboard Collection

This repository is a collection of Grafana dashboard definitions for monitoring various network devices using Prometheus and SNMP Exporter.

---

## Project Overview

**Goal:**  
Provide ready-to-use Grafana dashboards that visualize the operational metrics of network devices, improving monitoring and response.

**Stack:**

- **Data collection:** Prometheus + SNMP Exporter
- **Visualization:** Grafana

---

## Prerequisites

Before importing any dashboard, you must have:

1. A running Prometheus server
2. SNMP Exporter configured
3. A Grafana instance (11.0+)
4. SNMP enabled on the target device

---

## Dashboards

### Yamaha RTX1220

- **Location:** `yamaha-rtx1220/`
- **Metrics:** Uptime, CPU, memory, temperature, interface status, per-LAN traffic, errors, discards
- **Details:** [yamaha-rtx1220/README.md](yamaha-rtx1220/README.md)

### Allied Telesis AT-XS916MXT

- **Location:** `allied-telesis-xs916mxt/`
- **Metrics:** Uptime, port status (UP/DOWN/SHUTDOWN), per-port traffic, VLAN/LAG traffic, errors, discards
- **Details:** [allied-telesis-xs916mxt/README.md](allied-telesis-xs916mxt/README.md)

---

## Quick Start

1. Configure `snmp.yml` with the appropriate module for your device.
2. Add the SNMP Exporter scrape job to your `prometheus.yml`.
3. In Grafana, go to **Dashboards → Import**, and upload the dashboard JSON.
4. Select **Prometheus** as the data source.
5. Set the `instance` variable to your device's IP address.

See each dashboard's README for device-specific setup instructions.

---

## Roadmap

- Dashboards for additional network devices (Juniper, Cisco, Arista, etc.)
- Server dashboards (e.g. Linux node_exporter)
