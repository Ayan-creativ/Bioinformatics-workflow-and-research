# 🧬 Bioinformatics Workflow OS (Sheet-Based System)

## 📌 Overview

This project is a **state-driven bioinformatics workspace system** built entirely in Google Sheets, functioning as a **Notion-like operational layer for bioinformatics research, pipelines, and data exploration**.

Unlike static spreadsheets, this system implements:

* **dynamic table rendering via dropdown selections**
* **state-controlled content switching**
* **coupled visual + data views**
* **modular workflow navigation**

It behaves more like a **UI-driven application** than a spreadsheet.

---

## 🧠 Core System Concept

> A spreadsheet that behaves like a **state machine + UI layer for bioinformatics workflows**

User interaction flow:

```
[Dropdown Selection] → [State Change] → [Table + Visual Update]
```

This enables:

* Context-aware data display
* Workflow-driven navigation
* Multi-domain exploration without switching sheets

---

## 🏗️ System Architecture

```
                    ┌────────────────────────────┐
                    │     QUICK ACCESS LAYER     │
                    │  (Navigation + State Hub)  │
                    └─────────────┬──────────────┘
                                  │
                     ┌────────────┴────────────┐
                     │   STATE CONTROLLER      │
                     │ (Dropdown Selections)   │
                     └────────────┬────────────┘
                                  │
        ┌─────────────────────────┼─────────────────────────┐
        │                         │                         │
        ▼                         ▼                         ▼
┌──────────────────┐   ┌──────────────────────┐   ┌──────────────────────┐
│ KNOWLEDGE TABLES │   │ WORKFLOW TABLES      │   │ VISUAL RENDER LAYER  │
│ (Proteomics etc) │   │ (Pipelines)          │   │ (Images/Diagrams)    │
└──────────────────┘   └──────────────────────┘   └──────────────────────┘
                                  │
                                  ▼
                    ┌────────────────────────────┐
                    │ LOCKED VIEW / READ LAYER   │
                    │ (Protected Data Sections)  │
                    └────────────────────────────┘
```

---

## ⚙️ Key Functional Features

### 🔹 1. Dropdown-Based State Engine

The system uses **data validation dropdowns** as control inputs.

Example:

* Selecting **"Metagenomics"**
  → dynamically loads:

  * corresponding workflow table
  * associated tools
  * linked resources

This mimics:
👉 **frontend state management inside Sheets**

---

### 🔹 2. Dynamic Table Rendering

Tables are not static.

They change based on:

* selected domain
* selected workflow
* selected biomarker category

#### Example: Meta-genomics Workflow Table

| Category              | Tools Used                               |
| --------------------- | ---------------------------------------- |
| Preprocessing         | SortMeRNA, Trimmomatic, Fastp            |
| Assembly              | Trinity, MEGAHIT                         |
| Quantification        | Salmon, Kallisto, RSEM                   |
| Functional Annotation | eggNOG-mapper, KEGG Mapper, InterProScan |
| Pathway Analysis      | MetaCyc, MapMan                          |

👉 Entire table updates when dropdown state changes

---

### 🔹 3. Multi-Panel Layout System

Each screen is divided into functional panels:

* **Left Panel** → Control + context (dropdowns, descriptions)
* **Center Panel** → Active workflow / data table
* **Right Panel** → Reference datasets / extended info

This creates:
👉 a **dashboard-like UX inside a spreadsheet**

---

### 🔹 4. Biomarker Intelligence Table (Structured Data Layer)

A structured, query-like table:

| Organ/System | Tumor Markers           | Detection Methods        | Relevant Databases |
| ------------ | ----------------------- | ------------------------ | ------------------ |
| Lung         | CEA, CA-125, Cyfra 21-1 | Blood test, imaging (CT) | TCGA, ICGC         |
| Breast       | CEA, CA 15-3            | Mammography, blood test  | CGMD, KEGG         |
| Liver        | AFP, CEA, CA 19-9       | Blood test, ultrasound   | HCCDB              |
| Colorectal   | CEA, CA 19-9, M2-PK     | Stool test, colonoscopy  | CPTAC              |

Features:

* Domain-specific structuring
* Cross-linkable with workflows
* Acts as a **data retrieval layer**

---

### 🔹 5. Coupled Visual Rendering

Each data state is linked with:

* diagrams
* anatomical visuals
* contextual illustrations

Example:

* Selecting **Tumor Markers**
  → updates:

  * table (data)
  * image (organ-wise markers)

👉 This creates a **data + visualization binding layer**

---

### 🔒 6. Locked / Protected Sections (Read Layer)

Certain sections are intentionally **non-editable**:

* Prevent accidental modification
* Maintain data integrity
* Separate:

  * **view layer**
  * **edit/update layer**

This mimics:
👉 **production vs editable environments**

---

### 🔹 7. Biological Database Indexing System

A structured registry of foundational datasets:

| Domain          | Database     | Description                    |
| --------------- | ------------ | ------------------------------ |
| Genomics        | TCGA         | Cancer genome atlas            |
| Genomics        | TargetFinder | Promoter-enhancer interactions |
| Transcriptomics | GEO          | Functional genomics repository |
| Proteomics      | UniProt      | Protein sequence database      |
| Structural      | PDB          | 3D molecular structures        |
| Drug            | ChEMBL       | Bioactive compounds            |
| Chemical        | ZINC         | Compound database              |

👉 Used as:

* reference layer
* integration point for workflows

---

### 🔁 8. Workflow Navigation System

From Quick Access:

Users can directly jump into:

* Algorithms & Tools
* Drug Discovery workflows
* Proteomics pipelines
* Single-cell analysis
* Multi-omics systems

This acts as:
👉 **routing layer of the system**

---

## 🧩 Design Patterns Implemented

* **State-driven UI (via dropdowns)**
* **Manual relational mapping**
* **Separation of concerns**

  * control layer
  * data layer
  * visualization layer
* **Reusable workflow blocks**
* **Schema consistency via tables**

---

## 🛠️ System Capabilities

* Acts as a **knowledge graph (manual form)**
* Simulates a **workflow engine**
* Supports **context-aware exploration**
* Enables **rapid prototyping of bioinformatics systems**

---

## 🔮 Future Evolution

* Convert tables → JSON schema
* Map workflows → executable pipelines
* Integrate with LLMs for query-based navigation
* Build frontend UI replicating this system
* Deploy as a **Bioinformatics Workflow Platform (BioFlow)**

---

## ⚠️ Disclaimer

This project represents a structured system design for bioinformatics workflows and research.
No proprietary or sensitive data is included.

---

## 👤 Author

Ayan
Bioinformatics | Systems Design | AI in Biology
