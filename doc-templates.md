---
layout: default
title: Documentation Templates
nav_order: 3
permalink: /doc-templates
has_children: false
---

# Documentation Templates

This guide provides templates and commands to help you generate comprehensive documentation for your codebase using Cursor's AI capabilities.

## Table of Contents
- [Quick Command Reference](#quick-command-reference)
- [Documentation Templates](#documentation-templates)
- [Framework-Specific Documentation](#framework-specific-documentation)
- [Documentation Workflow](#documentation-workflow)
- [Best Practices](#best-practices)

## Quick Command Reference

Use these prompts with Cursor AI chat to generate different types of documentation.

### Project Documentation

- `Generate a README.md for this project with installation, setup, and usage instructions`
- `Create a project architecture overview explaining the main systems and their interactions`
- `Document the project folder structure with explanations of each directory's purpose`
- `Generate a contributing guide for this project`
- `Create a changelog template for this project`
- `Document environment variables and configuration options for this project`

### Code Structure Documentation

- `Create a module dependency graph documentation for this project`
- `Document the data flow between components/services in this application`
- `Generate API endpoints documentation with request/response formats`
- `Create a database schema documentation with table relationships`
- `Document the authentication and authorization flow in this application`
- `Generate a state management overview for this application`

### File-Level Documentation

- `Document this file's purpose, inputs, outputs, and dependencies`
- `Generate a detailed overview of the classes/functions in this file`
- `Create usage examples for the utilities in this file`
- `Document the error handling approach in this file`
- `Generate type definitions documentation for this file`
- `Document the business logic implemented in this file`

### Component/Function Documentation

- `Document this function with parameters, return values, and edge cases`
- `Create comprehensive documentation for this React component with props, state, and lifecycle hooks`
- `Document this API controller with all its routes and middleware`
- `Generate documentation for this database model with field explanations`
- `Document this utility class with all its methods and usage examples`
- `Create step-by-step usage examples for this service`

### Testing Documentation

- `Generate test documentation explaining the testing strategy`
- `Document test scenarios and coverage for this module`
- `Create test case documentation with expected inputs and outputs`
- `Document mocking strategies for this component's tests`

## Documentation Templates

### Project README Template

```markdown
# Project Name

## Overview
Brief description of what the project does and its main purpose.

## Features
- Feature 1: Description
- Feature 2: Description
- Feature 3: Description

## Technology Stack
- Frontend: [technologies]
- Backend: [technologies]
- Database: [technologies]
- Deployment: [technologies]

## Prerequisites
List of software, tools, and accounts needed before installation.

## Installation
```bash
# Step-by-step installation commands
npm install
```

## Configuration
Explanation of environment variables and configuration files.

## Usage
Basic examples of how to use the application.

## API Documentation
Link to or brief overview of API endpoints.

## Project Structure
Overview of the main directories and their purposes.

## Contributing
Guidelines for contributing to the project.

## License
Project license information.
```

### Module/File Documentation Template

```markdown
# Module Name: `filename.js`

## Purpose
Concise explanation of what this module does and why it exists.

## Dependencies
- Package/Module 1: Reason for dependency
- Package/Module 2: Reason for dependency

## Exports
| Name | Type | Description |
|------|------|-------------|
| `exportName` | Function/Class/Object | Brief description |

## Internal Components
List of key internal functions/classes not exported.

## Usage Examples
```javascript
// Example of how to use this module
import { someFunction } from './filename';

someFunction(params);
```

## Notes
Important information, limitations, or things to be aware of.
```

### Function Documentation Template

```markdown
## `functionName(param1, param2, ...)`

**Purpose**: What this function does.

**Parameters**:
- `param1` (Type): Description of parameter
- `param2` (Type): Description of parameter

**Returns**: 
- (Type): Description of return value

**Throws**:
- `ErrorType`: Conditions when error is thrown

**Example Usage**:
```javascript
const result = functionName('value1', 123);
// result will be...
```

**Notes**:
- Edge cases, performance considerations, or other important details
```

### Component Documentation Template

```markdown
## ComponentName

**Purpose**: What this component is responsible for.

**Props**:
| Prop | Type | Required | Default | Description |
|------|------|----------|---------|-------------|
| `propName` | `string` | Yes | - | What this prop controls |
| `callback` | `(param) => void` | No | `() => {}` | When this is called |

**State**:
| State | Type | Default | Description |
|-------|------|---------|-------------|
| `stateName` | `boolean` | `false` | What this state represents |

**Effects/Lifecycle**:
- On mount: Description of what happens
- On propName change: Description of what happens

**Example Usage**:
```jsx
<ComponentName 
  propName="value"
  callback={(result) => console.log(result)}
/>
```

**Rendered Output**:
Description of what this component renders in different states.
```

### API Endpoint Documentation Template

```markdown
## `GET /api/resource/:id`

**Purpose**: Description of what this endpoint does.

**URL Parameters**:
- `id` (string): Description of parameter

**Query Parameters**:
- `filter` (string, optional): Description of parameter

**Request Headers**:
- `Authorization`: Bearer token

**Request Body**:
```json
{
  "property": "value"
}
```

**Success Response**:
- Status: `200 OK`
```json
{
  "id": "123",
  "name": "Example"
}
```

**Error Responses**:
- Status: `404 Not Found`
```json
{
  "error": "Resource not found"
}
```

**Notes**:
- Rate limiting information
- Authentication requirements
- Other considerations
```

## Framework-Specific Documentation

### React Components

When documenting React components, request these additional sections:
- Prop validation
- Context usage
- Redux/state management connections
- Rendering optimizations
- Accessibility considerations
- Custom hooks used

Example prompt:
`Document this React component including prop validation, context usage, and accessibility considerations`

### Express/Node.js

For backend Node.js code, include:
- Middleware stack
- Error handling
- Request validation
- Response formatting
- Database interactions
- Authentication/authorization checks

Example prompt:
`Document this Express route with middleware, validation, and error handling explanations`

### Database Models

For ORM/database models:
- Schema definition
- Indexes and performance
- Relationships
- Validation rules
- Hooks/triggers
- Query examples

Example prompt:
`Document this database model with its schema, relationships, and example queries`

## Documentation Workflow

Follow this workflow for efficient documentation generation:

1. **Start with project overview**
   - Generate README.md
   - Document architecture and key concepts
   - Create directory structure documentation

2. **Document main interfaces**
   - API endpoints
   - Public components/modules
   - Database schema

3. **Document core functionality**
   - Business logic modules
   - Service layer
   - State management

4. **Document utilities and helpers**
   - Utility functions
   - Helper classes
   - Custom hooks

5. **Create examples and tutorials**
   - Usage examples
   - Integration examples
   - Common patterns

6. **Review and refine**
   - Check consistency
   - Fill documentation gaps
   - Add cross-references

## Best Practices

1. **Keep documentation close to code**
   - Place documentation in the same directory as the code it documents
   - Use file headers for overview and JSDoc for specifics

2. **Maintain consistent style**
   - Use consistent terminology throughout documentation
   - Follow the same templates for similar components

3. **Focus on the why, not just the what**
   - Explain rationale behind design decisions
   - Document non-obvious behaviors

4. **Document edge cases and limitations**
   - Note known issues or constraints
   - Document performance considerations

5. **Keep documentation up to date**
   - Update docs when code changes
   - Remove outdated information

6. **Include examples**
   - Provide realistic usage examples
   - Show common patterns and best practices

7. **Use formatting for readability**
   - Tables for structured data
   - Code blocks with syntax highlighting
   - Headers for organization

8. **Generate appropriate detail level**
   - More detail for complex, core functionality
   - Less detail for obvious utilities

9. **Include visual aids when helpful**
   - Flow diagrams for complex processes
   - Architecture diagrams for system overview
   - State diagrams for components with complex state

10. **Document for different audiences**
    - New developers (getting started)
    - Maintainers (implementation details)
    - API consumers (interface only) 