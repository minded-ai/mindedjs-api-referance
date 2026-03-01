# Changelog

All notable changes to MindedJS will be documented in this file.

## [3.1.42] - 2026-03-01

### Fixed

- **Validate Command**: Removed unnecessary logs from validate command.

## [3.1.41] - 2026-02-26

### Added

- **Lambda Handler Security**: Enhanced Lambda handler with isolated user code execution to prevent access to AWS credentials

## [3.1.40] - 2026-02-16

### Added

- **Document Processing**: Added configurable quality settings (standard, advanced); advanced mode is default.

## [3.1.39] - 2026-02-16

### Added

- **App Development**: Added support for copilot app development.

## [3.1.38] - 2026-02-12

### Fixed

- **Dashboard Message**: Fixed dashboard message payload parsing.

## [3.1.37] - 2026-02-11

### Added

- **Placeholder Resolution**: Support array pluck — `{tools.Node.messages.subject}` now extracts the property from every item, returning an array of values.

## [3.1.36] - 2026-02-10

### Fixed

- **App Tool Schema**: Fixed nested array/object types parsing.

## [3.1.35] - 2026-02-09

### Fixed

- **Flow Schema**: Added `replyToSource` validation to `AppTriggerNodeSchema`..

## [3.1.34] - 2026-02-05

### Fixed

- **Reply To Source (Slack)**: Fixed trigger payload parsing.

## [3.1.33] - 2026-02-05

### Fixed

- **Interfaces**: Add support for AI message auto-reply to trigger source.

## [3.1.32] - 2026-02-04

### Added

- **Knowledge Base RAG support**: Added first-class Knowledge Base RAG support with new retrieval functions (retrieveFromKnowledgeBase, retrieveAndGenerateFromKnowledgeBase), automatic default RAG context injection from platform config with memory-based filtering, deprecated legacy vector store API, and expanded documentation.

## [3.1.31] - 2026-02-03

### Added

- **App Tools, Triggers**: Support version.

## [3.1.30] - 2026-02-02

### Added

- **Triggers**: Support trigger output schema

## [3.1.29] - 2026-02-03

### Fixed

- **AppTool Output Parsing**: Fixed appTool response extraction to unwrap nested response structures from providers that wrap responses in `{ status: "Success", data: {...} }` format.

## [3.1.28] - 2026-01-28

### Changed

- **Documentation**: Improved Mindly low-code editor docs for flows and nodes.

## [3.1.27] - 2026-01-27

### Fixed

- **Validate Command**: Fixed validate command to check if outputSchema is an array.

## [3.1.26] - 2026-01-20

### Added

- **Agent Pods Support**: Added support for running agent in pods.
  - Added `BRANCH_NAME` environment variable for dashboard server connection.
  - Added `SKIP_INIT` environment variable for loading agent files without initialization.
  - Added `id` property to `Flow` type
  - Exported `Playbook` type

## [3.1.25] - 2026-01-13

### Added

- **RPA debug**: Added support for RPA debug in Copilot.

## [3.1.24] - 2026-01-09

### Added

- **Improved Browser Billing Metrics**: Adding more details to browser billing data.

### Changed

- **Proxy Configuration**: Refactored proxy parameters to unified `ProxyConfig` (replacing `ProxyType` and discrete proxy fields) across nodes, tools, types, and exports.

## [3.1.23] - 2026-01-07

### Added

- **RPA Session Persistence**: Use latest cookie

## [3.1.22] - 2026-01-06

### Added

- **RPA Session Persistence**: Added `persistSession` boolean option to RPA tools for automatic browser state persistence across executions using cloud storage.
- **Output Schema**: Added optional `output` property to tools for defining and validating tool return values using Zod schemas (variable must be named `outputSchema`).

## [3.1.21] - 2026-01-06

### Added

- **Proxy Support**: Added support custom proxy server in RPA tool.

## [3.1.20] - 2026-01-05

### Fixed

- **Connection**: Fixed reconnecting on invalid token.

## [3.1.19] - 2026-01-04

### Added

- **Validate CLI Command**: Now compiling graph as part of the validate command.

## [3.1.18] - 2026-01-01

### Added

- **Type Coercion**: Added Zod type coercion support for parameter compilation.

## [3.1.17] - 2026-01-01

### Fixed

- **Placeholders**: Fixed compilation of Minded tools placeholders

## [3.1.16] - 2025-12-31

### Added

- **LLM**: Added support for verbosity, reasoning control

## [3.1.15] - 2025-12-30

### Added

- **Multi-Document Parsing**: Added support for multi-document parsing and extraction, enabling processing of multiple documents in a single operation.

## [3.1.14] - 2025-12-30

### Added

- **Browser Session**: Added execution time to browser session logs.

## [3.1.13] - 2025-12-30

### Added

- **Manual Trigger**: Added support for manual trigger in flow YAML validation.

