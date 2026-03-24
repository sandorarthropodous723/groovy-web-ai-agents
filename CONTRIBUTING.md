# Contributing to Groovy Web AI Agents

Thank you for your interest in contributing to Groovy Web AI Agents! This document provides guidelines and instructions for contributing.

## 📋 Table of Contents

- [Code of Conduct](#code-of-conduct)
- [Getting Started](#getting-started)
- [Development Setup](#development-setup)
- [Making Changes](#making-changes)
- [Submitting Changes](#submitting-changes)
- [Reporting Issues](#reporting-issues)

## 🤝 Code of Conduct

We are committed to providing a welcoming and inclusive environment. Please be respectful and constructive in all interactions.

## 🚀 Getting Started

### Prerequisites

- Node.js 18+ and npm/yarn/pnpm
- Git
- A code editor (VS Code recommended)

### Development Setup

1. Fork the repository
2. Clone your fork:

```bash
git clone https://github.com/YOUR_USERNAME/groovy-web-ai-agents.git
cd groovy-web-ai-agents
```

3. Install dependencies:

```bash
npm install
```

4. Create a feature branch:

```bash
git checkout -b feature/your-feature-name
```

## 🛠️ Development Setup

### Project Structure

```
groovy-web-ai-agents/
├── src/
│   ├── agents/           # Agent implementations
│   ├── prompts/          # Prompt templates
│   ├── orchestrators/    # Multi-agent coordination
│   ├── utils/           # Helper functions
│   └── types/           # TypeScript definitions
├── tests/               # Test files
├── docs/                # Documentation
└── examples/            # Usage examples
```

### Running Tests

```bash
# Run all tests
npm test

# Watch mode
npm run test:watch

# Coverage report
npm run test:coverage
```

### Building

```bash
# Build the project
npm run build

# Watch mode
npm run build:watch
```

### Linting

```bash
# Run linter
npm run lint

# Fix issues
npm run lint:fix
```

## ✏️ Making Changes

### Coding Standards

- Use TypeScript for all new code
- Follow existing code style and patterns
- Write meaningful commit messages
- Add tests for new features
- Update documentation as needed

### Adding a New Agent

1. Create agent file in `src/agents/`
2. Implement the `BaseAgent` interface:

```typescript
import { BaseAgent, AgentConfig } from './types';

export class YourAgent extends BaseAgent {
  constructor(config: AgentConfig) {
    super(config);
  }

  async execute(input: any): Promise<any> {
    // Your agent logic here
  }
}
```

3. Add tests in `tests/agents/`
4. Export from `src/agents/index.ts`
5. Update README with usage example

### Adding Prompts

1. Create prompt template in `src/prompts/`
2. Use Mustache syntax for variables:

```typescript
export const YOUR_PROMPT = `
You are a {{role}}.
Your task is to {{task}}.

Context:
{{context}}

Requirements:
{{requirements}}
`;
```

3. Add tests for prompt generation
4. Document prompt variables in docs/

## 📤 Submitting Changes

### Commit Message Format

Follow conventional commits:

```
type(scope): description

[optional body]

[optional footer]
```

Types: `feat`, `fix`, `docs`, `style`, `refactor`, `test`, `chore`

Example:

```
feat(content-agent): add markdown generation support

- Added markdown formatter
- Updated tests
- Added documentation example

Closes #123
```

### Pull Request Process

1. Update documentation
2. Ensure all tests pass
3. Update CHANGELOG.md
4. Submit a pull request with:
   - Clear description of changes
   - Link to related issues
   - Screenshots for UI changes (if applicable)
   - Checklist of items completed

### PR Template

```markdown
## Description
Brief description of changes

## Type of Change
- [ ] Bug fix
- [ ] New feature
- [ ] Breaking change
- [ ] Documentation update

## Testing
- [ ] Tests added/updated
- [ ] All tests passing

## Checklist
- [ ] Code follows style guidelines
- [ ] Self-review completed
- [ ] Documentation updated
- [ ] No new warnings generated
```

## 🐛 Reporting Issues

### Before Reporting

1. Search existing issues
2. Check if issue is in dependencies
3. Gather relevant information

### Issue Template

Include:
- Clear title
- Detailed description
- Steps to reproduce
- Expected behavior
- Actual behavior
- Environment details
- Code samples
- Error messages/screenshots

## 💬 Getting Help

- Open a discussion for questions
- Join our Discord community
- Check existing documentation

## 📝 License

By contributing, you agree that your contributions will be licensed under the MIT License.

---

Thank you for contributing to Groovy Web AI Agents!
