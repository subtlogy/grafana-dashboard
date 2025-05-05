# Grafana Dashboard Collection

This repository is a collection of Grafana dashboard definitions for monitoring various network devices and services using Prometheus and SNMP. Currently it includes only a dashboard for the Yamaha RTX1220, with more device- and use-case dashboards planned.

---

## Project Overview

**Goal:**  
Provide ready-to-use Grafana dashboards that visualize the operational metrics of network devices and servers, improving monitoring and response.

**Stack:**  
- **Data collection:** Prometheus + SNMP Exporter  
- **Visualization:** Grafana  

---

## Prerequisites

Before importing any dashboard, you must have:

1. A running Prometheus server  
2. SNMP Exporter configured  
3. A Grafana instance  
4. SNMP enabled on the target device (e.g. Yamaha RTX1220)  

---

## Yamaha RTX1220 Dashboard

### Overview

- **Location:** `yamaha-rtx1220/`  
- **Metrics visualized:** CPU usage, memory usage, temperature, interface traffic, etc.  
- **Stack:** SNMP → Prometheus → Grafana  

### Import Instructions

1. Use the SNMP Exporter generator to load the RTX1220 MIB.  
2. Add the SNMP Exporter endpoint to your `prometheus.yml`.  
3. In Grafana, go to **Dashboard → Import**, and upload `rtx1220-dashboard.json`.  
4. If panels don’t display data, verify your Prometheus target and Grafana variables.

For detailed steps and examples, see `yamaha-rtx1220/README.md`.

---

## Roadmap

- Dashboards for Juniper, Cisco, Arista, and other routers/switches  
- Server dashboards (e.g. Linux node_exporter)  
