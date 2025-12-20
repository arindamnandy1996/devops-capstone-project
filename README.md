# DevOps Capstone Project

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![Python 3.9](https://img.shields.io/badge/Python-3.9-green.svg)](https://shields.io/)

Starter repository for the **IBM DevOps Capstone Project** (Course: *IBM-CD0285EN*), part of the **IBM DevOps and Software Engineering Professional Certificate**.

---

## Usage

Use this repository **only via the “Use this Template” button** on GitHub.
Do **not fork** the repository.

This creates a clean copy in your account with no upstream dependency.

---

## Development Environment

Designed to run in the **IBM Developer Skills Network Cloud IDE with OpenShift**.

Initialize the environment by sourcing:

```bash
source bin/setup.sh
```

> ⚠️ Do not run this as a script. It must be sourced.

After setup, your prompt should be:

```bash
(venv) theia:project$
```

---

## Common Commands

Activate virtual environment:

```bash
source ~/venv/bin/activate
```

Install dependencies:

```bash
make install
```

Start Postgres (Docker):

```bash
make db
```

---

## Project Structure

```text
├── service
│   ├── common/     # logging & error handling
│   ├── config.py   # Flask configuration
│   ├── models.py   # data model & business logic
│   └── routes.py   # REST API routes
├── tests
│   ├── factories.py
│   ├── test_models.py
│   ├── test_routes.py
│   └── test_cli_commands.py
└── setup.cfg
```

Follows the **Model–View–Controller (MVC)** pattern.

---

## Data Model – Account

| Field        | Type        | Required |
| ------------ | ----------- | -------- |
| id           | Integer     | Yes      |
| name         | String(64)  | Yes      |
| email        | String(64)  | Yes      |
| address      | String(256) | Yes      |
| phone_number | String(32)  | No       |
| date_joined  | Date        | Yes      |

---

## Your Task

Implement REST APIs for:

* **READ**
* **UPDATE**
* **DELETE**
* **LIST**

Requirements:

* Minimum **95% test coverage**
* Follow **Test Driven Development (TDD)**

---

## Local Kubernetes (Optional)

Use only for **local development**, not Cloud IDE.

```bash
make cluster       # Create local K3D cluster
make tekton        # Install Tekton
make clustertasks  # Install required ClusterTasks
```

---

## Author

**John Rofrano**
Senior Technical Staff Member, IBM Research
Coursera Instructor

---

## License

Apache License 2.0
© IBM Corporation 2022. All rights reserved.
* Rewrite it for **GitHub grading clarity**
* Add a **“How to run tests”** or **CI/CD section**
