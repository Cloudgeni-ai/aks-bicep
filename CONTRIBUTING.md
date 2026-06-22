# Contributing

Thank you for your interest in contributing to this project.

## Prerequisites

- Azure CLI
- Bicep CLI
- An Azure subscription with Owner rights

## Development Workflow

1. Fork this repository and create a feature branch.
2. Make your changes to the Bicep templates or pipeline YAML files.
3. Validate your Bicep files locally:
   ```bash
   az bicep build --file bicep/main.bicep
   ```
4. Open a pull request against `main` with a clear description of the changes.

## Code Conventions

- Use `camelCase` for Bicep parameter and variable names.
- Provide `@description` decorators for all parameters.
- Include relevant `@allowed` constraints where applicable.
- Ensure all resources include a `tags` parameter.

## Pipelines

The Azure DevOps pipeline definitions reside in the repository root and under `bicep/`. Do not modify the service connection name (`AKSBicep`) or the variable group references without updating all pipeline files consistently.
