# VectorShift Pipeline Builder Assessment

This project is a simplified pipeline builder that allows users to visually create and connect nodes to form a processing pipeline and submit it to a backend parser.

## Features 
- Drag and drop nodes onto the canvas
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

API Endpoint:

```
POST /pipelines/parse
```

Example Response:

```
{
  "num_nodes": 3,
  "num_edges": 2,
  "is_dag": true
}
```
# Running the Project

### Backend ### Frontend
```bash
cd backend cd frontend
uvicorn main:app --reload

Backend runs on:

```
http://localhost:8000
```

API documentation:

```
http://localhost:8000/docs
```

### Frontend

cd frontend
npm install
npm start

Frontend runs on:

```
http://localhost:3000
```

## Project Structure

```
VectorShift-assessment
│
├── README.md
│
├── frontend
│   ├── src
│   ├── package.json
│
└── backend
    ├── main.py
    └── requirements.txt
```

## Technologies Used

Frontend:

* React
* React Flow

Backend:

* FastAPI
* Python







