# 🧠🔐 PsychSecure

### Human Behaviour & Cybersecurity Analytics Platform

PsychSecure is a data-driven cybersecurity platform that studies **human behaviour in cybersecurity**.

The project combines:

* 🧠 Psychology
* 🔐 Cybersecurity
* 📊 Data Engineering
* 💻 Software Engineering

The goal is to understand patterns in cybersecurity behaviour, such as phishing clicks, suspicious-email reporting, security training, and security awareness.

> **Note:** PsychSecure uses simulated/anonymized data. It does not diagnose people or make psychological judgments about individuals.

---

## 🎯 Project Goal

Cybersecurity is not only about technology.

Human behaviour can also play an important role in security incidents.

PsychSecure collects cybersecurity behaviour data and processes it through a data pipeline.

The system then provides analytics through an API and dashboard.

---

## 🔄 How It Works

```text
                DATA SOURCES
                     │
        ┌────────────┼────────────┐
        ↓            ↓            ↓
   Phishing       Security     Training
     Events         Events       Data
        │            │            │
        └────────────┼────────────┘
                     ↓
              DATA INGESTION
                     ↓
              Kafka / Python
                     ↓
               DATA PIPELINE
                     ↓
             Airflow + Python
                     ↓
                PostgreSQL
                     ↓
                   dbt
                     ↓
              DATA ANALYTICS
                     ↓
                 FastAPI
                     ↓
                DASHBOARD
```

---

# 🧠 Psychology Component

The project uses psychology concepts related to human behaviour and cybersecurity.

Examples include:

* Risk perception
* Decision-making
* Security awareness
* Behaviour patterns
* Social engineering
* Human factors

The platform can compare survey responses with simulated cybersecurity behaviour.

For example:

> Do people who report higher security awareness also report more suspicious emails?

---

# 🔐 Cybersecurity Component

The platform focuses on human-related cybersecurity events.

Examples:

* Phishing emails
* Phishing clicks
* Suspicious-email reporting
* Security warnings
* Password-related events
* Security training
* Incident reporting

The project uses simulated cybersecurity events rather than attacking real systems.

---

# 📊 Data Engineering Component

PsychSecure demonstrates a complete data pipeline.

The pipeline can include:

* Data ingestion
* Data validation
* Data cleaning
* Data transformation
* Batch processing
* Stream processing
* Data storage
* Data analytics

### Technologies

| Technology       | Purpose                     |
| ---------------- | --------------------------- |
| Python           | Data processing and backend |
| PostgreSQL       | Database                    |
| Apache Airflow   | Workflow orchestration      |
| dbt              | Data transformation         |
| Kafka / Redpanda | Streaming data              |
| Apache Spark     | Large-scale processing      |
| FastAPI          | REST API                    |
| Docker           | Containerization            |
| Git/GitHub       | Version control             |

---

# 💻 Software Engineering Component

PsychSecure includes a backend API.

Example endpoints:

```text
GET /employees
GET /security-events
GET /phishing-analysis
GET /behaviour-trends
GET /risk-summary
POST /security-event
```

The API provides processed information to the dashboard.

---

# 📈 Dashboard

The dashboard can display:

### Security Overview

```text
Security Events       82,451
Phishing Attempts     12,340
Phishing Click Rate   18.4%
Reports Submitted     7,821
```

### Analytics

The dashboard can show:

* Phishing behaviour over time
* Security incidents by department
* Training completion
* Phishing click trends
* Reporting behaviour
* Behavioural patterns
* Security awareness trends

---

# 🔎 Behavioural Analysis

PsychSecure can identify patterns in the dataset.

For example:

```text
Training Completed
        ↓
Phishing Clicks
        ↓
Suspicious Email Reports
        ↓
Behavioural Analysis
        ↓
Security Insights
```

The system can explain which factors contributed to an observed pattern.

It should not treat these patterns as psychological diagnoses.

---

# 🔒 Privacy & Security

Privacy is an important part of the project.

The platform is designed to use:

* Anonymized employee IDs
* No real employee names
* No unnecessary personal information
* Role-based access
* Authentication
* Secure API endpoints
* Audit logging
* Data validation
* Environment variables for secrets

Example:

