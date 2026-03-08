# VectorShift Pipeline Builder Assessment

This project is a simplified pipeline builder that allows users to create and connect nodes visually and submit the pipeline to a backend parser.

## Features
- Drag and drop nodes
- Multiple node types (Input, LLM, Output, Text, API, Filter, Math, JSON, Delay)
- Dynamic variables using {{variable}} syntax
- Connect nodes to form pipelines
- Delete nodes using Delete/Backspace key
- Submit pipeline to backend for parsing

## Backend Functionality
The backend API parses the pipeline and returns:
- Number of nodes
- Number of edges
- Whether the pipeline is a DAG (Directed Acyclic Graph)

## Running the Project

### Backend
```bash
cd backend
uvicorn main:app --reload