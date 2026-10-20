# System Architecture

## High-Level Architecture

The system uses n8n as the workflow orchestration layer, with Python/FastAPI providing an analytical backend.

```text
Tender / RFP
     |
     v
Data Ingestion
     |
     v
n8n Workflow
     |
     +----------------------+
     |                      |
     v                      v
Requirement Analysis   Company Capabilities
     |                      |
     +----------+-----------+
                |
                v
        Compliance Matrix
                |
                v
       Python / FastAPI
                |
                v
        Decision Analysis
                |
                v
       Company Ranking
                |
                v
       Approval Routing
          /           \
     Approved        Rejected
        |               |
        v               v
Proposal Workspace   Reporting
        |
        v
Executive Report
