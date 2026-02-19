# bom-graph
A knowledge graph of the Book of Mormon
Book of Mormon Graph Explorer

An experimental semantic knowledge graph of the Book of Mormon, built using an ontology-first approach and designed to evolve toward a full GraphRAG system.

This project begins as a lightweight, GitHub-hosted interactive graph and is intended to grow into a typed, auditable theological knowledge graph capable of cross-canon expansion.

🎯 Project Goals

Build a structured graph of the Book of Mormon.

Represent chapters, people, places, and bridges as typed nodes.

Use typed, directed edges (not generic “related” links).

Preserve provenance for every edge.

Evolve toward semantic linking, clustering, and GraphRAG-style retrieval.

Eventually connect:

Book of Mormon

Bible

General Conference corpus

🧠 Design Principles
Ontology First

Nodes and relationships are explicitly typed. This is not a simple force-directed visualization of word overlap. Every edge has meaning.

Provenance Required

Every edge stores:

Method of creation (manual, dictionary match, sequence, etc.)

Evidence

Optional confidence score

This makes the graph auditable and prevents untraceable AI hallucinations.

Directed Relationships

Theology and narrative are directional. Edges support directionality.

🗂️ Current Version (V1)

Version 1 focuses on:

Chapter-level nodes

Typed edges:

SEQUENCE

MENTIONS_PERSON_NAME

MENTIONS_PLACE_NAME

(Optional) CITES_ISAIAH

Static graph rendering via GitHub Pages

JSON-based schema for portability

No embeddings or AI inference are used in V1.

📊 Data Schema (Simplified)

Nodes:

chapter

person_name

place_name

bridge

Edges:

Directed

Typed

Provenance included

Example structure:

{
  "nodes": [
    {
      "id": "1-nephi-01",
      "type": "chapter",
      "label": "1 Nephi 1",
      "book": "1 Nephi",
      "chapter": 1
    }
  ],
  "links": [
    {
      "source": "1-nephi-01",
      "target": "person_name:nephi",
      "type": "MENTIONS_PERSON_NAME",
      "directed": true,
      "provenance": {
        "method": "dictionary_match",
        "evidence": "Matched token 'Nephi'"
      }
    }
  ]
}
🚀 Roadmap
Version 2

Verse- or paragraph-level nodes

Embedding-based semantic similarity edges

Entity disambiguation (multiple Nephis, Almas, etc.)

Human review workflow

Version 3

Graph clustering and community detection

LLM-generated cluster summaries

Bridge discovery across communities

Cross-canon linking (Bible + General Conference)

Full GraphRAG implementation

🛠 Tech Stack

GitHub repository

GitHub Pages (static hosting)

JSON graph schema

Cytoscape.js (graph rendering)

Future: embeddings, clustering, GraphRAG pipeline

📌 Why This Exists

Scripture contains:

Repeating entities

Thematic arcs

Narrative progression

Doctrinal development

Traditional study tools are linear.
This project explores scripture as a structured semantic network.

It is intended as a study aid and research experiment — not an authoritative theological interpretation engine.

📄 License

Code is licensed under MIT.
Text data licensing depends on source and is handled separately.

🤝 Contributing

Future contributions may include:

Improved entity dictionaries

Additional typed relationships

Provenance validation

Visualization improvements

Please open an issue before major structural changes.
