# SAM — Strategic Attack Mapper

### Intelligent Cyber Incident Investigation & Attack Reconstruction System

SAM (Strategic Attack Mapper) is an intelligent cyber incident investigation platform designed to analyze security events, correlate digital evidence, reconstruct potential attack sequences, and visualize cyberattack progression through evidence-backed attack graphs.

It transforms fragmented security logs into structured, explainable investigations using graph theory, search algorithms, temporal reasoning, constraint validation and probabilistic analysis.

---

## Overview

Modern cyberattacks generate enormous volumes of security events across users, devices, processes and network infrastructure. Identifying meaningful connections between these events and reconstructing the sequence of an attack can be challenging.

SAM addresses this problem by providing an integrated investigation workflow that:

- Processes and normalizes security event data.
- Extracts entities from collected evidence.
- Identifies potential relationships between entities.
- Evaluates temporal and contextual constraints.
- Scores candidate relationships using evidence-based criteria.
- Constructs directed attack graphs.
- Explores attack paths using graph search algorithms.
- Reconstructs chronological incident timelines.
- Evaluates competing attack hypotheses.
- Generates structured investigation reports.

## Key Features

### 1. Security Evidence Explorer
- Inspect structured security events and logs.
- View raw and normalized event representations.
- Extract users, IP addresses, hosts, processes, files and domains.
- Filter and search evidence.
- Trace relationships between individual events and entities.

### 2. Algorithm Workbench
The central analytical component of SAM.

Visualizes the complete attack reconstruction pipeline through six stages:

1. Event Processing
2. Entity Extraction
3. Candidate Relationship Generation
4. Temporal Constraint Validation
5. Relationship Scoring
6. Attack Graph Construction

Includes step-by-step execution, intermediate results, mathematical calculations and algorithm explanations.

### 3. Attack Graph Explorer
- Interactive directed attack graph.
- Evidence-backed relationships between entities.
- Node and edge inspection.
- Attack path exploration.
- BFS and DFS graph traversal.
- Identification of potentially significant attack sequences.

### 4. Incident Timeline
- Chronological visualization of security events.
- Reconstruction of attack progression.
- Event-level evidence inspection.
- Correlation between timeline events and graph entities.

### 5. Hypothesis Analysis
- Evaluate alternative explanations for an incident.
- Examine supporting and contradicting evidence.
- Apply rule-based reasoning.
- Use probabilistic analysis where implemented.
- Compare competing attack scenarios.

### 6. Investigation Report
Generate structured investigation reports containing:
- Incident overview.
- Important evidence.
- Extracted entities.
- Reconstructed attack sequence.
- Attack graph findings.
- Hypothesis analysis.
- Investigation conclusions.

### 7. Investigation Dashboard
A centralized overview of the investigation, including incident severity, evidence statistics, extracted entities, relationship metrics and attack progression.

---

## Algorithmic Foundations

SAM incorporates concepts from Artificial Intelligence, graph theory, discrete mathematics and intelligent search.

| Concept | Application |
|---|---|
| Graph Theory | Representing relationships between security entities |
| Breadth-First Search (BFS) | Exploring attack paths |
| Depth-First Search (DFS) | Traversing connected attack structures |
| Best-First Search | Prioritizing promising investigation paths, where implemented |
| Temporal Constraints | Validating chronological compatibility |
| Weighted Relationship Scoring | Evaluating candidate connections |
| Rule-Based Reasoning | Identifying relationships using logical conditions |
| Bayesian Reasoning | Evaluating competing hypotheses, where implemented |
| State-Space Exploration | Representing and exploring possible attack progressions |

### Mathematical Model

The reconstructed attack structure can be represented as a directed graph:

\[
G=(V,E)
\]

Where:

- \(V\) represents extracted entities.
- \(E\) represents evidence-supported relationships.

Candidate relationships can be evaluated using a weighted scoring function:

\[
S(u,v)=w_1I+w_2T+w_3A+w_4R
\]

Where:

- \(I\): Identity or session match.
- \(T\): Temporal compatibility.
- \(A\): Attribution evidence.
- \(R\): Rule-based relationship match.
- \(w_i\): Assigned feature weights.

Temporal compatibility can be evaluated using:

\[
0\leq t_j-t_i\leq \Delta t_{\max}
\]

This helps eliminate relationships that violate defined chronological constraints.

The resulting graph provides an explainable representation of the potential attack sequence, with relationships linked to their supporting evidence.

---

