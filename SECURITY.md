# Segurança das regras

Este repositório contém apenas JSON de configuração. O aplicativo não executa scripts, workflows, comandos ou código baixado daqui.

A configuração publicada deve possuir:

```json
"integrity": {
  "sha256": "SHA-256 do JSON canônico sem integrity",
  "ed25519": "assinatura Base64 do mesmo JSON canônico"
}
```

A chave privada de assinatura é mantida fora do GitHub. Se ela for perdida, o APK atual não aceitará novas regras até que seja lançado outro APK com uma nova chave pública.
