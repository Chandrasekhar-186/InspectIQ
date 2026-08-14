# InspectIQ

AI-powered **Steel Manufacturing Inspection Platform**.

## V1 Scope

InspectIQ analyzes steel manufacturing inspection videos and live camera feeds,
detects surface defects with YOLO26, retrieves applicable inspection guidance
with RAG, and produces a governed inspection decision using LangGraph and MCP.

## Initial data foundation

- Severstal — primary steel production defect dataset
- NEU-DET — complementary steel defect benchmark
- GC10-DET — complementary industrial steel defect dataset

Datasets are **not committed to GitHub**. See `data/README.md`.

## Architecture

User → Authentication → Usage Validation → Relevance Check → Ingestion →
Delta Bronze → YOLO26 → Delta Silver → RAG/SOP → LangGraph → MCP →
Decision/Alert → Delta Gold → Web Result

## Development order

1. Dataset audit and unified taxonomy
2. Dataset preparation
3. YOLO26 baseline and training
4. Model evaluation and MLflow
5. Video ingestion and Delta Bronze
6. Bronze → YOLO26 → Silver
7. RAG/SOP verification
8. LangGraph + MCP
9. Web application
10. Azure deployment

See `docs/ARCHITECTURE.md` and `docs/DEVELOPMENT_ROADMAP.md`.