## System Architecture

```text
          SECURITY EVIDENCE
           (CSV / JSON Logs)
                  |
                  v
          EVENT PROCESSING
                  |
                  v
          ENTITY EXTRACTION
                  |
                  v
      CANDIDATE RELATIONSHIP GENERATION
                  |
                  v
       TEMPORAL CONSTRAINT VALIDATION
                  |
                  v
        RELATIONSHIP SCORING
                  |
                  v
         ATTACK GRAPH BUILDER
                  |
          +-------+-------+
          |       |       |
          v       v       v
        PATH   TIMELINE  HYPOTHESIS
       SEARCH  ANALYSIS  ANALYSIS
          |       |       |
          +-------+-------+
                  |
                  v
       INVESTIGATION REPORT
```

---

## Demonstration Scenario

SAM uses a deterministic synthetic corporate network incident to demonstrate the investigation workflow.

**Incident:** SAM-2026-047  
**Description:** Suspected Corporate Network Compromise  
**Severity:** High

The simulated attack progression includes:

1. Suspicious external authentication.
2. Employee account compromise.
3. Suspicious PowerShell execution.
4. Privilege escalation.
5. Lateral movement across internal hosts.
6. Access to sensitive corporate files.
7. Possible data exfiltration.

The same incident dataset is used across the dashboard, evidence explorer, algorithm workbench, attack graph, timeline and investigation report.

*All demonstration incident data is synthetic and does not represent a real-world security breach.*

---

## Technology

SAM is built using the existing repository architecture and its integrated frontend, backend, data-processing and visualization components.

Core technical areas include:

- Security event processing.
- Entity and relationship extraction.
- Graph construction and traversal.
- Constraint-based validation.
- Mathematical relationship scoring.
- Interactive data visualization.
- Explainable investigation workflows.

---

## Getting Started

### Prerequisites

Install the dependencies required by the project:

- Git
- Node.js and npm (if using the existing Node-based application)
- Python (if required by the backend)

### Installation

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/SAM.git
cd SAM
```

Install dependencies according to the project's frontend and backend configuration.

Start the application using the development commands defined in the respective package configuration files.

Open the local URL displayed in your terminal.

---

## Project Structure

The application is organized around the following functional modules:

```text
SAM/
│
├── frontend/
│   ├── dashboard/
│   ├── evidence-explorer/
│   ├── algorithm-workbench/
│   ├── attack-graph/
│   ├── incident-timeline/
│   ├── hypothesis-analysis/
│   └── investigation-report/
│
├── backend/
│   ├── ingestion/
│   ├── normalization/
│   ├── entity-extraction/
│   ├── relationship-mapping/
│   ├── temporal-validation/
│   ├── relationship-scoring/
│   └── graph-construction/
│
├── data/
│   └── synthetic-incidents/
│
└── README.md
```

*The structure above illustrates the logical organization of the system; actual directory names may differ.*

---

## Project Objectives

SAM aims to demonstrate how mathematical and AI-based techniques can be applied to cybersecurity investigations.

Its primary objectives are:

- Reduce the complexity of fragmented security evidence.
- Identify meaningful connections between security events.
- Reconstruct potential attack sequences.
- Apply graph algorithms to investigate relationships.
- Improve the explainability of automated investigation.
- Present complex analytical operations through an interactive interface.

---

## Scope and Limitations

SAM is an academic demonstration and research-oriented prototype.

- Uses synthetic incident data for reproducible demonstrations.
- Relationship scores are analytical scores, not automatically calibrated probabilities.
- Reconstructed attack paths represent evidence-supported hypotheses, not definitive proof of attacker intent.
- Detection quality depends on the completeness and reliability of the available evidence.
- It is not intended to replace enterprise Security Information and Event Management (SIEM) or Endpoint Detection and Response (EDR) platforms.

---

## Future Enhancements

Potential future development includes:

- Support for additional security log formats, including Sysmon and Windows Event Logs.
- Integration with real-time security event streams.
- Advanced probabilistic attack reconstruction.
- Improved uncertainty estimation and evidence confidence.
- Large-scale graph analysis.
- Machine-learning-based anomaly detection.
- Integration with established threat intelligence frameworks.

---

## Academic Project

**SAM — Strategic Attack Mapper**

*Intelligent Cyber Incident Investigation & Attack Reconstruction System*

Developed as an academic project exploring the intersection of Artificial Intelligence, Graph Theory, Algorithms and Cybersecurity.
