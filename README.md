# monero-container

Docker image of monero for [BTCPay Server](https://github.com/btcpayserver/btcpayserver).

Published to `ghcr.io/btcpay-monero/monero-container`.

Built for `linux/amd64`, `linux/arm64`, and `linux/arm/v7`.

## Build locally

```sh
docker build -t monero-container .
```

## Releasing a new version

1. Branch off `master`.
2. Copy SHA256 for `linux-x64`, `linux-armv8`, and `linux-armv7` from [Monero release notes](https://github.com/monero-project/monero/releases).
3. In `monero.json`, bump `version` and three `checksums`.
4. Open PR.
5. Confirm three checksums against release notes, then merge to `master`.