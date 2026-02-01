# Task Processing

## 📌 What is this project?

This repository is a **backend playground focused on task (job) processing and system evolution**.

In simple terms:

> This API allows you to **ask the system to do things**, execute those requests, track their lifecycle, and react to what happens.

---

## 🧠 Core idea

The system revolves around the concept of a **Task**.

A **Task** represents a request for work, such as:

* Sending an email
* Generating a report
* Calling a webhook
* Processing data
* Publishing an event

Each task goes through a lifecycle:

```
PENDING → PROCESSING → DONE
                 ↘ FAILED
```

The project focuses on **how tasks are created, executed, observed, and evolved**, not on complex business rules.

---

## 🏗️ How the system works (high level)

1. A client **creates a task** describing what should be done
2. The system **stores the task** and its metadata
3. The task is **executed** by the system
4. The task status is **updated** based on the outcome
5. Other systems may **observe or react** to the result

Visual flow:

```
[ Client ]
    |
    |  Create task
    v
[ Task Registry ]
    |
    |  Execute
    v
[ Task Executor ]
    |
    |  Perform work
    v
[ DONE | FAILED ]
```

This mirrors how real-world systems like background workers, automation platforms, and internal tooling work.

---

## 🚀 Running the project

```bash
docker compose up
```

The API will be available at:

```
http://localhost:3000
```

