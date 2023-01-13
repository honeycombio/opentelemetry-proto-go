# opentelemetry-proto-go

[![Go Reference](https://pkg.go.dev/badge/go.opentelemetry.io/proto/otlp.svg)](https://pkg.go.dev/go.opentelemetry.io/proto/otlp)

Generated Go code for the OpenTelemetry protobuf data model.

## Versioning Policy

The auto-generated Go code follows the stability guarantees as defined in
[maturity
level](https://github.com/open-telemetry/opentelemetry-proto?tab=readme-ov-file#maturity-level).

Versioning of modules in this project will be idiomatic of a Go project using [Go modules](https://github.com/golang/go/wiki/Modules).
They will use [semantic import versioning](https://github.com/golang/go/wiki/Modules#semantic-import-versioning).
Meaning modules will comply with [semver 2.0](https://semver.org/spec/v2.0.0.html) with the following exception:

- Packages with an `experimental` suffix do not comply with [semver 2.0](https://semver.org/spec/v2.0.0.html).
  - Backwards incompatible changes may be introduced to these packages between minor versions.
  - These packages are intended to be temporary.
    They will be deprecated and removed when the protobuf definition stabilizes or is removed.
    If the protobuf definition stabilizes, the package will be replaced with a stable "non-experimental" package.
    If the protobuf definition is removed, the package will be removed without a replacement.

**NOTE**

This is a modified version of the Go OpenTelemtry protobuf files to re-add deprecated/removed Metric types (IntSum, IntGuage, IntHistogram) and label type (StringKeyValue).

You should not depend on this module directly but instead use a replace in your go.mod to swap out the official proto package with this one like this:

```golang
replace go.opentelemetry.io/proto/otlp => github.com/honeycombio/opentelemetry-proto-go/otlp v1.3.0-compat
```

## Getting Started

Install the latest version in your project.

```sh
go get go.opentelemetry.io/proto/otlp@latest
```

Import the generated code directly in your project.

```go
import (
	collogspb "go.opentelemetry.io/proto/otlp/collector/logs/v1"
	colmetricspb "go.opentelemetry.io/proto/otlp/collector/metrics/v1"
	coltracepb "go.opentelemetry.io/proto/otlp/collector/trace/v1"
	commonpb "go.opentelemetry.io/proto/otlp/common/v1"
	logspb "go.opentelemetry.io/proto/otlp/logs/v1"
	metricspb "go.opentelemetry.io/proto/otlp/metrics/v1"
	resourcepb "go.opentelemetry.io/proto/otlp/resource/v1"
	tracepb "go.opentelemetry.io/proto/otlp/trace/v1"
)
```
