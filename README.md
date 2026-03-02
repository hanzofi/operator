# Hanzo Fi Operator

Kubernetes operator for deploying and managing the Hanzo Fi Stack.

## Features

- Single CRD to deploy the full finance stack
- Automated database migrations
- Health monitoring and auto-recovery
- Rolling updates with zero downtime

## Quick Start

```bash
kubectl apply -f https://github.com/hanzofi/operator/releases/latest/download/install.yaml

kubectl apply -f - <<EOF
apiVersion: hanzo.fi/v1beta1
kind: Stack
metadata:
  name: production
spec:
  version: latest
  ledger:
    enabled: true
  payments:
    enabled: true
EOF
```

## Development

```bash
go build ./...
go test ./...
```

## License

MIT — see [LICENSE](LICENSE)