```text
Employee #1042
```

instead of:

```text
John Smith
```

---

# 🏗️ Project Structure

```text
psychsecure/
│
├── api/
│   ├── main.py
│   ├── routes/
│   └── services/
│
├── data/
│   ├── raw/
│   └── sample/
│
├── pipeline/
│   ├── ingestion/
│   ├── processing/
│   └── validation/
│
├── airflow/
│   └── dags/
│
├── kafka/
│   ├── producer/
│   └── consumer/
│
├── dbt/
│   ├── models/
│   ├── tests/
│   └── seeds/
│
├── analytics/
│
├── dashboard/
│
├── tests/
│
├── docker-compose.yml
├── requirements.txt
└── README.md
```

---

# 🚀 Getting Started

## 1. Clone the repository

```bash
git clone https://github.com/yourusername/psychsecure.git
```

## 2. Enter the project

```bash
cd psychsecure
```

## 3. Create a virtual environment

```bash
python -m venv venv
```

Activate it:

### Windows

```bash
venv\Scripts\activate
```

### macOS/Linux

```bash
source venv/bin/activate
```

## 4. Install dependencies

```bash
pip install -r requirements.txt
```

## 5. Start the services

```bash
docker compose up -d
```

## 6. Run the API

```bash
uvicorn api.main:app --reload
```

The API will then be available locally.

---

# 🧪 Testing

The project includes automated tests for:

* API endpoints
* Data validation
* ETL processes
* Database operations
* Data transformations

Run tests with:

```bash
pytest
```

---

# 📚 Example Use Case

A company runs a simulated phishing campaign.

PsychSecure receives the events:

```text
Employee 101 → Clicked
Employee 102 → Reported
Employee 103 → Ignored
Employee 104 → Clicked
```

The data is processed through the pipeline.

The dashboard then shows:

```text
Phishing Click Rate
        ↓
Reporting Rate
        ↓
Training Completion
        ↓
Behavioural Trends
```

Security teams can use the information to understand where additional security awareness efforts may be useful.

---

# 🌟 What Makes PsychSecure Different?

PsychSecure combines four areas:

```text
        🧠 Psychology
             +
        🔐 Cybersecurity
             +
        📊 Data Engineering
             +
        💻 Software Engineering
```

Instead of building only a cybersecurity application, the project focuses on the **human side of cybersecurity** and demonstrates how behavioural data can be collected, processed and analyzed.

---

# 🎓 Background

This project was created from an interest in combining:

**Psychology + Technology + Data + Cybersecurity**

The project demonstrates how knowledge of human behaviour can be combined with software and data engineering skills to solve technology-related problems.

---

# ⚠️ Ethical Considerations

PsychSecure is an educational and portfolio project.

It does not:

* Diagnose psychological conditions
* Predict criminal behaviour
* Label people as "good" or "bad"
* Monitor real employees without consent
* Collect unnecessary personal information
* Perform real-world phishing attacks

All demonstrations should use simulated or properly anonymized data.

---

# 🔮 Future Improvements

Possible future features include:

* Real-time Kafka streaming
* Apache Spark processing
* Machine learning for pattern detection
* More advanced behavioural analytics
* Interactive dashboards
* Automated security-awareness recommendations
* Role-based security controls
* Data quality monitoring
* Cloud deployment
* CI/CD pipeline
* Monitoring and observability

---

# 👨‍💻 Skills Demonstrated

This project demonstrates experience with:

**Programming**

* Python
* SQL

**Backend**

* FastAPI
* REST APIs

**Data Engineering**

* ETL
* Data pipelines
* Airflow
* dbt
* Kafka
* PostgreSQL
* Spark

**Cybersecurity**

* Phishing
* Social engineering
* Security awareness
* Human security behaviour
* Privacy

**Software Engineering**

* Git
* Docker
* Testing
* API development
* System architecture

**Psychology**

* Human behaviour
* Decision-making
* Risk perception
* Behavioural analysis
* Research methodology

---

# 📌 Project Status

🚧 **Currently in development**

The project will be developed in stages, starting with a basic data pipeline and database, followed by analytics, API development, streaming, and dashboard features.

---

## 📄 License

This project is intended for educational and portfolio purposes.
