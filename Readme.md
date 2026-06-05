AI-Driven Compliance Transaction Screening Automation
🚀 Overview
An automated Transaction Screening (TS) system designed to eliminate operational bottlenecks in financial compliance. This project replaces repetitive manual review with an "Intelligent Compliance Layer," successfully processing 1,800+ transactions per day while reducing daily manual review time from 8 hours to under 15 minutes.

🎯 Problem Statement
Operational Bottleneck: Compliance teams were forced to manually review 1,800+ daily transactions out of a 2,000+ volume, leading to high human error risk and fatigue.

Systemic False Positives: Legacy Transaction Screening Systems (TSS) utilized primitive keyword matching, causing "over-screening" where legitimate financial transactions (e.g., dividends, bond redemptions) were repeatedly flagged due to name collisions with sanctioned vessels.

Core System Limitations: The core banking system lacked the flexibility to filter out vessel-based false positives at the source, forcing manual intervention for every single hit.

💡 Solution: The "Hybrid Compliance Engine"
The system functions as an independent processing layer, ensuring efficiency without altering the sensitive core banking infrastructure:

Event-Driven Pipeline:

Orchestrates processing based on core system export cycles (08:00, 10:00, 12:00, 16:00).

Handles variable batch sizes (1,500–2,500 transactions) dynamically without performance degradation.

Deterministic Rule Layer (High-Speed Filtering):

Implemented an automated logic-based filter to instantly clear 100% of vessel-related false positives that match predefined criteria, requiring zero AI compute cost.

AI Contextual Analysis Layer (Semantic Intelligence):

Integrated Claude AI via n8n to perform deep semantic analysis on non-structured SWIFT data.

The engine disambiguates "Financial Settlements" from "Maritime Logistics," ensuring high-risk transactions are identified while clearing legitimate financial activities.

Audit-Ready Architecture:

Every automated decision is logged with a specific "Justification" note, ensuring 100% transparency for internal and external audits.

🛠 Tech Stack
Workflow Orchestration: n8n – Automated data pipeline management.

Intelligence: Claude AI (Anthropic) – Contextual screening and decision support.

Data Processing: JavaScript (n8n Code Nodes) & Batch Processing.

Reliability: Automated "Move-to-Processed" architecture to prevent data duplication.

📈 Impact
Efficiency: Reduced manual review time by 95% (from 8 hours to ~15 minutes).

Scalability: System handles 1,800+ transactions per batch seamlessly.

Accuracy: Eliminated human-induced oversights and standardized the decision-making process.

Audit-Ready: Generated 100% traceable logs for every automatically released transaction.

⚙️ Workflow Overview
Ingestion: Automatic retrieval from the TSS export directory.

Rule-based Filter: Tier-1 deterministic logic for immediate vessel-based clearing.

Semantic Analysis: Tier-2 AI-driven analysis for ambiguous/complex entries.

Final Export: Automated generation of the Compliance Review Report.
