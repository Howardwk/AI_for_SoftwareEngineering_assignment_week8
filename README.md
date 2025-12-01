# AI Agents Assignment: AutoParts Inc. Case Study

This repository contains my submission for the "AI Agents - Comprehensive Understanding" assignment (Week 8).


## 🤖 Make.com Simulation

I have designed a multi-agent simulation using Make.com to demonstrate the interaction between the Guardian (IoT Monitor), Inspector (Quality Control), and Coordinator (Logistics) agents.

**Scenario Logic:**
1.  **Guardian**: Receives IoT data via Webhook. Routes high vibration/temp to Slack (Maintenance).
2.  **Inspector**: Randomly inspects products passing the Guardian's check.
3.  **Coordinator**: Logs "DEFECTIVE" or "PASSED" status to Google Sheets based on the Inspector's result.

### 🔗 Simulation Access

(https://eu1.make.com/public/shared-scenario/Vaz5KVcJMwt/integration-webhooks-tools-slack)

#### 1. To Run the Simulation (Trigger the Agent)
Use this Webhook URL to send test data to the live agent:

*(Example: `https://hook.us1.make.com/xxxxxxxx?vibration=85&temperature=95&product_id=P-101`)*

#### 2. To View the Scenario Logic (Source Code)
Import the included blueprint file into your own Make.com account:
1.  Create a new Scenario.
2.  Click the **More** (three dots) button at the bottom.
3.  Select **Import Blueprint**.
4.  Upload `Integration Webhooks, Tools, Slack.blueprint.json`.

## 🚀 How to Run
1.  **Trigger the Agent**: Copy the Webhook URL above, paste it into a browser, and hit Enter.
    *   **Test Defect**: `...&vibration=85` (Triggers Slack)
    *   **Test Pass**: `...&vibration=20` (Triggers Google Sheets)
