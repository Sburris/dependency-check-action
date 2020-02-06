# Introduction

 This action wraps the [OWASP Dependency Check](https://owasp.org/www-project-dependency-check/) scanning tool hosted in an unofficial docker image.

 *NOTE: The official docker image cannot be used in Github Actions because it does not run as the **root** user.*

## Usage

With minimal configuration

```yaml
    - uses: sburris/dependency-check-action@master
      with:
        Project-Name: TestApp
```

## Parameters

### Project-Name

The name of the project being scanned.

```yaml
    Project-Name:
        required: true
```

### Source-Location

The path to scan.

```yaml
    Source-Location:
        required: false
        default: '/github/workspace'
```

### Report-Format

What format(s) report to generate.

Options:

The report format (HTML, XML, CSV, JSON, JUNIT, or ALL). Multiple format parameters can be specified.

```yaml
    Report-Format:
        required: false
        default: 'ALL'
```

### Report-Location

The location to create the log file.

```yaml
    Report-Location:
        required: false
        default: '/github/workspace/reports'
```

### Log-Name

The name of the log file.

```yaml
    Log-Name:
        required: false
        default: log.txt
```
