# quantum

> see https://aka.ms/autorest

This is the AutoRest configuration file for quantum.

## Getting Started

To build the SDKs for My API, simply install AutoRest via `npm` (`npm install -g autorest`) and then run:

> `autorest readme.md`

To see additional help and options, run:

> `autorest --help`

For other options on installation see [Installing AutoRest](https://aka.ms/autorest/install) on the AutoRest github page.

---

## Configuration

### Basic Information

These are the global settings for the quantum.

``` yaml
openapi-type: arm
openapi-subtype: rpaas
tag: package-2022-01-10-preview
```

### Tag: package-2019-11-04-preview

These settings apply only when `--tag=package-2019-11-04-preview` is specified on the command line.

``` yaml $(tag) == 'package-2019-11-04-preview'
input-file:
  - Microsoft.Quantum/preview/2019-11-04-preview/quantum.json
```

### Tag: package-2022-01-10-preview

These settings apply only when `--tag=package-2022-01-10-preview` is specified on the command line.

``` yaml $(tag) == 'package-2022-01-10-preview'
input-file:
  - Microsoft.Quantum/preview/2022-01-10-preview/quantum.json
```

---

# Code Generation

## Swagger to SDK

This section describes what SDK should be generated by the automatic system.
This is not used by Autorest itself.

``` yaml $(swagger-to-sdk)
swagger-to-sdk:
  - repo: azure-sdk-for-python-track2
  - repo: azure-sdk-for-go
  - repo: azure-sdk-for-go-track2
  - repo: azure-sdk-for-js
```

## Go

See configuration in [readme.go.md](./readme.go.md)

## Python

See configuration in [readme.python.md](./readme.python.md)

## TypeScript

See configuration in [readme.typescript.md](./readme.typescript.md)

## CSharp

See configuration in [readme.csharp.md](./readme.csharp.md)

## Suppression

``` yaml
directive:
  - suppress: EnumInsteadOfBoolean
    where: $.definitions.operation.properties.isDataAction
    from: quantum.json
    reason: 'This property is really a boolean, there are no plans to have more than two values in the future.'
  - suppress: AvoidNestedProperties
    where: $.definitions.ProviderDescription.properties.properties
    from: quantum.json
    reason: We don't have end customers making direct API calls and this is a breaking change for our existing clients.
```
