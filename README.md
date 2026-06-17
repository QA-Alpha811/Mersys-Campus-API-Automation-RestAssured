# 🚀 MERSYS Campus Management System - API Test Automation Framework

<div align="center">

![Java](https://img.shields.io/badge/Java-21-orange?style=for-the-badge&logo=java)
![REST Assured](https://img.shields.io/badge/REST%20Assured-5.5.6-green?style=for-the-badge)
![TestNG](https://img.shields.io/badge/TestNG-7.11.0-red?style=for-the-badge&logo=testng)
![Allure](https://img.shields.io/badge/Allure-2.31.0-yellow?style=for-the-badge)
![Maven](https://img.shields.io/badge/Maven-Build-blue?style=for-the-badge&logo=apache-maven)

**Enterprise REST API Test Automation Architecture for School & Campus Management Services**

</div>

---

## 📋 About The Project

This repository contains an enterprise-level, production-ready REST API test automation framework developed for the **MERSYS Campus Management System** during the specialized backend engineering intern program. Engineered by **TEAM3**, the framework is structured natively in Java using REST Assured and TestNG, completely separating operational network calls from verification layers through clean serialization and deserialization via Jackson POJOs. The suite validates high-risk banking parameters, secure identity authorization tokens, global administrative geographies, examination registries, and dynamic custom field schema injections.

### ✨ Key Features

- ✅ **Jackson Serialization Engine:** Leverages automated Plain Old Java Objects (POJOs) under the `api/pojo/` package for strict payload mapping.
- ✅ **Secure Token Extraction:** Automates login session tracking and dynamically injects authorization bearer parameters across dependent endpoint pipelines.
- ✅ **Comprehensive Validation Matrices:** Combined with **Hamcrest Matchers** to execute rich JSON body schema validation and response time threshold assertions.
- ✅ **Allure Reports Integration:** Complete pipeline integration mapping structural environment details and granular request/response body logs.

## 🛠️ Tech Stack

| Technology | Version | Purpose |
|:-----------|:--------|:--------|
| **Java** | 21 | Core Object-Oriented Language |
| **REST Assured** | 5.5.6 | Java DSL for testing and validating REST services |
| **TestNG** | 7.11.0 | Test Suite Management, Configuration Hooks, and Parallel Executions |
| **Allure** | 2.31.0 | High-Fidelity Test Execution Reporting Framework |
| **Hamcrest** | 3.0 | Declarative Assertion & Matcher Library for Validation Pipelines |
| **Jackson** | 2.20.1 | High-performance JSON Processor and Object-Data Mapper |
| **Maven** | 3.x | Continuous Build Lifecycles and Dependency Orchestration |

## 🌟 Individual Contributions & Ownership

While this automation suite represents a collaborative engineering release by **TEAM3**, my individual technical accountability, endpoint design, and implementation focused on scripting and securing the foundational backend pipelines detailed below:

| Technical User Story | Targeted REST Method & Endpoint | Core Engineering Implementation & Verifications |
|:---------------------|:--------------------------------|:-------------------------------------------------|
| 🔑 **US_001** | `POST /login` | **Authentication & Security Tokenization:** Scripted the core security gateway authentication pipeline. Validates identity claims using the `Login` POJO model, checks structural response values, handles negative credentials boundary states, and extracts the dynamic bearer token to establish session states for all subsequent requests. |
| 🌍 **US_002** | `POST /api/3/countries` | **Dynamic Geography Provisioning:** Engineered the nested country and state initialization workflows. Implements robust request body serialization via the `Country` data model, handles state entity dependencies, validates HTTP status boundaries, and performs deep validation on the newly generated country entry attributes. |

## 📝 Automated Endpoints & Functional Coverage

The complete automation suite covers multi-layered operational modules matching the corporate system endpoints:

| Module Track | Technical Test Class Name | Functional Endpoint Verification Scope |
|:-------------|:--------------------------|:---------------------------------------|
| 🔐 **Authentication** | `US001_Login` | Handles user authentication, token capture, and session specs mapping. |
| 🗺️ **Geography Management** | `US002_CreateCountryWithState` <br> `US003_CRUDState` <br> `US004_CRUD_City` | Validates end-to-end CRUD matrix tracking for global geographical hierarchies including country mappings, states, and city data entries. |
| 📝 **Academic Management** | `US005_ExamsAPITest` <br> `US006_CustomFieldAPITest` | Verifies exam structure mutations, grade thresholds, and dynamic metadata custom field configuration schemas. |
| 👥 **Student Management** | `US007CreateStudentGroup` <br> `US_008_009_AddStudentsByGroupp` | Controls automated student cluster setups, operational student group CRUD, and child entity assignment routines. |

## 📁 Project Structure

The codebase architecture strictly reflects the operational workspace layout:

```text
API_MERSYS_INTERN_PROJECT/
├── pom.xml                                   # Dependency tracking (REST Assured, Jackson, Allure)
├── README.md                                 # Technical framework documentation
└── src/
    └── test/
        └── java/
            └── api/
                ├── pojo/                     # Object-Relational JSON Data Modeling Classes
                │   ├── Country.java
                │   ├── Exams.java
                │   ├── Login.java
                │   └── StudentsByGroup.java
                │
                ├── BaseTest.java             # Request/Response Specification Global Configurations
                ├── US001_Login.java          # Authentication Boundary Tests
                ├── US002_CreateCountryWithState.java # Country Dependency Mapping
                ├── US003_CRUDState.java      # State Level CRUD Validations
                ├── US004_CRUD_City.java       # City Level Structural Verification
                ├── US005_ExamsAPITest.java   # Examination Module Validation Core
                ├── US006_CustomFieldAPITest.java # Metadata Custom Fields Integrations
                ├── US007CreateStudentGroup.java  # Core Student Group Asset Lifecycle
                └── US_008_009_AddStudentsByGroupp.java # Group Membership Ingestion Pipelines
```
🚀 Execution Configurations
Trigger the backend automation suite natively through terminal controls using versatile Maven criteria:

Execute Complete REST API Test Automation Suite
```text
Bash
mvn clean test
```
Trigger a Specific Isolation Regression Runner
```text
Bash
mvn test -Dtest=US001_Login
```
Run Automated Suites and Spin Up Allure Visual Reporting
```text
Bash
mvn clean test
mvn allure:serve
```
📊 High-Fidelity Test Analytics
Upon automated pipeline processing, the framework routes behavioral analytics into the Allure Reports engine:

Raw Metadata Repository Location: target/allure-results/

The dashboard spins up an interactive server visualization containing:

High-level test summary tracking success trends, flakiness, and pass/fail metrics.

Comprehensive request/response tabulations capturing exact headers, query parameters, and JSON payloads.

Detailed tracking metrics displaying transaction execution times.

Granular error trace graphs mapped directly to individual Hamcrest validation statements.

To launch the reporting dashboard locally over an automated port:
```text
Bash
mvn allure:serve
```
🏆 Backend Engineering Best Practices
Zero Hardcoded Data Payload Management: Ensure all dynamic payloads are generated cleanly through isolated POJO schemas, eliminating static text bodies.

Dynamic Session Reuse: Avoid redundant server processing by utilizing token parameters globally across operational specs hooks.

Explicit Network Status Verifications: Guarantee service stability by asserting exact HTTP status codes before scanning payload structures.

Independent Test Isolation: Clean and restore testing data loops within local execution sessions to maintain total framework independence.

Engineered with precision and excellence by TEAM3