## [3.1.12] - 2025-12-29

### Fixed

- **Checkpoint Restore**: Fixed checkpoint restore for deployed agents.

## [3.1.11] - 2025-12-28

### Fixed

- **Document Parsing**: Fixed parsing of image documents with Hebrew characters.

## [3.1.10] - 2025-12-25

### Fixed

- **Proxy Configuration**: Fixed proxy configuration in RPA tools.

## [3.1.9] - 2025-12-23

### Added

- **CLI**: Added support for invoking the agent using the CLI "npx minded run <json_input>".

## [3.1.8] - 2025-12-22

### Fixed

- **RPA**: Extended logs & screenshots capture for RPA tools.

## [3.1.7] - 2025-12-23

### Added

- **Document Processing**: New utility methods and enum for parsing and extracting structured data
  - `parseDocumentAndExtractStructuredData` - Parse documents with optional AI-powered extraction
  - `parseDocument` - Parse documents and extract raw text
  - `extractStructuredDataFromString` - Extract structured data from parsed text
  - `DocumentProcessingMode` enum for managed/local processing modes

### Changed

- **Document Processing Tool**: Updated to support structured output via node's `outputSchema` and `prompt` properties
- **Documentation**: Improved document processing documentation with clearer examples and function signatures

## [3.0.7] - 2025-12-22

### Added

- **Trigger Type**: Added support for trigger type interface in flow YAML.

## [3.0.6] - 2025-12-18

### Added

- **CLI**: Added validate command to validate a flow YAML file

## [3.0.5] - 2025-12-16

### Added

- **Docs**: Add Security Architecture document

## [3.0.4] - 2025-12-16

### Added

- **Playbooks**: Added support for markdown prompt in playbooks.

## [3.0.3] - 2025-12-16

### Fixed

- **Extraction**: Fixed extraction tool to avoid excessive type depth inference.

## [3.0.2] - 2025-12-16

### Added

- **Minded Metadata**: Added minded metadata to adapt thinking messsage in the platform.

## [3.0.1] - 2025-12-15

### Fixed

- **Versioning**: Version bump

## [3.0.0] - 2025-12-14

### Added

- **Migrated thinking node to prompt node**: Migrated thinking node to prompt node with sendAiMessage: false.

## [2.0.47] - 2025-12-09

### Fixed

- **SDK Socket errors handling**: Fixed SDK socket error handling

## [2.0.46] - 2025-12-09

### Added

- **Managed Document Processing**: Added managed/local modes via `DOCUMENT_PROCESSING_MODE` with backend-driven upload/parse workflow, `documentSource` parameter, and built-in AI extraction.

### Changed

- **App Tool Resolution**: App tools now resolve by `actionKey` instead of `displayName`.
- **Playbook Compilation**: Playbooks compile once and are included in system message for tool nodes.
- **Error Handling**: Enhanced explicit error handling across Zendesk, timers, voice/retell, interrupts, checkpoint saver, and flow loading. `awaitEmit` returns raw responses with explicit error checks.

## [2.0.45] - 2025-12-08

### Added

- **Docs**: Improved docs

## [2.0.44] - 2025-12-02

### Added

- **Output Schema Suppoer**: Added support to output schema in Thinking node and tokenize values in nodes prompt\input.

## [2.0.43] - 2025-12-02

### Added

- **Storage support**: Added support for storage that can be used to store data between sessions.

## [2.0.42] - 2025-12-01

### Added

- **RPA sessions debugging**: Added failure artifacts for debugging in Mindly.

## [2.0.41] - 2025-11-26

### Added

- **Proxy Support**: Added support & cloud mode for proxy in RPA tools.

## [2.0.40] - 2025-11-25

### Added

- **Thinking Node**: Added support for thinking node that can be used to process logic without calling a tool or generating an AI message.

## [2.0.39] - 2025-11-20

### Added

- **CAPTCHA Tool**: Added support for solving CAPTCHA resolution in RPA tools.

## [2.0.38] - 2025-11-20

### Added

- **Tool Parameter Overrides in Flows**: Added support for overriding tool input parameters per node in flow YAML with runtime schema filtering, AI-bypass when all params are provided, and updated documentation and tests. Flow engine now merges YAML overrides, skips LLM calls as appropriate, and improved system message construction; added end-to-end tests for override scenarios.

## [2.0.37] - 2025-11-19

### Added

- **Agent Initialization**: Added baseUrl to agent initialization error logging

## [2.0.36] - 2025-11-19

### Added

- **Docs**: Improved docs

## [2.0.35] - 2025-11-16

### Added

- **RPA tool**: Added support for RPA tool that supports realtime screenshot capture and logs upload

## [2.0.34] - 2025-11-13

### Added

