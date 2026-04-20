# 🚀 DocuMind

## 🧠 AI-Powered Document Processing & Rule Engine Platform

DocuMind is a scalable, AI-driven document processing system that extracts structured data from unstructured documents using LLMs and applies configurable rule-based evaluation to automate decision workflows.

---

## ✨ Features

* 📄 Document ingestion (resume, JSON, text)
* 🤖 AI-based data extraction (LLM integration)
* ⚙️ Configurable rule engine (UI-driven)
* 🔄 Asynchronous processing using queue
* 📊 Real-time status tracking (SignalR)
* 🔁 Retry & fault-tolerant workflow
* 🧱 Clean architecture (Domain-driven design)

---

## 🏗️ Architecture

```text
Angular UI
   ↓
.NET API
   ↓
RabbitMQ (Task Queue)
   ↓
Worker Service
   ↓
LLM Extraction
   ↓
Rule Engine
   ↓
Database
   ↓
Kafka (Optional Events)
   ↓
SignalR → UI
```

---

## 🧱 Tech Stack

### Backend

* .NET 10 Web API
* Clean Architecture (Domain, Application, Infrastructure)
* Entity Framework Core
* SignalR

### Messaging

* RabbitMQ (task queue)
* Kafka (event streaming - optional)

### AI

* OpenAI / Azure OpenAI (LLM extraction)
* RAG-ready architecture

### Frontend

* Angular
* RxJS
* Angular Material

### DevOps

* Docker & Docker Compose

---

## 📂 Project Structure

```text
DocuMind/
│
├── backend/
│   ├── DocuMind.Api
│   ├── DocuMind.Application
│   ├── DocuMind.Domain
│   ├── DocuMind.Infrastructure
│   └── DocuMind.Worker
│
├── client/
│   └── documind-ui
│
├── docker/
│   └── docker-compose.yml
│
└── docs/
```

---

## ⚙️ How It Works

1. User uploads a document
2. API stores request and pushes job to queue
3. Worker consumes job asynchronously
4. LLM extracts structured data
5. Rule engine evaluates document
6. Result is stored and pushed to UI via SignalR

---

## 🧠 Example Use Case

### Resume Screening

* Extract candidate details (experience, skills)
* Apply rules:

  * Experience ≥ 3 years
  * Must have .NET
* Generate score and shortlist candidates automatically

---

## 🔁 Workflow

```text
Pending → Validating → Processing → Evaluating → Completed / Failed
```

---

## 🧪 Running Locally

### Backend

```bash
cd backend/DocuMind.Api
dotnet run
```

---

### Frontend

```bash
cd client/documind-ui
npm install
ng serve
```

---

### Docker (Optional)

```bash
docker-compose up --build
```

---

## 🧠 Key Design Decisions

* JSON-based rule engine for flexibility
* Async processing using queues
* Separation of concerns via clean architecture
* Real-time updates using SignalR

---

## 🚀 Future Enhancements

* Multi-tenant support
* Rule versioning
* Advanced LLM evaluation
* Analytics using Kafka
* Distributed scaling

---

## 💬 Interview Highlights

* Designed a modular document processing pipeline
* Implemented async workflows using RabbitMQ
* Integrated LLM for unstructured data extraction
* Built configurable rule engine with UI
* Applied clean architecture for scalability

---

## 👨‍💻 Author

**Tarun Kushwaha**

---

## ⭐ If you found this useful

Give it a star ⭐ and feel free to contribute!
