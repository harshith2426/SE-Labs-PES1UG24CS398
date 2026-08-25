# Airport Lost Luggage Claim & Tracking Portal - UML Use-Case Diagram

## Actors

- **Passenger** - submits a lost-baggage claim and views the claim status and scan timeline.
- **Baggage Service Agent** - reviews a claim and updates its recovery status.
- **Baggage Scan System** - an external system that provides bag-tag scan information from transit hubs to support cross-referencing.

## Use Cases

| ID | Use Case | Primary Actor | Requirement Alignment |
| --- | --- | --- | --- |
| UC-01 | Submit Lost-Baggage Claim | Passenger | FR-002 |
| UC-02 | Cross-Reference Scan Logs | System (included during claim submission) | FR-001 |
| UC-03 | View Claim Status & Scan Timeline | Passenger | FR-003 |
| UC-04 | Review & Update Claim Status | Baggage Service Agent | FR-004 |
| UC-05 | Initiate Compensation Workflow | System (conditional extension) | FR-005 |
| UC-06 | Generate Recovery Alert | System (conditional extension) | FR-001 |

## Relationships

- **UC-01 <<include>> UC-02:** each submitted claim is cross-referenced with the luggage scan logs.
- **UC-06 <<extend>> UC-02 [matching scan found]:** a recovery alert is generated only when the cross-reference identifies a match.
- **UC-05 <<extend>> UC-04 [claim meets compensation conditions]:** compensation processing starts only when an updated claim meets the configured conditions.
- **Baggage Scan System - UC-02 association:** the portal obtains baggage scan information from the external system when cross-referencing scan logs.

NFR-001 and NFR-002 constrain the implementation of the relevant use cases rather than being modelled as separate use cases.