- **TURN_END Event**: New lifecycle event that fires when a trigger invocation completes, just before returning the result. Allows customizing the return value from the `invoke` function.
  - Emitted with final agent state after execution completes
  - Handlers can return `any` to customize the response
  - Enables response transformation, metadata addition, and custom return formats
  - Works for both qualified and disqualified triggers
  - See [Events documentation](../docs/sdk/events.md#turn_end) for usage examples

## [2.0.33] - 2025-11-09

### Fixed

- **Checkpoint Saver**: Increased timeout to 30 seconds for checkpoint operations

## [2.0.32] - 2025-11-06

### Added

- **Schedule**: Added schedule trigger

## [2.0.31] - 2025-11-05

### Added

- **Previous Node Result Access**: Enhanced logical condition edges with `lastNodeResult` variable for routing based on previous node results
  - Access tool results via `lastNodeResult` object in logical conditions (e.g., `lastNodeResult.status === 'success'`)
  - Access operator output schema results for conditional routing (e.g., `lastNodeResult.result === 1`)
  - Enables success/failure routing patterns after tools and operators
  - Comprehensive documentation with examples for both tools and operators

### Fixed

- **Browser Task Screenshot**: Fixed sreenshot timeout

## [2.0.30] - 2025-11-03

### Added

- **CLI**: Added support for direct tool execution
- **Browser Tasks**: Exported withBrowserSession tool for RPA automation

## [2.0.29] - 2025-11-02

### Fixed

- **Browser Task Screenshot**: Fixed timeout to fail gracefully

## [2.0.28] - 2025-11-02

### Fixed

- **Browser Task Screenshot**: Added timeout to screenshot to prevent hang

## [2.0.27] - 2025-11-02

### Added

- **Platform LLM Configuration**: Support for organization-level LLM configuration with automatic conversion from platform settings
- **Dynamic Configuration Updates**: Agent now reloads resources when configuration changes are detected from the platform

## [2.0.26] - 2025-10-27

### Added

- **Infra**: Support EKS deployment

## [2.0.25] - 2025-10-22

### Added

- **Browser Tasks**: Added S3 screenshot capture and history logs upload on each browser step
- **Local Browser Management**: Support for multiple Chrome instances with CDP-based cookie persistence and dynamic port allocation
- **Configuration**: Extended browser task options with screenshot config and tool call tracking

## [2.0.24] - 2025-10-14

### Fixed

- **Invocation start event**: Now fires invocation event only on qualified triggers

## [2.0.23] - 2025-10-14

### Added

- **socket reconnect**: Added minded socket auto reconnect retries

## [2.0.22] - 2025-10-13

### Added

- **tacking events**: Added trackAnalyticsEvent method to track events

## [2.0.21] - 2025-10-04

### Changed

- **Browser Use**: Added local run download files to tool response

## [2.0.20] - 2025-10-01

### Changed

- **Integration nodes**: Added support to pass variables into integration node parameters

## [2.0.19] - 2025-09-29

### Changed

- **Browser Use**: Changed OTP_SECRET to TOTP_SECRET

## [2.0.18] - 2025-09-22

### Fixed

- **Browser Use**: Fixed a bug where the browser task would not be killed if the local browser process stopped running

## [2.0.17] - 2025-09-18

### Changed

- **CDP State Structure**: Refactored CDP-related state properties (`cdpUrl`, `cdpLiveUrl`, `cdpSessionId`) into a single `cdp` object with `url`, `liveUrl`, and `sessionId` properties for better organization

### Fixed

- **CDP Initialization Check**: Fixed conditional checks to properly verify CDP URL existence using `state.cdp?.url` instead of just checking the object

## [2.0.16] - 2025-09-18

### Changed

- **RPA node**: Rpa node can create cdp session no if not existing already

## [2.0.15] - 2025-09-17

### Added

- **Classifier**: Added retry support for classifier

## [2.0.14] - 2025-09-16

### Fixed

- **Local Operator Setup**: Fixed local operator setup script

## [2.0.13] - 2025-09-16

### Fixed

- **Browser Use**: Fixed browser task run node to compile the prompt with env variables after the tool call

## [2.0.12] - 2025-09-16

### Fixed

- **Browser Use**: Added support for OTP generation tool in operator

## [2.0.11] - 2025-09-16

### Fixed

- **Browser Use**: Moved browser operator mode to env variable instead of node configuration

## [2.0.10] - 2025-09-15

### Added

- **Rpa node**: Added Rpa node that can perform different actions like click, goto, type on cdp sessions

## [2.0.9] - 2025-09-14

### Fixed

- **Browser Use**: Fixed local browser session

## [2.0.8] - 2025-09-14

### Fixed

- **Browser Use**: Support local browser session

## [2.0.7] - 2025-09-11

### Fixed

- **Run locally**: Fixed configuration to run fully locally

## [2.0.6] - 2025-09-09

### Fixed

- **Logs**: Fix agent crash logs and monitoring

## [2.0.5] - 2025-09-09

### Fixed

- **Browser Use**: Support closing remote browser sessions. Fix run-from-here + scenarios for lambda

## [2.0.4] - 2025-09-08

### Changed

- **Interrupts**: Fixed a bug where disqualified invocation resulted sometimes in poor handling of the triggers queue

## [2.0.3] - 2025-09-07

### Added

- **Stability**: Added retries to agent<>Minded platform connections

## [2.0.2] - 2025-09-03

### Fixed

- **Browser Use**: Fixed error handling in browser use task

## [2.0.1] - 2025-09-03

### Changed

- **Prompt node**: Prompt node can now make multiple call tools in a row, and will always finish with an AI message

## [2.0.0] - 2025-09-03

### Changed

#### Breaking Changes

#### State Updates Now By Reference

**BREAKING: Complete overhaul of state management - state is now updated by reference instead of returning new state objects**

This major version introduces a fundamental change to how state is managed throughout the MindedJS SDK. State is now updated in place (by reference) rather than returning partial state updates.

##### Key Changes:

1. **Tools**: No longer return `state` in their response
   - **Before (v1.x)**: Tools returned `{ state?, result? }` with partial state updates
   - **After (v2.0)**: Tools directly modify state in place and only return `{ result? }`
   - State modifications are done directly: `state.memory.field = value`

2. **Event Handlers**: Lifecycle hooks like `TRIGGER_EVENT` also update state by reference
   - **Before (v1.x)**: Returned state updates that were merged
   - **After (v2.0)**: Directly modify the provided state object

3. **No More Partial Updates**: State is no longer partial - you work with the complete state object

##### Migration Guide

###### Updating Tools

**Before (v1.x):**

```typescript
const myTool: Tool<typeof schema, Memory> = {
  name: 'myTool',
  description: 'My tool',
  input: schema,
  execute: async ({ input, state, agent }) => {
    // Process logic
    const result = await processData(input);

    // Return partial state update
    return {
      state: {
        memory: {
          lastAction: input.action,
          processedData: result.data,
        },
      },
      result: 'Success',
    };
  },
};
```

**After (v2.0):**

```typescript
const myTool: Tool<typeof schema, Memory> = {
  name: 'myTool',
  description: 'My tool',
  input: schema,
  execute: async ({ input, state, agent }) => {
    // Process logic
    const result = await processData(input);

    // Update state directly by reference
    state.memory.lastAction = input.action;
    state.memory.processedData = result.data;

    // Only return result, no state
    return {
      result: 'Success',
    };
  },
};
```

###### Updating Event Handlers

**Before (v1.x):**

```typescript
agent.on(events.TRIGGER_EVENT, async ({ triggerName, triggerBody, state }) => {
  if (triggerName === 'userMessage') {
    return {
      isQualified: true,
      state: {
        memory: {
          conversationStarted: true,
          sessionId: triggerBody.sessionId,
        },
      },
      messages: [new HumanMessage(triggerBody)],
    };
  }
});
```

**After (v2.0):**

```typescript
agent.on(events.TRIGGER_EVENT, async ({ triggerName, triggerBody, state }) => {
  if (triggerName === 'userMessage') {
    // Update state directly by reference
    state.memory.conversationStarted = true;
    state.memory.sessionId = triggerBody.sessionId;
    state.messages.push(new HumanMessage(triggerBody));

    return {
      isQualified: true,
      // No state in return value
    };
  }
});
```

###### Error Event Handler Updates

**Before (v1.x):**

```typescript
agent.on(events.ERROR, async ({ error, state }) => {
  return {
    throwError: false,
    state: {
      memory: {
        ...state.memory,
        errorRecovered: true,
        lastError: error.message,
      },
    },
  };
});
```

**After (v2.0):**

```typescript
agent.on(events.ERROR, async ({ error, state }) => {
  // Update state directly
  state.memory.errorRecovered = true;
  state.memory.lastError = error.message;

  return {
    throwError: false,
    // No state in return value
  };
});
```

##### Important Notes

- This is a breaking change that requires updating all tools and event handlers

## [1.0.150] - 2025-08-31

### Fixed

- **zendesk interface**: Fixed setCustomFields interface

## [1.0.149] - 2025-08-31

### Fixed

- **Tool calling log**: Fixed the error log for tool calling inside prompt nodes

## [1.0.148] - 2025-08-28

### Fixed

- **State Update**: Fix logical cond state upadte, it will improve runtime speed as well

## [1.0.147] - 2025-08-28

### Fixed

- **logs**: Fixed logs loading

## [1.0.146] - 2025-08-28

### Added

- **logs**: Added sessionId for critical logs in edge router and prompt node

## [1.0.145] - 2025-08-28

### Added

- **timers**: State is not available in the timers handler callback

## [1.0.144] - 2025-08-27

### Fixed

- **State initialization**: Fixed a bug related to state initialization for deployed agents

## [1.0.143] - 2025-08-26

### Fixed

- **timers**: Fixed a bug related to timers

## [1.0.142] - 2025-08-25

### Fixed

- **Logs**: Fixed messages duplications

## [1.0.141] - 2025-08-25

### Changed

- **Logs**: Use synchronous stdout for logs

## [1.0.140] - 2025-08-21

### Changed

- **Events API**: All agent events now consistently take and return state objects for better state management
- **Flow Control**: Renamed `overrideStartFromNodeId` to `goto` for jumping to specific nodes in tools and events

### Added

- **Environment Variables**: Added `MINDED_CLOUD` environment variable for runtime environment detection
- **Webhook Headers**: Request headers are now available through `triggerBody.headers` for webhook triggers

## [1.0.139] - 2025-08-21

### Changed

- **Minded Connection**: Disconnect socket connection when lambda finishes

## [1.0.138] - 2025-08-21

### Changed

- **Agent Logs**: Style updates for logs

## [1.0.137] - 2025-08-19

### Changed

- **Minded Connection**: Changed transports to websocket

## [1.0.136] - 2025-08-19

### Changed

- Improved error logging when connection fails

## [1.0.135] - 2025-08-17

### Added

- **Data Extraction Tool**: New `minded-extraction` library tool for AI-powered data extraction from unstructured text
  - Supports structured extraction with Zod schemas
  - Automatic use of LLM's `withStructuredOutput` when available for guaranteed schema compliance
  - Fallback to JSON parsing with validation and retry logic
  - Configurable strict/non-strict modes for flexibility
  - Built-in validation and error handling with customizable retry attempts

## [1.0.134] - 2025-08-14

### Fixed

- Fixed platform message parsing

## [1.0.133] - 2025-08-14

### Added

- **Vectore Store Query API**: New `agent.getDocumentsFromDB()` method for querying indexed document collections
  - Query knowledge bases and indexed collections directly from agent code
  - Support for filtering, scoring thresholds, and result limits
  - Configurable timeout for long-running queries
  - Returns `Document[]` with pageContent and metadata

- **Custom Session ID Parser**: Added `parseSessionIdFromTrigger` option to Agent constructor
  - Allows custom extraction of session IDs from incoming triggers
  - Defaults to `triggerBody.sessionId` if not provided
  - Enables flexible session management across different trigger sources

### Improved

- **Error Handling**: Improved browser task error handling

## [1.0.131] - 2025-08-12

### Improved

- **Error Handling**: Standardized error handling across the SDK
  - Changed all `catch (error)` to `catch (err)` to properly utilize Pino's error serializer

## [1.0.130] - 2025-08-10

### Added

- **LLM Debug Callback Handler**: Added `LLMDebugCallbackHandler` for debugging LLM interactions in real-time
  - Inspect messages before they're sent to the LLM
  - Set debugger breakpoints to pause execution and examine conversation state
  - Log LLM responses and token usage
  - Capture and debug LLM errors
  - Extends LangChain's BaseCallbackHandler with all callback methods available
  - ESLint rules disabled for debugging purposes (no-debugger, no-unused-vars)

- **Tool Execution API**: Enhanced tool execution system with browser automation support
  - New `ToolExecutor` class in `src/platform/toolExecutor.ts` for standalone tool execution
  - Tools must explicitly opt-in with `allowExecutionRequests: true` flag for security
  - Support for `cdpUrl` parameter in state for browser automation tools
  - Browser-use tools can access Chrome DevTools Protocol URL via `state.cdpUrl`
  - Enables custom browser automation using Playwright or similar libraries within tools
  - Automatic state management and updates after tool execution
  - Request-based tool execution via socket connections

- **CDP URL State Annotation**: Added `cdpUrl` field to LangGraph state annotations
  - Available in `state.cdpUrl` during browser-use tool execution
  - Allows tools to connect directly to browser instances for advanced automation
  - Automatically injected when browser-use requests tool execution
  - Enables hybrid automation combining MindedJS tools with direct browser control

### Documentation

- Added comprehensive LLM debugging guide in `docs/sdk/debugging.md`
  - Step-by-step instructions for using `LLMDebugCallbackHandler`
  - Examples of basic and advanced debugging techniques
  - Custom debug handler implementation examples
  - IDE debugging workflow documentation

## [1.0.129] - 2025-08-07

### Added

- **Added support to run operator nodes on prem**

## [1.0.128] - 2025-08-07

### Added

- **Browser task output schema**: Added support for output schema in browser task nodes.

## [1.0.127] - 2025-08-07

### Fixed

- **fixed a bug with document processing**

## [1.0.126] - 2025-08-07

### Fixed

- **fixed a bug where the wrong message ids where used for the history steps**

## [1.0.125] - 2025-08-04

### Fixed

- **Scenarios in non voice agents**
- **Bullet points in playbooks**
- **Add messages from tool result**
- **Get state outside agent lifecycle**

## [1.0.124] - 2025-08-3

### Added

- **Import types**: Added some type exports.

## [1.0.123] - 2025-08-3

### Added

- **Handle Interruptions**: Added support for managing interruptions in critical nodes such as prompt nodes and tool nodes.

## [1.0.122] - 2025-07-31

### Added

- **Enhanced Prompt Placeholders**: Prompt placeholders now support accessing memory values with `{memory.x}` syntax and system values with `{system.currentTime}` where currentTime returns `new Date().toISOString()`
- **Model calls**: Added support for placeholders. Removed applying memory to model calls.
- **Genesys escalation tool**: Added support for escalating voice calls to a specialist for Genesys integration.

## [1.0.121] - 2025-07-31

### Fixed

- **Prompt Construction**: Fixed issue with prompt construction to properly handle placeholders and template rendering
- **Jump to node**: Fixed issue with jump to node not working when used in a flow.
- **Memory in init**: Fixed issue with memory not being applied to state in graph init.

## [1.0.120] - 2025-08-01

### Added

- **Multi-Environment Support**: Added support for deploying agents to sandbox, staging and production environments

## [1.0.119] - 2025-07-31

### Fixed

- **Browser task node**: Increased the timeout on browser task execution

## [1.0.118] - 2025-07-31

### Added

- **TRIGGER_EVENT State Parameter**: Improved the browser-task infrastructure, now managed by minded.

## [1.0.117] - 2025-07-30

### Added

- **TRIGGER_EVENT State Parameter**: The `AgentEvents.TRIGGER_EVENT` handler now receives the current state (including memory, messages, history, etc.) as an optional parameter. This allows handlers to access existing session state when processing triggers, enabling better session continuity and avoiding re-initialization issues.
  ```typescript
  agent.on(AgentEvents.TRIGGER_EVENT, async ({ triggerName, triggerBody, sessionId, state }) => {
    // Access existing state including memory
    if (state?.memory?.isInitialized) {
      // Continue with existing session state
    }
  });
  ```

## [1.0.116] - 2025-07-30

### Added

- **Interface Trigger Node**: Added support for interface trigger nodes that can be used to trigger flows from external interfaces

## [1.0.115] - 2025-07-30

### Added

- **Interface Trigger Node**: Added support for interface trigger nodes that can be used to trigger flows from external interfaces

## [1.0.114] - 2025-07-30

### Added

- **Interface Trigger Node**: Added support for interface trigger nodes that can be used to trigger flows from external interfaces

## [1.0.113] - 2025-07-30

### Added

- **Secrets Management**: Added support for loading secrets from platform and injecting them into environment variables

## [1.0.112] - 2025-07-29

### Added

- **Scenarios**: Added support for scenarios in the platform.

## [1.0.111] - 2025-07-27

### Added

- **CLI Lambda Handler Generation**: Fix CLI command `generate-lambda-ts-handler` that generates a TypeScript Lambda handler

## [1.0.110] - 2025-07-28

### Added

- **Voice Escalation**: Added support for voice escalation for Genesys integraiton.
- **Voice Session Update**: Added support for updating the memory outside agent lifecycle.

## [1.0.109] - 2025-07-27

### Added

- **Logical Condition Debugging**: Added `ON_LOGICAL_CONDITION` and `ON_LOGICAL_CONDITION_RESULT` events to provide transparency when debugging logical conditions locally. Backend developers can now listen to these events to log condition evaluation, inspect state, track performance, and handle errors during agent development.

## [1.0.108] - 2025-07-27

### Fixed

- **Image Resizing Tool**: Removed to reduce package size

## [1.0.107] - 2025-07-27

### Added

- **Retell Support**: Export support for Retell voice integration, enabling voice calls through the Retell platform with `retellCall` and `retellGetCall` methods

## [1.0.106] - 2025-07-27

### Added

- **Retell Support**: Added support for Retell voice integration, enabling voice calls through the Retell platform with `retellCall` and `retellGetCall` methods

## [1.0.105] - 2025-07-27

### Fixed

- **Image Resizing Tool**: Document processing image resizing package (Sharp) is now optional

## [1.0.104] - 2025-07-26

### Added

- **Library Tools Support**: Introduced support for library tools that can be reused across different agents and flows, providing a standardized toolkit for common operations.

- **Parse Document Tool**: Added new `parseDocument` tool for processing and extracting data from various document formats including PDFs, images, Word documents, and more.
  - Supports multiple input sources: URL, file path, buffer, or string content
  - Flexible extraction modes: raw text, structured data with Zod schema, or unstructured data with custom prompts
  - Configurable parameters that can be predefined in flow configuration
  - Automatic session tracking and error handling with structured logging
  - Memory integration for tracking document processing history

## [1.0.103] - 2025-07-21

### Added

- **Browser Task Agents**: use the node display name for the browser task tool name.

## [1.0.102] - 2025-07-21

### Added

- **Browser Task Agents**: Added support for browser task automation agents that can interact with web pages, perform actions like clicking, typing, and navigation, and extract information from web content.

## [1.0.101] - 2025-07-20

### Added

- **Browser Task Agents**: Introduced cloud-based browser task automation, eliminating the need for local installations.

## [1.0.100] - 2025-07-20

### Added

- **Browser Tasks Agents**: Added support for browser task automation agents that can interact with web pages, perform actions like clicking, typing, and navigation, and extract information from web content.

## [1.0.99] - 2025-01-20

### Added

- **Parallel LLM Requests**: New feature to reduce latency by sending multiple identical requests and using the fastest response. Can reduce latency by 30-50% in scenarios with variable network conditions.
  - **Configuration-Based Approach**: All LLM providers (`MindedChatOpenAI`, `AzureChatOpenAI`, `ChatOpenAI`) now support `numParallelRequests` and `logTimings` configuration in `minded.json`
  - **Automatic Parallel Wrapping**: The SDK automatically applies parallel functionality when parallel options are detected in configuration
  - **Backend Processing for MindedChatOpenAI**: Parallel requests are handled efficiently on the Minded platform backend
  - **Manual Control**: Added `createParallelWrapper()` function for advanced use cases requiring direct LLM instance control
  - **Comprehensive Documentation**: Updated docs and examples prioritizing configuration-based approach over manual instantiation
  - Includes detailed timing logs when `logTimings` is enabled

### Added

- **Browser Tasks Agents**: Added support for browser task automation agents that can interact with web pages, perform actions like clicking, typing, and navigation, and extract information from web content.

## [1.0.97] - 2025-07-20

### Added

- **Browser Tasks Agents**: Added support for browser task automation agents that can interact with web pages, perform actions like clicking, typing, and navigation, and extract information from web content.

## [1.0.86] - 2025-07-08

### Fixed

- **Playbook Parsing**: Fixed issue with playbook parsing

## [1.0.78] - 2025-01-31

### Added

- **INIT Event**: Added support for INIT event that is emitted when the agent's graph state is initialized. This event provides access to the full initial agent state including session information, memory, and session type. Learn more about events [here](https://docs.minded.ai/platform/events).

### Changed

- **Playbooks Auto-Compilation**: Playbooks are now automatically compiled to markdown format for improved readability and documentation generation.

### Fixed

- **Multiple Flows**: Fixed issue with multiple flows handling to ensure proper flow execution and state management.

## [1.0.70] - 2025-07-02

### Added

- **Jump To Nodes**: Added support for jump to nodes. Learn more about jump to nodes [here](https://docs.minded.ai/low-code-editor/nodes).

## [1.0.69] - 2025-06-30

### Added

- **Playbooks**: Added support for playbooks. Learn more about playbooks [here](https://docs.minded.ai/low-code-editor/playbooks).

## [1.0.68] - 2025-06-30

### Fixed

- Voice in playground bug fix

## [1.0.67] - 2025-01-30

### Fixed

- **Edge Handling**: Fixed issue with edges to **end** node when canStayOnNode=true

## [1.0.65] - 2025-01-29

### Internal

- **Deployment Infrastructure**: Enhanced managed agent deployment process
  - Improved build pipeline efficiency
  - Optimized Lambda function generation
  - Better error handling during deployment

## [1.0.64] - 2025-01-29

### Internal

- **CLI Enhancements**: Added `generate-lambda-ts-handler` command for managed agent deployments
  - Generates TypeScript Lambda handler with proper AWS types
  - Respects project's tsconfig.json settings
  - Automatically compiles handler to configured output directory
  - Improved template management for better maintainability

### Changed

- **Build Process**: Updated build scripts to include CLI templates in distribution
  - Lambda handler template now included in npm package

## [1.0.63] - 2025-01-27

### Changed

- **BREAKING: Events API Enhanced with Full State Access** :
  - **AI_MESSAGE Event**: Now passes the full agent `state` object instead of separate `memory` and `sessionId` parameters
  - **Before**: `{ message: string, memory: Memory, sessionId: string }`
  - **After**: `{ message: string, state: { messages, memory, history, sessionId } }`
  - Event handlers now have access to complete agent state including conversation messages, flow execution context
  - Enhanced session management and debugging capabilities through comprehensive state visibility

### Improved

- **Tool Response Handling**: Fixed tool response state updates to properly include tool messages in the conversation history
- **Type Safety**: Enhanced event payload typing with proper generic memory support using `StateWithMemory<Memory>` helper type
- **Documentation**: Updated event handling examples and documentation to reflect new state-based API across all code samples

### Migration Guide

#### Updating AI_MESSAGE Event Handlers

**Before (Old API):**

```ts
agent.on(events.AI_MESSAGE, async ({ message, memory, sessionId }) => {
  console.log('AI said:', message);
  console.log('Current memory:', memory);
  console.log('Session ID:', sessionId);

  await sendMessageToUser(message, sessionId);
});
```

**After (New API):**

```ts
agent.on(events.AI_MESSAGE, async ({ message, state }) => {
  console.log('AI said:', message);
  console.log('Current memory:', state.memory);
  console.log('Session ID:', state.sessionId);
  console.log('Message count:', state.messages.length);

  await sendMessageToUser(message, state.sessionId);

  // Now you can access full conversation context
  await websocket.send(
    JSON.stringify({
      type: 'ai_message',
      content: message,
      sessionId: state.sessionId,
      memory: state.memory,
      messageCount: state.messages.length,
    }),
  );
});
```

## [1.0.61] - 2025-06-25

### Added

- **Structured Logging System**: Added comprehensive logging functionality with contextual data support
  - Import logger from `mindedjs`: `import { logger } from 'mindedjs'`
  - Support for structured logging with session context
  - Automatic PII masking in log entries when PII masking is enabled
  - Log levels: debug, info, warn, error
  - Performance and error logging best practices

- **Enhanced PII Masking Configuration**:
  - Added Trigger SessionId Field configuration in the UI
  - Field name validation (letters, numbers, underscores only)
  - Improved session isolation and PII data grouping

- **Comprehensive PII Gateway Documentation**:
  - Complete HTTP client interface documentation
  - Support for all HTTP methods (GET, POST, PUT, DELETE, PATCH)
  - Request configuration options (headers, params)
  - Enhanced error handling and logging integration

### Changed

- **BREAKING: Tools API Updated**: Tools now receive `state` object instead of `memory` parameter
  - **Before**: `execute: ({ input, memory }) => Promise<{ memory?, result? }>`
  - **After**: `execute: ({ input, state, agent }) => Promise<{ state?, result? }>`
  - `state` object includes `memory`, `sessionId`, and other platform context
  - Tools now receive `agent` parameter for accessing PII gateway and other features
  - Return value changed from `{ memory?, result? }` to `{ state?, result? }`
  - State updates are partial - only return the parts that changed
  - Memory is now accessed via `state.memory`

- **Enhanced Tool Functionality**:
  - Tools can now access `agent.piiGateway` for secure HTTP requests
  - Session context available via `state.sessionId`
  - Improved error handling with structured logging
  - Better integration with PII masking system

### Improved

- **PII Gateway Enhancements**:
  - Automatic request unmasking and response masking
  - Better session isolation and error handling
  - Comprehensive HTTP method support with configuration options
  - Improved integration with logging system

- **Documentation Updates**:
  - Updated tools documentation with new State-based API
  - Enhanced PII masking documentation with UI configuration details
  - Added comprehensive logging documentation
  - Updated all code examples to reflect new API patterns

### Migration Guide

#### Updating Tools to Use State API

**Before (Old API):**

```ts
const myTool: Tool<typeof schema, Memory> = {
  name: 'myTool',
  description: 'My tool',
  input: schema,
  execute: async ({ input, memory }) => {
    console.log(memory.userId);

    return {
      memory: {
        lastAction: input.action,
      },
      result: 'Success',
    };
  },
};
```

**After (New API):**

```ts
import { logger } from 'mindedjs';

const myTool: Tool<typeof schema, Memory> = {
  name: 'myTool',
  description: 'My tool',
  input: schema,
  execute: async ({ input, state, agent }) => {
    logger.info('Tool execution', {
      sessionId: state.sessionId,
      userId: state.memory.userId,
    });

    return {
      state: {
        memory: {
          lastAction: input.action,
        },
      },
      result: 'Success',
    };
  },
};
```

#### Key Changes to Apply:

1. **Parameter Changes**:
   - Replace `memory` parameter with `state`
   - Add `agent` parameter
   - Access memory via `state.memory`

2. **Return Value Changes**:
   - Replace `{ memory?, result? }` with `{ state?, result? }`
   - Wrap memory updates in `state: { memory: { ... } }`
   - Return only partial state updates

3. **Logging Updates**:
   - Replace `console.log` with `logger` methods
   - Include `sessionId` in log context
   - Use structured logging objects

4. **PII Gateway Usage**:
   - Replace direct HTTP calls with `agent.piiGateway` methods
   - Always pass `state.sessionId` as first parameter

This update provides better separation of concerns, improved PII security, and enhanced observability while maintaining backward compatibility where possible.

## [1.0.96] - 2025-07-17

### Changed

- **Main Flow Priority**: Updated agent initialization to ensure the first node is always from the Main flow when no triggers are present, improving flow predictability and execution order.

## [1.0.98] - 2025-07-17

### Added

- **Goto support**: Added support for tools to control flow by returning a `goto` property in their state update, enabling programmatic navigation to specific nodes
