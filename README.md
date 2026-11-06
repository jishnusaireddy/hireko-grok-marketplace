# Hireko AI Recruiter — xAI Grok Plugin

Official Grok plugin for **Hireko AI Recruiter**: candidate interview analytics, automated AI interview link generation, candidate match scorecards, and multi-tenant talent search.

---

## Capabilities

- 📊 **Candidate Pipeline & Analytics**: Fetch candidate counts, status breakdowns (completed vs. pending), and interview outcomes directly within Grok.
- 🔗 **AI Interview Generation**: Create personalized interview links for candidates across all supported job funnels.
- 🎯 **Candidate Search & Scoring**: Retrieve semantic match scores and evaluation details for candidates evaluated by Hireko AI.
- 🔐 **Zero-Config Multi-Tenant Auth**: Direct local auth proxy (`bundle.mjs`) with seamless browser login. Recruiters simply enter their tenant credentials securely.

---

## Installation in Grok

### 1. From the Grok Plugin Marketplace (Recommended)
Search for **Hireko AI Recruiter** in Grok Build and click **"Install"**.

### 2. Manual Installation
Clone this repository into your Grok plugins directory:
```bash
git clone https://github.com/jishnusaireddy/hireko-grok-marketplace.git
```

---

## Starter Prompts

Once installed, try asking Grok:
- *"Show candidate interview counts and pass rates for my team"*
- *"Create a candidate interview link for Senior Backend Engineer"*
- *"Search candidates for Java Spring Boot and Microservices"*

---

## Engine & Architecture
- **Engine**: Local Stdio MCP Router (`node ${GROK_PLUGIN_ROOT}/bundle.mjs serve`)
- **Downstream Tools**: 10 Recruiter Facade business tools
- **Authentication**: Multi-tenant AWS Cognito via browser device flow
