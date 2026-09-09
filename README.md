# CommBox

Solução de negócio com ambiente inteligente integrado (openCode + IA).

## Setup em Novo Computador

```bash
# 1. Clonar o repositório
git clone https://github.com/echevarria-bi/commbox.git
cd commbox

# 2. Configurar chaves de ambiente
[System.Environment]::SetEnvironmentVariable("ANTHROPIC_API_KEY", "sua_chave", "User")
[System.Environment]::SetEnvironmentVariable("GITHUB_TOKEN", "seu_token", "User")

# 3. Reiniciar o terminal e iniciar o opencode
opencode
```

## Inteligências Incluídas

Este repositório carrega automaticamente:
- **Agentes**: analista, dev, reviewer (em `.opencode/agents/`)
- **Skills**: analise-dados, dev-negocio (em `.opencode/skills/`)
- **Comandos**: /analise, /revisar (em `.opencode/commands/`)
- **Tema**: tokyonight dark

## Estrutura

```
commbox/
├── opencode.json       # Configuração do ambiente
├── AGENTS.md           # Instruções gerais
├── .opencode/
│   ├── agents/         # Inteligências (analista, dev, reviewer)
│   ├── skills/         # Habilidades customizadas
│   └── commands/       # Comandos personalizados
└── src/                # Código do projeto (criar)
```

## Configuração GitHub

Você precisa de um Personal Access Token com permissões:
- `repo`, `workflow`, `read:org`

Criar em: https://github.com/settings/tokens