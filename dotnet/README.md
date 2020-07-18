# Uonet+ request signer for .NET

![Nuget](https://img.shields.io/nuget/v/UonetRequestSigner?style=flat-square)

## Instalation

```bash
$ dotnet add package UonetRequestSigner
```

## Usage

```cs
using Wulkanowy

var signed = UonetRequestSigner.SignContent(Password, Certificate, ontent)
```

## Tests

```bash
$ dotnet test
```
