# AI Agent Configuration and Evaluation with Azure AI Foundry

A hands-on experiment configuring and testing three domain-specific AI assistants in **Microsoft Azure AI Foundry**, using a shared **GPT-4.1** model deployment.

## Project overview

This experiment explores how different agent instructions influence the behavior of assistants built on the same foundation model. Three assistants were configured for customer support, healthcare information, and financial education, then tested in the Azure AI Foundry Agents Playground.

**Focus:** Model deployment, agent configuration, prompt engineering, and qualitative evaluation.

## Technology stack

| Component | Used in this experiment |
| --- | --- |
| Platform | Microsoft Azure AI Foundry |
| Foundation model | GPT-4.1 |
| Deployment type | Global Standard (consumption-based) |
| Testing interface | Azure AI Foundry Agents Playground |

## Experiment workflow

### 1. Set up the Azure AI Foundry project

Created an Azure AI Foundry resource and project in an Azure subscription, configured resource settings including region, networking, and identity, and opened the project in the Foundry portal.

**Why:** To provide a central workspace for model deployments and agent configurations.

### 2. Deploy GPT-4.1

Selected GPT-4.1 from the model catalog and deployed it using **Global Standard**.

**Why:** To use one consistent foundation model across all three assistants, making it easier to examine the effects of role-specific instructions.

### 3. Configure three assistants

Created three agents, each connected to the same GPT-4.1 deployment but given different instructions:

| Agent | Purpose | Configuration focus |
| --- | --- | --- |
| Customer Service Chatbot | Customer enquiries | Polite, empathetic responses and clear next steps |
| Healthcare Information Assistant | General health education | Educational information, disclaimers, and referral to licensed professionals |
| Financial Advisor | Financial education | Explaining investment concepts, highlighting risks, and avoiding personalized advice |

The exact instruction text is included in the [technical lab report](Azure_AI_Foundry_Technical_Lab_Report.docx).

### 4. Test in the Agents Playground

Tested each assistant individually with prompts relevant to its assigned role.

**Why:** To examine whether responses followed the configured instructions and to identify potential limitations.

### 5. Compare behavior

Reviewed the responses against these qualitative criteria:

- Relevance and clarity
- Adherence to agent instructions
- Response speed
- Conversational context
- Handling of uncertainty
- Situations requiring human review

## Evaluation scope

The lab documents the testing approach and includes screenshots of agent interactions. **It does not report measured response times, numerical accuracy scores, or benchmark results.** The experiment therefore supports a qualitative discussion of configuration and behavior, not a quantified performance claim.

## Technical takeaway

A single deployed language model can support multiple role-specific assistants through different instruction sets. These instructions influence expected behavior but do not guarantee factual accuracy or safe decisions in sensitive domains.

**Important distinction:** A role-configured conversational assistant is not automatically an autonomous agent with planning, external tools, or persistent memory.

## Documentation

- [Technical Lab Report (Word)](Azure_AI_Foundry_Technical_Lab_Report.docx) — procedure, agent instructions, testing approach, discussion, and Playground screenshots.

## Project context

Completed as a hands-on experiment for **AI Agent Fundamentals with Azure AI Foundry**. This repository documents the configuration and evaluation exercise; it does not include application source code or an independently deployed production service.
undry-agent-experiment

