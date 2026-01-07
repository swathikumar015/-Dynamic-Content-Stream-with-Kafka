# 🌀 Dynamic Content Stream with Kafka

A real-time adaptive content streaming system where topics can be created, approved, and streamed dynamically using Apache Kafka.

---


## 🎯 Objective
To design a scalable Kafka-based platform supporting:
- Dynamic topic creation & management via **Kafka Admin API**  
- Multi-threaded producers for real-time ingestion  
- Consumers with dynamic topic subscriptions  
- Central database for topic & user mapping  
- Simple web UI for visualization  

---

## ⚙️ System Overview

### 🧱 **Producer (System 1)**
- Multi-threaded design:
  - **Publisher Thread:** Publishes messages to Kafka topics  
  - **Input Listener:** Captures incoming data  
  - **Topic Watcher:** Monitors DB and creates approved topics via Admin API  

### 🧩 **Kafka Broker (System 2)**
- Central message pipeline  
- `auto.create.topics.enable = false` for controlled topic creation  

### 📥 **Consumers (System 3)**
- Fetch active topics from DB  
- Subscribe/unsubscribe dynamically  
- Stream live data from producer  

### 🧠 **Admin & Database (System 4)**
- Approves/rejects topic requests  
- Stores:
  - `topics` → topic metadata & status  
  - `user_subscriptions` → user-topic mappings  
- Notifies producer on approval  

---

## 🧰 Tech Stack
- **Language:** Python  
- **Broker:** Apache Kafka  
- **Database:** SQLite / MySQL  
- **Web Framework:** Flask / FastAPI  
- **Libraries:** `kafka-python`, `threading`, `requests`, `sqlite3`, `json`

---

## 🚀 Key Features
✅ Dynamic topic lifecycle (create → approve → stream)  
✅ Multi-threaded producer & real-time consumers  
✅ Centralized topic & subscription control  
✅ Simple admin interface for approvals

---


---

## 🏁 How to Run
1. Start **Kafka & Zookeeper**
2. Run the **Admin &**
3. Start the **Producer**
4. Run **Consumer(s)**
5. Access the **Web UI** to view topics and subscriptions



