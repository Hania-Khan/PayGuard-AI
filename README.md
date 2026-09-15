# PayGuard-AI
PayGuard AI is a cloud-native payments platform that processes transactions through an immutable ledger,  routes payments across multiple simulated providers, detects fraud using both deterministic rules and an AI- assisted investigator, and demonstrates measurable scalability under load - directly extending real fintech architecture experience.

* **Backend:** NestJS + TypeScript
* **Database:** PostgreSQL
* **Cache:** Redis
* **Containerisation:** Docker + Docker Compose
* **ORM:** TypeORM

## 🏗️ Current Architecture

```text
                 PayGuard AI
                      |
             +--------+--------+
             |        |        |
           API    PostgreSQL  Redis
          :3000     :5432     :6379
             |
        Docker Network
```

## 📁 Project Structure

```text
payguard-ai/
├── apps/
│   └── api/
├── packages/
├── services/
├── infrastructure/
├── tests/
├── docs/
├── docker-compose.yml
├── .env.example
├── .gitignore
└── README.md
```

## 🐳 Running Locally

Create your environment file:

```bash
cp .env.example .env
```

Start the application:

```bash
docker compose up --build
```

Check running containers:

```bash
docker compose ps
```

Stop the application:

```bash
docker compose down
```

## 🔐 Environment Variables

Credentials and environment-specific configuration are stored in `.env` and are **not committed to Git**.

Use `.env.example` as the template.

## 🎯 Roadmap

* [ ] Payment processing API
* [ ] Idempotency
* [ ] Double-entry ledger
* [ ] Event-driven architecture with Kafka
* [ ] Risk scoring engine
* [ ] AI-powered fraud analysis
* [ ] Observability
* [ ] CI/CD
* [ ] AWS deployment with Terraform

