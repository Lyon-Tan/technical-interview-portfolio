# Technical Interview Foundation Portfolio: Interview Usage Guide

Use these repositories as concrete learning evidence. They are independent simulated labs, not components of a deployed system. Describe only code, queries, and checks you can explain and reproduce. AI helped create these materials; distinguish your understanding and validation from independent authorship.

English is the primary professional language. Existing Traditional Chinese and conversational Malaysian Malay notes are revision aids; use them to understand concepts before explaining the same reasoning in the interview's language.

## 30-second portfolio introduction

> I have a small Technical Interview Foundation Portfolio using simulated transaction data. Python covers validation and duplicate reporting, SQL covers missing records and reconciliation, and the AI notes explain how I review and test generated code. A Neo4j specialisation explores shared devices and linked accounts. I use these labs to practise explaining assumptions, investigation evidence, and limitations. They are learning projects, not production systems or claims of professional experience.

Rehearse in your own words. Adjust the timing to your speaking pace rather than memorizing a script you cannot explain.

## 60-second repository explanations

### Python Data Troubleshooting

> This lab explores a transaction CSV with intentional issues such as duplicate IDs, missing customers, malformed amounts, and invalid statuses. The script validates each row, checks IDs against a set, and writes duplicate, invalid-record, and summary reports without changing the source. The sample has 15 rows: 3 pass and 12 are flagged, including one later duplicate occurrence. I would explain the distinction between a duplicated ID and proof of a duplicated financial event, why Decimal still needs a finite-value check, and why retained IDs and reports use memory. The project demonstrates basic automation and investigation reasoning. It does not connect to an ERP system or automatically fix records.

