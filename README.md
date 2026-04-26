# Contact List API Testing

A comprehensive REST API test automation project for a Contact List microservice, built with **Postman** and **JavaScript** test scripts. This repository contains structured test collections, environments, documentation, and bug reports covering end-to-end validation of both `Users` and `Contacts` domains.

---

## Project Overview

This project validates the functionality, security, and performance of a Contact List REST API. It includes automated test cases for CRUD operations, authentication flows, negative path validation, and response time SLAs.

### Domains Tested
- **Users** — registration, login, logout, profile retrieval, updates, and deletion
- **Contacts** — creation, retrieval, updating, and deletion of contact records

---

## Repository Structure

```
├── postman/
│   ├── collections/          # Postman test collections
│   │   ├── Contacts test_cases.postman_collection.json
│   │   └── Users test_cases.postman_collection.json
│   └── environments/         # Postman environment variables
├── .postman/
│   └── resources.yaml        # Postman workspace/cloud resource mapping
├── API_Test_Plan_ContactList.docx
├── Bug_Report_API.docx
├── Test_Summary_Report_ContactListAPI.xlsx
├── RTM API (Final).xlsx          # Requirements Traceability Matrix
├── Test Cases- Contact list.xlsx
├── Contacts test_cases.postman_collection.json
└── Users test_cases.postman_collection.json
```

---

## Test Coverage

| Category | Details |
|----------|---------|
| **Test Cases** | 40+ automated test cases |
| **Assertions** | 240+ JavaScript assertions |
| **HTTP Methods** | POST, GET, PATCH, DELETE |
| **Auth Types** | Bearer token, no-auth, invalid/expired tokens |
| **Negative Tests** | Missing fields, invalid data types, malformed payloads, unauthorized access |
| **Performance** | Response time validation (<200ms to <1000ms) |

---

## Tools & Technologies

- **Postman** — API testing & collection runner
- **JavaScript (Chai assertions)** — automated validation scripts
- **Postman Environments** — dynamic variable management (`base_url`, `token`, `contactId`)
- **Git/GitHub** — version control & collaboration

---

## Key Features

- **Dynamic Environment Variables** — token extraction and contact ID chaining across requests
- **Pre-request Scripts** — automated user creation and auth setup for dependent test cases
- **Modular Collections** — organized by domain (Users / Contacts) and HTTP method
- **Edge-case Coverage** — empty bodies, invalid tokens, duplicate entries, boundary values
- **Collaborative QA Docs** — Test Plan, RTM, Bug Report, and Summary Report

---

## How to Run

1. Open **Postman** and import the collections from `postman/collections/`.
2. Import the environment files from `postman/environments/`.
3. Set the `base_url` variable in your active environment.
4. Run the collections individually or via Postman Runner / Newman.

```bash
# Optional: Run with Newman (CLI)
newman run "postman/collections/Users test_cases.postman_collection.json" \
  -e "postman/environments/mainenv.environment.yaml"
```

---

## Contributors

This project was developed collaboratively by a QA team using shared Postman workspaces and GitHub for version control.

---

## License

This project is for educational and portfolio purposes.
