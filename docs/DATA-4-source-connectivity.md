\# DATA-4 — Source Connectivity Validation



\## 1. Objective



Validate connectivity to all required Harborline Logistics source systems before developing data ingestion pipelines.



\*\*Ticket:\*\* DATA-4

\*\*Project:\*\* Data Platform Foundation

\*\*Environment:\*\* Local Harborline Lab

\*\*Status:\*\* Connectivity tests completed; evidence review pending.



\## 2. Simulator Build



A Medium dataset build was completed using the Harborline Simulator.



| Metric | Result |

|---|---|

| Build preset | Medium |

| Historical period | 24 months |

| Dataset size | 6.2 GB (Control Center reported) |

| Build duration | \[Enter actual duration] |

| WMS row count | \[Enter verified total] |

| AX 2012 row count | \[Enter verified total] |

| IoT row count | \[Enter verified total] |

| Salesforce row count | \[Enter verified total] |

| Carrier row count | \[Enter verified total] |



\*\*Validation:\*\* Record the completed build's run ID and verify source row counts independently where possible.



\## 3. PostgreSQL Connectivity



Validated connectivity through DBeaver using the read-only `etl\_reader` account.



| Database | Connection | Read test |

|---|---|---|

| WMS (`wms`) | Successful | Successful |

| AX 2012 (`ax2012`) | Successful | Successful |

| IoT (`iot`) | Successful | Successful |



\*\*Connection details:\*\*



\- Host: `localhost`

\- Port: `5433`

\- User: `etl\_reader`

\- Client: DBeaver



Example validation query:



```sql

SELECT current\_database(), current\_user;

```



An additional WMS read test returned 979,824 rows from `wms.order\_header` at the time of testing.



\## 4. Salesforce REST API



Validated authentication and data retrieval using Postman.



\*\*Authentication:\*\* OAuth 2.0 Client Credentials



\*\*Instance URL:\*\*



`
