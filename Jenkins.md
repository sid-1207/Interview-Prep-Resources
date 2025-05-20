# Jenkins

## Overview

- Jenkins is used to **Build**, **Test**, and **Deploy** software using **pipelines**.
- Based on **Master-Slave (Agent)** architecture.

---

## Architecture

### Master
- Controls pipelines  
- Schedules builds  
- Detects code changes (e.g., in Git)  

### Slave (Agent)
- Performs the actual build and test jobs  
- Selected by master based on configuration and rules

---

## Flow

1. Developer commits code to a Git repository  
2. Jenkins Master detects the commit  
3. Master triggers the pipeline  
4. Assigns a suitable agent to execute the job  
5. Agent runs the build/test/deploy tasks

---

## Agent Types

- **Permanent Agents**  
  - Dedicated servers for running jobs  
  - Examples: Standalone Windows/Linux servers  

- **Cloud Agents**  
  - Dynamic agents spun up on demand (e.g., using AWS, Kubernetes)  

---

## Build Types

- **Freestyle Build**  
  - Basic build configuration  
  - Similar to shell scripting  
  - Less modular and flexible  

- **Pipelines**  
  - Written in **Groovy** syntax  
  - Uses **stages** to break down the build process  
  - Suitable for complex workflows  
  - Dynamically adapts to the **intensity of the job** at runtime  

