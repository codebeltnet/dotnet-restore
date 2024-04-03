# .NET Restore

This action uses the .NET CLI `dotnet restore` command including a select few options tied to [dotnet restore](https://learn.microsoft.com/en-us/dotnet/core/tools/dotnet-restore) otherwise pre-configured specifically for the Codebelt methodology.

Supports `projects` input we learned to appreciate from [AzDO DotNetCoreCLI](https://learn.microsoft.com/en-us/azure/devops/pipelines/tasks/reference/dotnet-core-cli-v2?view=azure-pipelines).

This ensures a smooth and consistent way to setup your CI/CD pipeline as well as structuring your repository.

## Usage

To use this action in your GitHub repository, you can follow these steps:

```yaml
uses: codebeltnet/dotnet-restore@main
```

### Inputs

```yaml
with:
  # Optional path to the project(s) file to restore. Pass empty to restore all dependencies and tools of a solution. 
  # Supports globbing.
  projects: '**/*.csproj'

  # Sets the verbosity level of the command.
  # Allowed values are q[uiet], m[inimal], n[ormal], d[etailed], and diag[nostic]. 
  # The default is quiet.
  level: 'quiet'
```

### Outputs

This action has no inputs.

## Examples

### Restore all C# projects

```yaml
steps:
  - name: Restore Dependencies
    uses: codebeltnet/dotnet-restore@main
```

## Contributing to .NET Restore

Contributions are welcome! 
Feel free to submit issues, feature requests, or pull requests to help improve this action.

### License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
