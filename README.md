# .NET Restore from Codebelt

Uses the .NET CLI `dotnet restore` [command](https://learn.microsoft.com/en-us/dotnet/core/tools/dotnet-restore) to restore the dependencies for specified projects or the solution itself.

Supports `projects` input we learned to appreciate from [AzDO DotNetCoreCLI](https://learn.microsoft.com/en-us/azure/devops/pipelines/tasks/reference/dotnet-core-cli-v2?view=azure-pipelines).

> This action is part of the Codebelt umbrella and ensures a consistent way of: 
> 
> - Defining your CI/CD pipeline 
> - Structuring your repository
> - Keeping your codebase small and feasible
> - Writing clean and maintainable code
> - Deploying your code to different environments
> - Automating as much as possible
>
> A paved path to excel as a DevSecOps Engineer.

See also: [dotnet-restore](https://github.com/codebeltnet/dotnet-restore)

## Usage

To use this action in your GitHub repository, you can follow these steps:

```yaml
uses: codebeltnet/dotnet-restore@v2
```

### Inputs

```yaml
with:
  # Optional path to the project(s) file to restore. Pass empty to restore all dependencies of a solution. 
  # Supports globbing.
  projects: ''
  # Sets the verbosity level of the command.
  # Allowed values are q[uiet], m[inimal], n[ormal], d[etailed], and diag[nostic].
  # Default is quiet.
  verbosity-level: 'quiet'
```

### Outputs

This action has no outputs.

## Examples

### Restore all C# projects

```yaml
steps:
  - name: Restore Dependencies
    uses: codebeltnet/dotnet-restore@v3
```

## Caller workflows to showcase the Codebelt experience

### Basic CI/CD Pipeline

- Bootstrapper API - https://github.com/codebeltnet/bootstrapper/blob/main/.github/workflows/pipelines.yml
- Extensions for Asp.Versioning API - https://github.com/codebeltnet/asp-versioning/blob/main/.github/workflows/pipelines.yml
- Extensions for AWS Signature Version 4 API - https://github.com/codebeltnet/aws-signature-v4/blob/main/.github/workflows/pipelines.yml
- Extensions for Globalization API - https://github.com/codebeltnet/globalization/blob/main/.github/workflows/pipelines.yml
- Extensions for Newtonsoft.Json API - https://github.com/codebeltnet/newtonsoft-json/blob/main/.github/workflows/pipelines.yml
- Extensions for Swashbuckle.AspNetCore API - https://github.com/codebeltnet/swashbuckle-aspnetcore/blob/main/.github/workflows/pipelines.yml
- Extensions for xUnit API - https://github.com/codebeltnet/xunit/blob/main/.github/workflows/pipelines.yml
- Extensions for YamlDotNet API - https://github.com/codebeltnet/yamldotnet/blob/main/.github/workflows/pipelines.yml
- Shared Kernel API - https://github.com/codebeltnet/shared-kernel/blob/main/.github/workflows/pipelines.yml
- Unitify API - https://github.com/codebeltnet/unitify/blob/main/.github/workflows/pipelines.yml

### Intermediate CI/CD Pipeline

- Savvy I/O - https://github.com/codebeltnet/savvyio/blob/main/.github/workflows/pipelines.yml

### Advanced CI/CD Pipeline

- Cuemon for .NET - https://github.com/gimlichael/Cuemon/blob/main/.github/workflows/pipelines.yml

## Contributing to .NET Restore from Codebelt

Contributions are welcome! 
Feel free to submit issues, feature requests, or pull requests to help improve this action.

### License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

> [!TIP]
> To learn more about the Codebelt experience and offerings, visit our [organization page](https://github.com/codebeltnet) on GitHub.
