
<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=0,2,5,10,30&height=220&section=header&text=🛡️%20MuleGuard&fontSize=50&fontColor=fff&animation=twinkling&fontAlignY=35&desc=Tamil%20Nadu%20Fraud%20Intelligence%20Platform&descAlignY=58&descSize=22" width="100%"/>

  ### 🚨 Real-Time Fraud Detection System for Banking Networks
  
  *An advanced full-stack intelligence application specializing in mule account identification, live transaction network mapping, and cross-jurisdiction tracking across Tamil Nadu.*
</div>

---

## 📌 Table of Contents
* [🚀 Features](#-features)
* [🛠️ Tech Stack](#️-tech-stack)
* [📋 Prerequisites](#-prerequisites)
* [⚡ Quick Start](#-quick-start)
* [🔍 Detection Rules & Heuristics](#-detection-rules--heuristics)
* [📊 Data Model & Thresholds](#-data-model--thresholds)
* [📱 API Endpoints & WebSockets](#-api-endpoints--websockets)
* [🎯 Use Cases](#-use-cases)
* [🔒 Security & Production](#-security--production)
* [🗺️ Roadmap](#️-roadmap)
* [👨‍💻 Authors](#-authors)

---

## 🚀 Features

### ⏱️ Real-Time Detection
* **Advanced Engine:** Employs **12 analytical fraud detection rules** enhanced by AI anomaly scoring.
* **Live Monitoring:** Uses stateful WebSocket connections for immediate UI updates on pending transfers.
* **Spatial Tracking:** Tracks suspicious behavior across regional hubs (*Chennai, Coimbatore, Madurai, Trichy*).
* **Fingerprinting:** Collects device and IP telemetry data to isolate multi-account identity overlap.

### 🏦 Banking Integration
* **API Validation:** Simulates programmatic hooks to verification models of prominent Indian banking APIs.
* **KYC Surveillance:** Continually logs and checks compliance flag discrepancies.
* **Risk Categorization:** Auto-scores velocity patterns into actionable threat buckets.

### 🖥️ Interactive Analyst Dashboard
* **Network Graph:** Dynamic, visual **Knowledge Graphs** rendering complex relational transactional rings.
* **Workflow Automation:** Inline investigation tooling for clearing or escalating flags instantly.

---

## 🛠️ Tech Stack

| Component | Technology | Role |
| :--- | :--- | :--- |
| **Backend Core** | Node.js + Express | REST architecture & core router engine |
| **Database** | MongoDB + Mongoose | High-velocity storage & object mapping |
| **Real-Time Layer** | Socket.io | Bi-directional streaming for live alerts |
| **AI Processing** | OpenRouter AI | Graph Neural Network (GNN) behavioral logic |
| **Frontend UI** | React 19 + Framer Motion | Modern, accelerated canvas with smooth animations |
| **Data Engine** | Force Graph + Lucide | Complex network topography canvas and icons |

---

## 📋 Prerequisites
* **Node.js:** `v18.0.0` or higher
* **MongoDB:** `v5.0.0` or higher (Local Community Server or Atlas Cluster Instance)
* **Access Tokens:** Active `OpenRouter API Key` configuration

---

## ⚡ Quick Start

### 1. Clone & Install Dependencies
```bash
git clone <repository-url>
cd MULE

# Install server dependencies
npm install

# Install client dependencies
cd client && npm install
cd ..

```

### 2. Environment Configuration

Create a `.env` file in your root workspace:

```env
PORT=5000
NODE_ENV=development
MONGO_URI=mongodb+srv://<user>:<password>@cluster.mongodb.net/mule_detection
OPENROUTER_API_KEY=sk-or-v1-your-api-key-here

```

### 3. Execution Engines

```bash
# Spin up both client and server parallel execution tracks
npm start

# Or activate services independently
npm run server  # REST Core & WS Server Instance -> localhost:5000
npm run client  # Vite Dev Bundler Frontend Platform -> localhost:5173

```

---

## 🔍 Detection Rules & Heuristics

Every active transaction transaction is parsed through structural, behavioral, and telemetry filters to compute an aggregate risk weight percentage.

### 📐 Risk Vector Mapping

| Target Rule | Signature Identifier | Base Risk Penalty |
| --- | --- | --- |
| **High-Velocity Transfer** | Multiple discrete transfers within a 2-minute epoch | `+35%` |
| **Circular Flow** | Loop route ($A \rightarrow B \rightarrow A$) closing inside 5 minutes | `+45%` |
| **Shared Hardware Signatures** | Single Device UUID processing distinct account authorizations | `+30%` |
| **Fan-Out Topology** | Single origin point $\rightarrow$ 3 or more concurrent receivers | `+40%` |
| **Fan-In Topology** | 3 or more discrete payment origins $\rightarrow$ single collector | `+40%` |
| **Transaction Structuring** | Artificially split balances targeted just beneath reporting limits | `+35%` |
| **Smurfing** | Unbroken replication of fine token value metrics | `+30%` |
| **Anomalous Hours** | Activity spikes occurring during dark windows (1:00 AM - 4:00 AM) | `+20%` |
| **Geographic Warp** | High physical velocity between disparate municipal cell towers | `+25%` |
| **KYC Vulnerability** | Unverified credentials, incomplete registrations, or legacy data | `+25% to 60%` |

---

## 📊 Data Model & Thresholds

* **Anonymized Accounts:** `rajesh_kumar_sbi2023`, `priya_sharma_hdfc4589`
* **Currency Windows:** Operational ranges spanning ₹500 to ₹2,00,000+
* **Regional Entities:** Telemetry points map onto local ISPs (*Jio, Airtel, BSNL*) across primary Tamil Nadu grids.
* **Supported Rails:** API simulation intercepts webhooks across GPay, PhonePe, Paytm, and unified BHIM protocols.

### ⚖️ Regulatory Monitoring Metrics

* **₹50,000:** Standard Regulatory Record Threshold
* **₹1,00,000:** High-Priority Monitoring Tier
* **₹2,00,000:** Immediate High-Value Threat Notification Trigger

---

## 📱 API Endpoints & WebSockets

### 🔌 REST Controller Routes

```http
GET    /transactions                # Fetches active data log window
GET    /transaction/:id             # Inspects deep object properties of an asset
POST   /transaction                 # Enqueues or tests a new transaction object
PATCH  /transaction/:id/block       # Freezes transaction and targets linked node IDs
PATCH  /transaction/:id/investigate # Places transaction under analyst review status
PATCH  /transaction/:id/clear       # Overrides system flags as a verified clean ledger
GET    /stats                       # Collects computed values for dashboard metrics
GET    /alerts                      # Returns stored database event logs

```

### 🛰️ Socket.io Client Event Handles

* `newTransaction` $\rightarrow$ Streams live inbound transactions to the streaming view.
* `newAlert` $\rightarrow$ Dispatches a critical visual toast alert for events exceeding the `70%` risk score.
* `transactionUpdated` $\rightarrow$ Modifies UI node parameters on a state override (*blocked/cleared*).

---

## 🎯 Use Cases

### 🏛️ Banking Security Operations

* Isolates structural account chains in real time before monetary drawdowns occur.
* Automatically creates graph visualization maps of local networks for internal auditors.

### 🛡️ Law Enforcement & Cyber Cells

* Generates clear digital forensic patterns for cross-jurisdiction data tracking.
* Exports detailed threat metrics mapping out localized fraud networks operating inside city lines.

---

## 🔒 Security & Production

### 🛡️ Data Sanitization

* Architecture relies entirely on non-sensitive financial abstractions.
* Personally Identifiable Information (PII) is securely salted and masked before entering standard logging stores.

### ⚙️ Production Operations

```yaml
# To spin up production containers in detached mode:
docker-compose up -d

# To observe streaming engine container analytics logs:
docker-compose logs -f

```

* **Scaling Vectors:** Designed for horizontal scaling using MongoDB horizontal sharding and a high-performance Redis cache layer.

---

## 🗺️ Roadmap

### 📦 Current Lifecycle (v1.5)

* [x] Enhanced contextual AI processing integration via OpenRouter.
* [x] Real-time operational queues allowing multiple analysts to safely review incidents concurrently.
* [x] Exportable reporting structures tailored for technical regulatory submissions.

### 🚀 Future Milestones (v2.0)

* [ ] Native local Graph Neural Network model training directly within the pipeline.
* [ ] Live integrations with live clearing interfaces.
* [ ] Dedicated mobile interface deployment for field security notifications.

---

## 👨‍💻 Authors

| Developer | Contact / Links |
| --- | --- |
| **Tharunkumar K** | [](https://www.google.com/search?q=https://github.com/Tharun4743) [](https://www.google.com/search?q=https://tharunkumark4743.netlify.app) |
