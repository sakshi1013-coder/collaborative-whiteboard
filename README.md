# Collaborative Whiteboard System (Event Streaming)

A simplified real-time collaborative whiteboard system inspired by Miro and Figma, built to demonstrate event-driven architecture, real-time synchronization, and publish/subscribe communication using Python.

---

# Project Objective

The goal of this project is to design and simulate a collaborative whiteboard system where multiple users can draw, edit, and interact on a shared board in real time.

The system demonstrates:
- Real-time collaboration
- Event streaming architecture
- Pub/Sub communication
- Event ordering
- Undo/redo handling
- Persistence and recovery
- Scalable system design concepts

---

# Important Note

This is a simplified student-level prototype implementation built in Python/Google Colab/Jupyter Notebook to demonstrate system design concepts without requiring complex distributed system setup.

The following production components are simulated:

| Production Component | Simplified Version |
|---|---|
| Apache Kafka | Python Queue |
| Redis Cache | Python Dictionary |
| WebSocket Gateway | Simulated Event Flow |
| Database | SQLite |
| Frontend Canvas | Python Client Simulation |

---

# Features

## Core Features
- Real-time event processing
- Event-driven architecture
- Publish/Subscribe model
- Event broadcasting
- Queue-based event stream
- Undo/redo support
- SQLite event persistence
- Board state caching

## Optional Concepts Included
- Event replay
- Snapshot recovery
- Conflict resolution explanation
- Scalability considerations

---

# Tech Stack

| Component | Technology |
|---|---|
| Backend | Python |
| Event Stream | queue.Queue() |
| Database | SQLite |
| Cache | Python Dictionary |
| Concurrency | threading |
| Notebook Environment | Jupyter / Google Colab |

---

# Functional Requirements

The system supports:
- Create/join board sessions
- Draw events
- Real-time synchronization
- Event broadcasting
- Undo/redo actions
- Persistent event storage
- Board state management

---

# Non-Functional Requirements

| Requirement | Description |
|---|---|
| Low Latency | Fast event updates |
| Scalability | Supports event streaming concepts |
| Consistency | Ordered event processing |
| Availability | Queue-based asynchronous handling |
| Fault Tolerance | Event persistence and replay |
| Durability | SQLite event storage |

---

# High-Level Design (HLD)

## Main Components

| Component | Responsibility |
|---|---|
| Client Simulation | Simulates users |
| Collaboration Server | Receives events |
| Event Queue | Event stream/pub-sub |
| Event Processor | Processes events |
| Cache Store | Stores latest board state |
| Database | Stores event history |
| Undo/Redo Manager | Maintains action history |
| Broadcast Layer | Sends updates to users |

---

# Low-Level Design (LLD)

## APIs / Events

| API/Event | Purpose |
|---|---|
| connect(board_id) | Join board |
| sendEvent(event) | Send drawing event |
| receiveEvent() | Receive updates |
| undo() | Undo action |
| redo() | Redo action |

---

# Event Model

```json
{
  "event_id": "evt_1",
  "board_id": "board_1",
  "user_id": "user_1",
  "type": "draw",
  "payload": {
    "shape": "line"
  },
  "timestamp": 1746523000
}
