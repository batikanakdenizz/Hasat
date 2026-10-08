# Use-case Point Complexity

The table below declares which technical complexity factors are important in HASAT. Ten of the thirteen factors are considered; each is justified with the part of the proposal it comes from.

| Factor | Description | Considered (Yes/No) | Justification |
|---|---|---|---|
| T1 | Distributed system (Advanced architectural decisions) | Yes | Separate components must work together: a web client, a backend, a machine-learning model and a data pipeline that collects data from external services (Proposed Solution; Project Risks: integration problems). |
| T2 | Response time/performance objectives | Yes | Each recommendation depends on remote calls to external data services; the system must respond in reasonable time and handle slow or unavailable services with caching and fallbacks (Project Risks; Objective 5). |
| T3 | End-user efficiency | Yes | A grower can manage several orchards with different varieties (Persona 2 has three); saved orchards and earlier recommendations are available without entering them again, and goals can be compared quickly for the same orchard (Proposed Solution; Happy Path 2). |
| T4 | Internal processing complexity | Yes | A machine-learning model predicts maturity-index progression from the collected data; goal-specific decision rules turn the prediction into a harvest window; evaluation uses only information available at each forecast issue date (Objectives 2 and 3). |
| T5 | Code reusability | No | — |
| T6 | Easy to install | No | Web application; growers do not install anything. |
| T7 | Easy to use | Yes | The primary persona is a 58-year-old grower with limited digital skills who uses a phone browser; the workflow must take a few simple steps, explain results in plain language and give clear messages for unsupported inputs (Persona 1; Objectives 5 and 6). |
| T8 | Portability to other platforms | Yes | The same workflow must work in a phone browser (Happy Path 1) and a desktop browser (Happy Path 2). |
| T9 | System maintenance (Deployment) | Yes | The web application, the machine-learning model and the data pipeline are deployed and maintained as separate parts; input data must be refreshed regularly and the model re-evaluated or retrained as new observations arrive (Deliverables 1–3). |
| T10 | Concurrent/parallel processing | Yes | Generating a recommendation is a long-running task (data retrieval from several services, data processing, model inference); requests are handled asynchronously as background jobs, and data retrieval from different services can run in parallel. |
| T11 | Security features | Yes | Each grower signs in with an e-mail account; orchard locations and recommendation history are personal data that only their owner can see, and the service is protected against bots and automated abuse (Proposed Solution). |
| T12 | Access for third parties | Yes | Input data are retrieved from third-party data services through their APIs, and the orchard location is selected on a third-party map service (Happy Path 1). |
| T13 | End-user training | No | Designed to be used without training; a short user guide is provided (Deliverable 4). |
