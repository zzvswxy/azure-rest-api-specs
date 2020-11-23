## Java

These settings apply only when `--java` is specified on the command line.
Please also specify `--azure-libraries-for-java-folder=<path to the root directory of your azure-libraries-for-java clone>`.

``` yaml $(java)
azure-arm: true
fluent: true
namespace: com.microsoft.azure.management.azureiidt
license-header: MICROSOFT_MIT_NO_CODEGEN
payload-flattening-threshold: 1
output-folder: $(azure-libraries-for-java-folder)/azure-mgmt-azureiidt
```

### Java multi-api

``` yaml $(java) && $(multiapi)
batch:
  - tag: package-2020-06-10-privatepreview
  - tag: package-2020-07-01-privatepreview
  - tag: package-2020-07-15-privatepreview
  - tag: package-2020-11-01-privatepreview

```

### Tag: package-2020-06-10-privatepreview and java

These settings apply only when `--tag=package-2020-06-10-privatepreview --java` is specified on the command line.
Please also specify `--azure-libraries-for-java=<path to the root directory of your azure-sdk-for-java clone>`.

``` yaml $(tag) == 'package-2020-06-10-privatepreview' && $(java) && $(multiapi)
java:
  namespace: com.microsoft.azure.management.azureiidt.v2020_06_10_privatepreview
  output-folder: $(azure-libraries-for-java-folder)/sdk/azureiidt/mgmt-v2020_06_10_privatepreview
regenerate-manager: true
generate-interface: true
```


### Tag: package-2020-07-01-privatepreview and java

These settings apply only when `--tag=package-2020-07-01-privatepreview --java` is specified on the command line.
Please also specify `--azure-libraries-for-java=<path to the root directory of your azure-sdk-for-java clone>`.

``` yaml $(tag) == 'package-2020-07-01-privatepreview' && $(java) && $(multiapi)
java:
  namespace: com.microsoft.azure.management.azureiidt.v2020_07_01_privatepreview
  output-folder: $(azure-libraries-for-java-folder)/sdk/azureiidt/mgmt-v2020_07_01_privatepreview
regenerate-manager: true
generate-interface: true
```

### Tag: package-2020-07-15-privatepreview and java

These settings apply only when `--tag=package-2020-07-15-privatepreview --java` is specified on the command line.
Please also specify `--azure-libraries-for-java=<path to the root directory of your azure-sdk-for-java clone>`.

``` yaml $(tag) == 'package-2020-07-15-privatepreview' && $(java) && $(multiapi)
java:
  namespace: com.microsoft.azure.management.azureiidt.v2020_07_15_privatepreview
  output-folder: $(azure-libraries-for-java-folder)/sdk/azureiidt/mgmt-v2020_07_15_privatepreview
regenerate-manager: true
generate-interface: true
```

### Tag: package-2020-11-01-privatepreview and java

These settings apply only when `--tag=package-2020-11-01-privatepreview --java` is specified on the command line.
Please also specify `--azure-libraries-for-java=<path to the root directory of your azure-sdk-for-java clone>`.

``` yaml $(tag) == 'package-2020-11-01-privatepreview' && $(java) && $(multiapi)
java:
  namespace: com.microsoft.azure.management.azureiidt.v2020_11_01_privatepreview
  output-folder: $(azure-libraries-for-java-folder)/sdk/azureiidt/mgmt-v2020_11_01_privatepreview
regenerate-manager: true
generate-interface: true
```

