# Security Center

> see https://aka.ms/autorest

This is the AutoRest configuration file for Security.

---

## Getting Started

To build the SDK for Security, simply [Install AutoRest](https://aka.ms/autorest/install) and in this folder, run:

> `autorest`

To see additional help and options, run:

> `autorest --help`

---

## Configuration

## Suppression

```yaml
directive:
  - suppress: ValidFormats
    from: securityContacts.json
    where: $.definitions.SecurityContactProperties.properties.email.format
    reason: email format is allowed
```

### Basic Information

These are the global settings for the Security API.

```yaml
title: SecurityCenter
description: API spec for Microsoft.Security (Azure Security Center) resource provider
openapi-type: arm
tag: package-composite-v3
```

## Composite packages

The following packages may be composed from multiple api-versions.

### Tag: package-composite-v1

These settings apply only when `--tag=package-composite-v1` is specified on the command line.

```yaml $(tag) == 'package-composite-v1'
input-file:
- Microsoft.Security/preview/2019-01-01-preview/regulatoryCompliance.json
- Microsoft.Security/preview/2017-08-01-preview/pricings.json
- Microsoft.Security/preview/2017-08-01-preview/securityContacts.json
- Microsoft.Security/preview/2017-08-01-preview/workspaceSettings.json
- Microsoft.Security/preview/2017-08-01-preview/autoProvisioningSettings.json
- Microsoft.Security/preview/2017-08-01-preview/compliances.json
- Microsoft.Security/preview/2017-08-01-preview/advancedThreatProtectionSettings.json
- Microsoft.Security/preview/2017-08-01-preview/deviceSecurityGroups.json
- Microsoft.Security/preview/2017-08-01-preview/settings.json
- Microsoft.Security/preview/2017-08-01-preview/informationProtectionPolicies.json
- Microsoft.Security/preview/2015-06-01-preview/operations.json
- Microsoft.Security/preview/2015-06-01-preview/locations.json
- Microsoft.Security/preview/2015-06-01-preview/tasks.json
- Microsoft.Security/preview/2015-06-01-preview/alerts.json
- Microsoft.Security/preview/2015-06-01-preview/discoveredSecuritySolutions.json
- Microsoft.Security/preview/2015-06-01-preview/jitNetworkAccessPolicies.json
- Microsoft.Security/preview/2015-06-01-preview/applicationWhitelistings.json
- Microsoft.Security/preview/2015-06-01-preview/externalSecuritySolutions.json
- Microsoft.Security/preview/2015-06-01-preview/topologies.json
- Microsoft.Security/preview/2015-06-01-preview/allowedConnections.json
- Microsoft.Security/preview/2015-06-01-preview/adaptiveNetworkHardenings.json

# Needed when there is more than one input file
override-info:
  title: SecurityCenter
```

### Tag: package-composite-v2

These settings apply only when `--tag=package-composite-v2` is specified on the command line.

```yaml $(tag) == 'package-composite-v2'
input-file:
- Microsoft.Security/preview/2019-01-01-preview/regulatoryCompliance.json
- Microsoft.Security/stable/2018-06-01/pricings.json
- Microsoft.Security/preview/2017-08-01-preview/securityContacts.json
- Microsoft.Security/preview/2017-08-01-preview/workspaceSettings.json
- Microsoft.Security/preview/2017-08-01-preview/autoProvisioningSettings.json
- Microsoft.Security/preview/2017-08-01-preview/compliances.json
- Microsoft.Security/preview/2017-08-01-preview/advancedThreatProtectionSettings.json
- Microsoft.Security/preview/2017-08-01-preview/deviceSecurityGroups.json
- Microsoft.Security/preview/2017-08-01-preview/settings.json
- Microsoft.Security/preview/2017-08-01-preview/informationProtectionPolicies.json
- Microsoft.Security/preview/2015-06-01-preview/operations.json
- Microsoft.Security/preview/2015-06-01-preview/locations.json
- Microsoft.Security/preview/2015-06-01-preview/tasks.json
- Microsoft.Security/stable/2019-01-01/alerts.json
- Microsoft.Security/preview/2015-06-01-preview/discoveredSecuritySolutions.json
- Microsoft.Security/preview/2015-06-01-preview/jitNetworkAccessPolicies.json
- Microsoft.Security/preview/2015-06-01-preview/applicationWhitelistings.json
- Microsoft.Security/preview/2015-06-01-preview/externalSecuritySolutions.json
- Microsoft.Security/preview/2015-06-01-preview/topologies.json
- Microsoft.Security/preview/2015-06-01-preview/allowedConnections.json
- Microsoft.Security/preview/2015-06-01-preview/adaptiveNetworkHardenings.json

# Needed when there is more than one input file
override-info:
  title: SecurityCenter
```

### Tag: package-composite-v3

These settings apply only when `--tag=package-composite-v3` is specified on the command line.

```yaml $(tag) == 'package-composite-v3'
input-file:
- Microsoft.Security/stable/2017-08-01/complianceResults.json
- Microsoft.Security/stable/2018-06-01/pricings.json
- Microsoft.Security/stable/2019-01-01/alerts.json
- Microsoft.Security/stable/2019-01-01/settings.json
- Microsoft.Security/preview/2015-06-01-preview/allowedConnections.json
- Microsoft.Security/preview/2015-06-01-preview/discoveredSecuritySolutions.json
- Microsoft.Security/preview/2015-06-01-preview/externalSecuritySolutions.json
- Microsoft.Security/preview/2015-06-01-preview/jitNetworkAccessPolicies.json
- Microsoft.Security/preview/2015-06-01-preview/applicationWhitelistings.json
- Microsoft.Security/preview/2015-06-01-preview/locations.json
- Microsoft.Security/preview/2015-06-01-preview/operations.json
- Microsoft.Security/preview/2015-06-01-preview/tasks.json
- Microsoft.Security/preview/2015-06-01-preview/topologies.json
- Microsoft.Security/preview/2017-08-01-preview/advancedThreatProtectionSettings.json
- Microsoft.Security/preview/2017-08-01-preview/autoProvisioningSettings.json
- Microsoft.Security/preview/2017-08-01-preview/compliances.json
- Microsoft.Security/preview/2017-08-01-preview/informationProtectionPolicies.json
- Microsoft.Security/preview/2017-08-01-preview/securityContacts.json
- Microsoft.Security/preview/2017-08-01-preview/workspaceSettings.json
- Microsoft.Security/preview/2017-08-01-preview/iotSecuritySolutions.json
- Microsoft.Security/preview/2017-08-01-preview/iotSecuritySolutionAnalytics.json
- Microsoft.Security/preview/2019-01-01-preview/regulatoryCompliance.json
- Microsoft.Security/preview/2019-01-01-preview/serverVulnerabilityAssessments.json

# Needed when there is more than one input file
override-info:
  title: SecurityCenter
```

---

# Code Generation

## Swagger to SDK

This section describes what SDK should be generated by the automatic system.
This is not used by Autorest itself.

```yaml $(swagger-to-sdk)
swagger-to-sdk:
  - repo: azure-sdk-for-go
  - repo: azure-sdk-for-python
  - repo: azure-sdk-for-js
  - repo: azure-sdk-for-node
```

## C#

See configuration in [readme.csharp.md](./readme.csharp.md)

## Go

See configuration in [readme.go.md](./readme.go.md)

## Python

See configuration in [readme.python.md](./readme.python.md)

## Node.js

See configuration in [readme.nodejs.md](./readme.nodejs.md)

## TypeScript

See configuration in [readme.typescript.md](./readme.typescript.md)

## Ruby

See configuration in [readme.ruby.md](./readme.ruby.md)
