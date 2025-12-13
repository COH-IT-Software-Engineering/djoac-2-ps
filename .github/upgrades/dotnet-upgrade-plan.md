# .NET 10.0 Upgrade Plan

## Execution Steps

Execute steps below sequentially one by one in the order they are listed.

1. Validate that an .NET 10.0 SDK required for this upgrade is installed on the machine and if not, help to get it installed.
2. Ensure that the SDK version specified in global.json files is compatible with the .NET 10.0 upgrade.
3. Upgrade djoac-2-ps\djoac-2-ps.csproj

## Settings

This section contains settings and data used by execution steps.

### Excluded projects

| Project name | Description |
|:-----------------------------------------------|:---------------------------:|

### Aggregate NuGet packages modifications across all projects

NuGet packages used across all selected projects or their dependencies that need version update in projects that reference them.

| Package Name                        | Current Version | New Version | Description                                   |
|:------------------------------------|:---------------:|:-----------:|:----------------------------------------------|
| Microsoft.Extensions.Configuration              |   5.0.0         |  10.0.1      | Deprecated, recommended for .NET 10.0         |
| Microsoft.Extensions.Configuration.FileExtensions|   5.0.0         |  10.0.1      | Deprecated, recommended for .NET 10.0         |
| Microsoft.Extensions.Configuration.Json         |   5.0.0         |  10.0.1      | Deprecated, recommended for .NET 10.0         |
| System.Data.SqlClient                          |   4.8.2         |  4.9.0       | Security vulnerability                        |

### Project upgrade details

#### djoac-2-ps\djoac-2-ps.csproj modifications

Project properties changes:
  - Target framework should be changed from `netcoreapp3.1` to `net10.0`

NuGet packages changes:
  - Microsoft.Extensions.Configuration should be updated from `5.0.0` to `10.0.1` (deprecated, recommended for .NET 10.0)
  - Microsoft.Extensions.Configuration.FileExtensions should be updated from `5.0.0` to `10.0.1` (deprecated, recommended for .NET 10.0)
  - Microsoft.Extensions.Configuration.Json should be updated from `5.0.0` to `10.0.1` (deprecated, recommended for .NET 10.0)
  - System.Data.SqlClient should be updated from `4.8.2` to `4.9.0` (security vulnerability)

Other changes:
  - None
