# Technical Interview Foundation Portfolio Roadmap

Four independent learning repositories provide reusable examples of transaction validation, relational investigation, responsible AI-assisted development, and graph investigation. All scenarios are simulated. The portfolio supports technical discussion; it does not establish professional, SAP/FICO product, production, fraud investigation, or AML experience.

English is the primary professional language. Each repository retains concise Traditional Chinese and conversational Malaysian Malay revision notes. Use those notes to build understanding, then practise explaining the work in the interview's language.

## FOUNDATION

| Repository | Current evidence | Reuse in interviews |
| --- | --- | --- |
| [Python Data Troubleshooting](https://github.com/Lyon-Tan/python-data-troubleshooting/blob/main/README.md) | A local CSV validator, duplicate checks, issue reports, and regression tests. | Explain functions, sets, validation, failure handling, complexity, and evidence-based troubleshooting. |
| [SQL Data Investigation](https://github.com/Lyon-Tan/sql-data-investigation-lab/blob/main/README.md) | A synthetic SQLite staging schema, 15 investigation queries, and a verification helper. | Explain JOINs, NULL, duplicates, business grain, and expected-versus-actual reconciliation. |
| [AI-Assisted Development](https://github.com/Lyon-Tan/ai-assisted-development-notes/blob/main/README.md) | Review guidance, a prompt example, a deliberately flawed/corrected Python example, and a validation checklist. | Explain how suggestions are reviewed and tested; distinguish a documented workflow from an integrated AI application. |

Foundation means skills that can be reused across technical questions, not a claim that every role requirement is covered. The three repositories are independent; they are not connected as one running system.

## SPECIALISATION

| Repository | Current evidence | Boundary |
| --- | --- | --- |
| [Neo4j Fraud Investigation](https://github.com/Lyon-Tan/neo4j-fraud-investigation-lab/blob/main/README.md) | A fictional property graph, shared-device queries, bounded traversal, flag counts, and scoped write examples. | Risk events are supplied examples. Static syntax/data checks were performed; live Neo4j execution remains unverified. No fraud-ring scoring or AML detection is implemented. |

Use the specialisation when a job description mentions graph data, linked entities, fraud technology, digital identity risk, or investigation tooling. Start with the investigation question, then show how a relationship path helps answer it. A shared device is a lead, not proof of wrongdoing.

## NEXT PROJECTS

All four projects below are **planned, not implemented**. They are candidates for separate future repositories. Keep each small and testable before combining them.

| Proposed project | Learning objective | Suggested acceptance evidence |
| --- | --- | --- |
| API / Backend Integration Lab | Accept synthetic transactions through an API with an explicit input contract and clear failure responses. | Document request/response examples; test malformed input, duplicate requests, and failure behaviour. Add authentication only with a defined scope and tests. |
| RAG Investigation Assistant | Retrieve from approved synthetic investigation notes and produce answers tied to evidence. | Provide a small known-answer set, source references, an insufficient-evidence response, and prompt-injection tests. Do not claim accuracy without evaluation. |
| Transaction Monitoring / AML Lab | Explore transparent, synthetic monitoring rules and analyst review steps. | Define time windows and expected alerts; test false positives, boundary cases, and data gaps. Alerts are review candidates, not proof of money laundering or compliance readiness. |
| Extended AI Fraud Risk Detection | Compare a simple baseline with an AI-assisted approach using suitable synthetic labels. | State label assumptions, separate evaluation data, report relevant error metrics, and retain human review. Do not invent performance figures. |

A practical sequence is API contracts first, then bounded retrieval, explicit monitoring rules, and finally evaluated risk detection. Adjust the sequence to a specific job description rather than adding technology for its own sake.

## Role mapping

This is a **portfolio discussion-priority map**, based on the demonstrated examples and the role titles supplied for this portfolio. It is not a hiring standard or a claim of qualification. Read the actual job description before selecting examples.

- **Core:** lead with this repository when its demonstrated skills match the role's stated tasks.
- **Useful:** use it as supporting evidence for a related question.
- **Bonus:** optional context; do not let it displace a stronger example.

| Role | Python | SQL | AI notes | Neo4j | Important gap to acknowledge |
| --- | --- | --- | --- | --- | --- |
| FICO / ERP Operation Engineer | Core | Core | Useful | Bonus | No FICO/SAP product integration, live operations, or real incident ownership. |
| AI Software Developer | Core | Useful | Core | Bonus | AI notes are not a model API, RAG service, agent, or evaluated AI product. |
| Software Developer | Core | Core | Useful | Bonus | No deployed application, backend API, or service integration. |
| Application Support Analyst | Core | Core | Useful | Bonus | No live monitoring, service-level ownership, or production incident history. |
| System Analyst | Core | Core | Useful | Useful | No stakeholder discovery, approved requirements, or delivered system integration. |
| Business Systems Analyst | Useful | Core | Useful | Bonus | No real business process discovery, stakeholder sign-off, or user acceptance project. |
| Data Analyst | Core | Core | Useful | Useful | No BI dashboard, statistical study, or real business impact measurement. |
| Technology Risk | Useful | Useful | Useful | Bonus | No formal control assessment, audit evidence, or risk-governance implementation. |
| Cybersecurity / IAM | Useful | Useful | Useful | Bonus | No authentication, authorisation, identity lifecycle, or security-testing implementation. |
| Fraud Analyst | Useful | Core | Useful | Core | No real casework, confirmed fraud labels, or validated detection performance. |
| Financial Crime Technology | Useful | Core | Useful | Core | No AML rules engine, sanctions screening, case system, or regulatory reporting. |

Roles with no Core entry expose a current portfolio gap. For example, the existing labs can support a discussion of data quality or safe AI use in cybersecurity, but they do not form an IAM portfolio.

## Reusable improvement backlog

These are future ideas, not current features. The per-repository README gives the full scope.

| Repository | Next learning directions |
| --- | --- |
| Python | Database-backed validation, logging, larger inputs, API input, and automated reconciliation. |
| SQL | Window functions, query optimisation, execution plans, larger reconciliation, and monitoring scenarios. |
| AI notes | Structured outputs, API integration, RAG, tool/function calling, evaluation, and injection/security tests. |
| Neo4j | Monitoring graphs, transparent ring scoring, device/IP links, temporal relationships, algorithms, and analyst workflows. |

Before implementing any item, write one question it should answer, one normal example, one failure case, and a clear expected result. Prefer an explainable small extension to an impressive-looking feature that cannot be defended.

## Portfolio maintenance

Keep each README independently useful on GitHub. Preserve English explanations, runnable examples, limitations, and the concise multilingual notes. Separate implemented behaviour, validation evidence, and proposed work.

This central index publishes copies of the portfolio roadmap and interview usage guide. The four learning repositories remain independent and are linked rather than embedded. The original workspace guides are preserved separately.

Use [INTERVIEW_USAGE_GUIDE.md](INTERVIEW_USAGE_GUIDE.md) to rehearse introductions and select evidence for a job description. This index documents existing learning projects and planned work; it does not implement the proposed projects.