Open [the README](https://github.com/Lyon-Tan/python-data-troubleshooting/blob/main/README.md), [the input](https://github.com/Lyon-Tan/python-data-troubleshooting/blob/main/data/transactions.csv), and [the script](https://github.com/Lyon-Tan/python-data-troubleshooting/blob/main/src/investigate.py). Show the two `TX001` rows and the reviewed [summary example](https://github.com/Lyon-Tan/python-data-troubleshooting/blob/main/output/examples/summary.json).

### SQL Data Investigation

> This lab uses synthetic customers, transactions, and payments in a permissive staging schema. It contains duplicates, missing relationships, split payments, and amount mismatches. The queries investigate each issue using JOINs, grouping, NULL checks, subqueries, and CTEs. My main example is T004: 3,000 cents expected versus 2,800 paid. T009 shows why split payments must be summed before comparing totals. I would explain business grain and why a raw join can multiply values. A verification helper checks selected results in SQLite. This demonstrates reconciliation reasoning, not access to a financial institution's database or production query performance.

Open [the README](https://github.com/Lyon-Tan/sql-data-investigation-lab/blob/main/README.md), [the schema](https://github.com/Lyon-Tan/sql-data-investigation-lab/blob/main/schema.sql), and [queries 4 and 14](https://github.com/Lyon-Tan/sql-data-investigation-lab/blob/main/investigation_queries.sql). Explain the expected result before running a query.

### AI-Assisted Development Notes

> This repository documents how to use AI suggestions while keeping responsibility for the code. It includes a constrained prompt, a review checklist, and a deliberately constructed debugging example. The flawed function adds an ID to a set before checking membership, so A, B, A incorrectly returns three duplicates. The correction checks first and returns one. Five assertions cover representative cases, including missing IDs. I would explain how I choose expected results independently, question unfamiliar APIs and assumptions, and keep secrets out of prompts. This is documentation and a small Python example, not a live AI integration, RAG system, or autonomous agent.

Open [the debugging example](https://github.com/Lyon-Tan/ai-assisted-development-notes/blob/main/debugging-example.md), [the prompt](https://github.com/Lyon-Tan/ai-assisted-development-notes/blob/main/prompt-example.md), and [the checklist](https://github.com/Lyon-Tan/ai-assisted-development-notes/blob/main/validation-checklist.md). Do not describe unchecked checklist boxes as completed validation evidence.

### Neo4j Fraud Investigation

> This lab models fictional users, devices, transactions, and risk events. It contains 22 nodes and 19 relationships. Queries find shared devices, trace a user to flagged transactions, and follow bounded paths between linked accounts. User 1 has two flagged transactions but three events, so DISTINCT counts matter. A shared device is an investigation lead, not proof of a fraud ring. The files passed static syntax and data checks, but live Neo4j execution remains unverified. I would use the lab to discuss graph modelling and explainable paths. It does not implement fraud scoring, AML detection, or a production investigation platform.

Open [the graph model](https://github.com/Lyon-Tan/neo4j-fraud-investigation-lab/blob/main/README.md), [the sample graph](https://github.com/Lyon-Tan/neo4j-fraud-investigation-lab/blob/main/sample_data.cypher), and [queries 6, 7, 9, and 11](https://github.com/Lyon-Tan/neo4j-fraud-investigation-lab/blob/main/investigation_queries.cypher). Explain a path from the source definition if no live database is available; do not imply a live demonstration occurred.

## Common interviewer questions

| Question | Concise answer or evidence to discuss |
| --- | --- |
| Why did you create these projects? | To practise validation, reconciliation, safe AI review, and graph reasoning using small examples I can fully explain. |
| What did AI do, and what did you do? | AI helped draft materials and code. Explain the specific assumptions, corrections, and checks you personally reviewed; do not claim work or understanding you cannot demonstrate. |
| Why a set rather than a list? | Average O(1) membership checks avoid scanning earlier IDs repeatedly. The full program still retains data in memory. |
| Why use Decimal? | Avoid binary floating-point artifacts for decimal amounts, then separately check finiteness and business rules. |
| Does a duplicate ID prove a retry? | No. It is a symptom; source records and logs are needed to validate that hypothesis. |
| Why LEFT JOIN? | Preserve left-side records and expose missing right-side matches. Check a non-nullable right-side key and watch WHERE filters. |
| Why can reconciliation totals be wrong? | Duplicates, join fan-out, NULL amounts, partial payments, and inconsistent scope can distort comparisons. |
| Does AI-generated code passing one example prove correctness? | No. Review assumptions and check edge cases, input contracts, failures, security, and dependencies. |
| Does a shared device prove fraud? | No. Check innocent explanations and independent evidence before drawing a conclusion. |
| Why count DISTINCT transactions in the graph? | One transaction can have multiple events; counting matched rows would overcount transactions. |
| What has actually been validated? | Distinguish Python regression checks, SQLite checks, snippet assertions, and Cypher static checks. State when evidence is from a previous run and never claim live Neo4j execution. |
| What would you improve next? | Select one clearly unimplemented item, explain its acceptance criteria, and describe how you would test it. |

## What not to overclaim

| Avoid saying | Say instead |
| --- | --- |
| I operated SAP/FICO or resolved production incidents. | I practised transferable transaction-data investigation using simulated exports; I have not demonstrated product operations here. |
| I built an enterprise-grade platform. | I built or reviewed small local learning labs with explicit limitations. |
| I detected a real fraud ring or money laundering. | I explored synthetic risk signals and linked accounts; these paths do not prove wrongdoing. |
| I built an AI application, agent, or RAG assistant. | I documented an AI-assisted review workflow; integrations are future projects. |
| My Neo4j queries were tested against a running database. | They passed static checks; live execution remains unverified. |
| The code is secure, scalable, or production-ready. | Explain the checks actually run and the specific untested boundaries. |
| I achieved business savings or detection accuracy. | No real business-impact or detection-performance measurement is supplied by these labs. |
| All four repositories form one integrated system. | They are independent exercises connected by a learning theme. |

## Connecting projects to a job description

Read the actual tasks first. Select two matching requirements, choose one repository as the lead example, and use another only when it adds evidence. Keep a gap statement ready.

| Job-description emphasis | Lead example | Connection and boundary |
| --- | --- | --- |
| Application support, ERP operations, incident troubleshooting | Python, supported by SQL | Show validation and reconciliation; acknowledge the lack of live operations and product integration. |
| Software or backend development | Python, supported by SQL and AI notes | Explain functions, contracts, failure behaviour, and review; no backend service is implemented. |
| AI software development | AI notes, supported by Python | Explain human validation and test design; API integration, RAG, and evaluation platforms are future work. |
| System or business systems analysis | SQL, supported by Python | Translate a discrepancy into data rules and an investigation plan; no real stakeholder requirements project is demonstrated. |
| Data analysis | SQL, supported by Python | Check completeness and totals before interpretation; no BI dashboard or statistical study is supplied. |
| Technology risk or cybersecurity/IAM | AI notes and data-validation examples | Discuss careful handling and assumptions; acknowledge the absence of control assessment, IAM, and security-testing implementations. |
| Fraud, financial crime technology, or graph investigation | Neo4j, supported by SQL | Explain entity links and evidence quality; no real casework, AML system, or validated risk model exists. |

Use this answer structure: **requirement → concrete example → reasoning → validation evidence → limitation → relevant next step**. Do not change the technical facts to fit a role.

For example: "The role mentions reconciliation. My SQL lab compares a transaction's expected amount with summed payment records. T004 exposes a 200-cent shortfall. I can explain how the query handles split payments and blocks duplicate transaction IDs. It is a synthetic SQLite exercise, so I would need to learn your schema, access procedures, and business rules."

## Before each interview

Choose a lead repository, review the exact lines you intend to discuss, and rehearse one normal case and one failure case. Confirm your local setup before offering a live run. Use saved examples when appropriate and identify them as examples. Never expose credentials or real private records during a demonstration.

Review [PORTFOLIO_ROADMAP.md](PORTFOLIO_ROADMAP.md) for the Core/Useful/Bonus role map and the planned next projects. Future work should be introduced with "I would" or "I plan to", not described as an implemented feature.
