# mcp_model_integration
# Gemini MCP Chatbot - Setup and Usage Guide

## 🚀 Overview

This Spring Boot application integrates Google Gemini AI with a Model Context Protocol (MCP) server to create an intelligent chatbot that can use external tools. The chatbot can perform calculations, get weather information, query databases, and more through the MCP protocol.

## 📋 Prerequisites

- Java 23 or higher
- Maven 3.6+
- Google Gemini API key
- Spring Boot 3.2+

## 🛠️ Setup Instructions

### 1. Clone and Configure

```bash
git clone <your-repo>
cd gemini-mcp-chatbot
```

### 2. Set Environment Variables

```bash
export GEMINI_API_KEY="your-actual-gemini-api-key"
```

Or create `application-local.yml`:
```yaml
gemini:
  api-key: "your-actual-gemini-api-key"
```

### 3. Build and Run

```bash
mvn clean install
mvn spring-boot:run
```

The application will start on:
- Main app: `http://localhost:8080`
- MCP server: `http://localhost:8081/mcp`

## 🔧 Architecture Overview

### Components

1. **GeminiChatService**: Manages AI interactions using LangChain4j
2. **McpClientService**: Handles communication with the MCP server
3. **McpServerController**: Implements the MCP server with tools
4. **ChatController**: REST API endpoints
5. **WebSocket Support**: Real-time chat interface

### MCP Tools Available

- **Weather Tool**: Get weather information for any location
- **Calculator**: Perform mathematical calculations
- **DateTime Tool**: Get current date/time in various formats
- **Database Query**: Mock database operations

## 🌐 API Endpoints

### REST API
