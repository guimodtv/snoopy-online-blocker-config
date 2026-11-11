# SNOOPY ONLINE BLOCKER

Repositório público de regras remotas para o SNOOPY FIREWALL.

## Arquivo usado pelo APK

- `config.json`
- URL RAW: `https://raw.githubusercontent.com/guimodtv/snoopy-online-config/main/config.json`

No aplicativo, abra **INFO → SNOOPY ONLINE BLOCKER**, informe essa URL e toque em **SINCRONIZAR AGORA**.

## Como alterar as permissões

Edite somente os campos `allowlist` e `appStates`:

- `true` = aplicativo verde, autorizado a usar internet.
- `false` = aplicativo vermelho, bloqueado.
- Pacotes que não estão instalados são ignorados pelo aparelho.
- Para liberar um aplicativo, adicione o pacote ao `allowlist` e marque-o como `true` em `appStates`.
- Para bloquear, remova-o do `allowlist` e marque-o como `false` em `appStates`.
- Incremente `version` a cada publicação de regras.
- Atualize `updatedAt`.

O APK mantém a última configuração válida offline, cria backup antes de substituir regras e atualiza a política sem reiniciar a VPN.

## Segurança

O APK aceita apenas HTTPS do GitHub e exige `integrity.sha256` e `integrity.ed25519`. A assinatura é feita sobre a representação canônica do JSON sem o campo `integrity` (chaves ordenadas, sem espaços extras). A chave privada nunca fica neste repositório.

A chave pública fixada no APK é Ed25519 e termina em:

```text
...T3UTtRAmOWw4=
```

Para assinar uma nova versão, use a chave privada offline correspondente e gere novamente os dois campos dentro de `integrity`. Não altere o arquivo manualmente depois de assinar.
