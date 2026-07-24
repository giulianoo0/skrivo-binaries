# Skrivo Wallet — Binários

Distribuição de binários do **Skrivo Wallet**, o aplicativo desktop que guarda
o certificado digital A1 e mantém a conexão com o Skrivo.

Este repositório **não contém código fonte**. Os binários são compilados por
GitHub Actions a partir do repositório fonte privado — o fonte só existe dentro
do runner durante o build — e publicados em
[Releases](../../releases).

## Download

Pegue o `.tar.gz` da plataforma na release mais recente e confira o checksum:

```bash
tar -xzf skrivo-wallet-*-linux-x86_64.tar.gz
sha256sum -c skrivo-wallet-*-linux-x86_64.sha256
./skrivo-wallet
```

Plataformas: Linux x86_64 (Wayland/X11). Windows e macOS virão quando o app
ganhar suporte de bandeja nessas plataformas.

## Como um build é disparado

- Manualmente: aba Actions → "Build Skrivo Wallet" → Run workflow (opcionalmente
  apontando um branch/tag do fonte).
- Automaticamente: `repository_dispatch` (`build-wallet`) enviado pelo CI do
  repositório fonte ao criar uma tag `wallet-v*`.
