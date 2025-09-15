
# README for FloatChat: AI-Powered Conversational Interface for Ocean Data

## Project Overview

FloatChat is a next-generation platform designed to democratize access to oceanographic data by combining scientific data processing with advanced AI-powered conversational capabilities. It transforms raw ARGO ocean float data into an interactive, explainable, and scientifically rigorous chat system that enables users to query, visualize, and analyze ocean data without needing specialized coding skills.

## Key Features

- Physics-aware embeddings for better scientific accuracy  
- Model Context Protocol (MCP) for safe, auditable LLM-to-SQL translation  
- Multi-modal retrieval augmented generation (RAG) combining text, metadata, and charts  
- Real-time ingestion and visualization using edge agents and LeafletJS  
- Explainability with provenance, quality checks, and confidence scores  
- Intuitive chat interface with dashboard visualizations

## System Architecture

- Data ingestion from NetCDF ARGO profiles → normalized SQL and Parquet storage  
- Vector embeddings with FAISS/Chroma for semantic querying  
- RAG pipeline using LLM with a Model Context Protocol mediator  
- Backend API layer for query execution and data serving  
- Frontend dashboard with AI chat interface, LeafletJS maps, and chart visualizations  
- Deployment with Docker and Kubernetes for scalable and reproducible demos

***

## Work Division and Responsibilities

The following task assignments reflect the core components of the project. Each team member will lead their respective domain and coordinate with others for integration.

| Team Member | Responsibilities                                                                                         |
|-------------|-------------------------------------------------------------------------------------------------------|
| Shristi     | - Data Download, Parsing, and Ingestion Pipeline                                                      |
|             | - Convert ARGO NetCDF data into normalized SQL schema and store in PostgreSQL                          |
|             | - Automate ETL workflows using Python (xarray, pandas, dask)                                          |
| Fine-tune LLM Developer | - Fine-tune the large language model on oceanographic question-answering datasets             |
|             | - Develop and optimize embeddings tailored for ocean data semantics                                   |
| MCP Server Developer | - Implement the Model Context Protocol (MCP) server to safely translate natural language queries to SQL |
|             | - Build audit logging and traceability features                                                       |
| Frontend Developer | - Create AI chat interface enabling natural language queries                                        |
|             | - Integrate chat with backend LLM + RAG service                                                       |
|             | - Build interactive dashboards with profile plotting and export functionality                         |
| Frontend/Visualization Developer | - Develop LeafletJS map to show real-time float locations and trajectories                    |
|             | - Integrate charting libraries (e.g., Plotly) for data visualization                                  |
| DevOps Engineer | - Containerize all backend and frontend services using Docker                                      |
|             | - Setup CI/CD pipelines and Kubernetes (k3s) cluster deployment                                      |
|             | - Manage cloud resources and GPU allocation for LLM inference                                        |

***
