# Agent Framework Journey

## Overview

Creating Agents using Agent Framework - A comprehensive demonstration of building intelligent multi-agent systems with Azure AI Foundry integration.

This repository showcases the power and simplicity of the **Agent Framework** for creating sophisticated multi-agent systems that can intelligently route queries, coordinate responses, and maintain persistent state across sessions. The implementation demonstrates enterprise-ready multi-agent coordination with minimal code complexity while maintaining production-grade reliability and performance.

### Key Features
- 🤖 **Intelligent Multi-Agent System** with automatic query routing
- 🔗 **Native Azure AI Foundry Integration** with portal management
- 💾 **Persistent Agent Registry** for cross-session state management
- ⚡ **Concurrent Processing** for optimal performance
- 🛡️ **Enterprise-Grade Error Handling** and resilience
- 📊 **Built-in Monitoring** and performance analytics

---

📝 **For more details on Agent Framework, refer to my Blog Post:**  
🔗 [Microsoft Agent Framework: The Open Source Engine for Agentic AI Apps](https://singhrajeev.com/2025/10/05/microsoft-agent-framework-the-open-source-engine-for-agentic-ai-apps/)

---

## Prerequisites

Before running the Agent Framework demos, ensure you have the following:

### System Requirements
- **Python 3.8+** installed on your system
- **Azure CLI** installed and configured
- **Azure subscription** with access to AI services
- **Git** for version control (optional)

### Azure Resources Required
- **Azure AI Foundry Project** (recommended) OR **Azure OpenAI Resource**
- **Deployed AI Model** (e.g., GPT-4o, GPT-4, or GPT-3.5-turbo)
- **Appropriate permissions** to create and manage AI resources

### Authentication Setup
- Azure CLI authentication: Run `az login` and ensure you're signed into the correct subscription

## Setup

### Step 1: Creating Virtual Environment

```bash
# Clone or navigate to the repository
cd AgentFramework

# Create virtual environment
python -m venv venv

# Activate virtual environment
# On Windows:
.\venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate
```

### Step 2: Install Dependencies

```bash
# Upgrade pip
python -m pip install --upgrade pip

# Install required packages
pip install python-dotenv
pip install azure-identity
pip install agent-framework
pip install asyncio

# Alternative: Install from requirements file (if available)
# pip install -r requirements.txt
```

### Step 3: Configure Environment Files

1. **Create Environment Configuration**
   ```bash
   # Copy the template
   cp README.env .env
   ```

2. **Configure Azure Settings**
   - Edit the `.env` file with your Azure configuration
   - See [Environment Setup Guide](./README.env) for detailed instructions

3. **Verify Azure Authentication**
   ```bash
   az login
   az account show  # Verify correct subscription
   ```

### Step 4: Azure AI Foundry Project Setup

Follow the detailed setup instructions in our [Setup Guide](./documents/Setup-guide.md) to:
- Create an Azure AI Foundry project
- Configure model deployments  
- Get your project endpoint
- Set up authentication

## Folder/Project Structure

```
AgentFramework/
├── 📄 README.md                           # Main documentation (this file)
├── 🔒 .env                               # Environment configuration
├── � README.env                         # Environment setup template
├── 📁 .gitignore                         # Git ignore configuration
├── 📁 documents/                          # Documentation and guides
│   ├── 📋 Setup-guide.md                 # Complete setup instructions
│   └── 📊 Agent-Framework-vs-Semantic-Kernel-Comparison.md
├── 🐍 python/                            # Python implementations
│   └── 1.ai-foundry-agents/              # AI Foundry agent demos
│       ├── 🎯 agent-framework-demo1.py   # Basic agent setup demo
│       ├── 🤝 multi-agent-demo2.py       # Multi-agent coordination demo
│       ├── 📋 agents_registry.json       # Agent persistence registry
│       └── 📖 README.md                  # Technical implementation docs
└── 🔧 venv/                             # Python virtual environment (excluded from git)
```

## QuickStart

### Overview for Code in `python/1.ai-foundry-agents`

This folder contains the core implementation of multi-agent systems using Microsoft's Agent Framework. The demos showcase progressively advanced concepts from basic agent creation to sophisticated multi-agent coordination.

**📖 [Detailed Technical Documentation](./python/1.ai-foundry-agents/README.md)** - Complete implementation details, architecture diagrams, and code explanations.

### Quick Demo Run

1. **Navigate to the agents directory**
   ```bash
   cd python/1.ai-foundry-agents
   ```

2. **Run Basic Agent Demo**
   ```bash
   python agent-framework-demo1.py
   ```
   - Introduces Agent Framework fundamentals
   - Single agent creation and basic interaction
   - Azure AI Foundry connection setup

3. **Run Multi-Agent Demo**
   ```bash
   python multi-agent-demo2.py
   ```
   - Advanced multi-agent coordination system
   - **🍎 FoodExpertAgent**: Specialized in nutrition analysis and dietary guidance
   - **🍽️ MealPlanningAgent**: Focused on meal suggestions and recipes  
   - **🧠 Intelligent Routing**: Automatic query classification
   - **💾 Persistent Registry**: Cross-session agent tracking (`agents_registry.json`)
   - **🔄 Real-time Coordination**: Seamless agent collaboration

### Sample Interactions

```bash
# Single agent queries
🗣️ "How many calories are in a banana?" → Routes to FoodExpertAgent
🗣️ "Suggest a healthy dinner" → Routes to MealPlanningAgent

# Multi-agent coordination  
🗣️ "both" → "I want to lose weight" → Both agents collaborate
```



## What's Next

### Upcoming Agent Framework Features & Explorations

The Agent Framework roadmap includes revolutionary features that will transform how we build and deploy AI agents. Here are the key areas we'll be exploring in future articles:

#### � **1. Unified SDK + Runtime Integration**
- **Semantic Kernel + AutoGen Convergence**: Best of both worlds in one unified platform
- **Cross-framework Compatibility**: Seamless integration between different agent frameworks  
- **Unified Development Experience**: Single SDK for all agent development needs
- **Migration Pathways**: Easy transition from existing frameworks

#### 📊 **2. Advanced Observability & Durability**
- **OpenTelemetry Integration**: Industry-standard monitoring and tracing baked in
- **Human-in-the-Loop Workflows**: Built-in approval and intervention mechanisms
- **Long-running Durability**: Persistent agent operations across sessions and failures
- **Advanced Debugging**: Deep insights into agent decision-making processes
- **Performance Analytics**: Real-time metrics and optimization recommendations

#### 🔗 **3. Open Standards Support**  
- **OpenAPI Integration**: Standard REST API compatibility for universal connectivity
- **MCP (Model Context Protocol)**: Enhanced context management and sharing
- **A2A (Agent-to-Agent)**: Native inter-agent communication protocols
- **Standards Compliance**: Industry-standard protocols for maximum interoperability

#### 🏢 **4. Enterprise Migration Path**
- **Local → Azure AI Foundry**: Seamless deployment pipeline from development to production
- **Governance Hooks**: Built-in compliance and policy enforcement mechanisms
- **CI/CD Integration**: DevOps-ready agent development lifecycle
- **Security by Design**: Enterprise-grade security controls throughout the pipeline

#### ⚙️ **5. State-of-the-Art Workflow Engine**
- **Advanced Orchestration Patterns**: Both deterministic and dynamic workflow capabilities
- **Agent Orchestration**: Sophisticated multi-agent coordination and task delegation
- **Workflow Orchestration**: Complex business process automation with intelligent routing
- **Conditional Logic**: Smart decision trees and branching workflows

#### 🔌 **6. Enhanced Interoperability** 
- **Built-in Connectors**: Ready-to-use integrations with popular services and APIs
- **MCP + A2A + OpenAPI**: Triple protocol support for maximum compatibility
- **Plugin Architecture**: Extensible connector framework for custom integrations
- **Legacy System Integration**: Bridges to existing enterprise systems

#### 🧠 **7. Advanced Memory Systems**
- **Pluggable Memory Stores**: Support for first-party and third-party storage options
- **Persistent & Adaptive Memory**: Learning and retention capabilities with context evolution
- **Hybrid Approaches**: Combining multiple memory strategies for optimal performance
- **Retrieval Optimization**: Advanced search and context retrieval mechanisms
- **Memory Governance**: Privacy-compliant memory management and data lifecycle controls

#### 🏆 **8. Enterprise Readiness Features**
- **Observability Dashboard**: Comprehensive monitoring and analytics platform
- **Approval Workflows**: Built-in human oversight and governance mechanisms  
- **CI/CD Pipeline Integration**: Automated testing, deployment, and rollback capabilities
- **Long-running Durability**: Enterprise-grade reliability and fault tolerance
- **Hydration Capabilities**: Advanced state restoration and persistence across environments

---

## 🏃‍♂️ Quick Start

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd AgentFramework
   ```

2. **Follow the [Setup Guide](./documents/Setup-guide.md)**

3. **Run the demo**
   ```bash
   cd python/1.ai-foundry-agents
   python multi-agent-demo2.py
   ```

4. **Test intelligent routing**
   - Try: "How many calories in an apple?" 
   - Try: "Suggest a healthy dinner"
   - Try: "both" for comprehensive analysis

---

## 📚 Additional Resources

- **[Agent Framework Documentation](https://docs.microsoft.com/azure/ai-foundry/)**
- **[Azure AI Foundry Portal](https://ai.azure.com/)**
- **[Agent Framework vs Semantic Kernel Comparison](./documents/Agent-Framework-vs-Semantic-Kernel-Comparison.md)**
- **[Setup Guide](./documents/Setup-guide.md)**

---

## License

This project is licensed under the **MIT License**.

For the complete license text, see the [LICENSE](./LICENSE) file.

---

**Built with ❤️ using Microsoft Agent Framework and Azure AI Foundry**