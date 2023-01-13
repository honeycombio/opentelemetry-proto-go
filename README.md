# opentelemetry-proto-go

[![Go Reference](https://pkg.go.dev/badge/go.opentelemetry.io/proto/otlp.svg)](https://pkg.go.dev/go.opentelemetry.io/proto/otlp)

Generated Go code for the OpenTelemetry protobuf data model.

**NOTE**

This is a modified version of the Go OpenTelemtry protobuf files to re-add deprecated/removed Metric types (IntSum, IntGuage, IntHistogram) and label type (StringKeyValue).

You should not depend on this module directly but instead use a replace in your go.mod to swap out the official proto package with this one like this:

```golang
replace go.opentelemetry.io/proto/otlp => github.com/honeycombio/opentelemetry-proto-go/otlp v0.19.0
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
