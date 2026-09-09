# Ambiente Inteligente de Projetos

## Visão Geral
Este é um ambiente de desenvolvimento inteligente integrado com IA para análise de dados e desenvolvimento de soluções de negócio.

## Modelos Disponíveis
- **Padrão**: anthropic/claude-sonnet-4-6 (análise, código, general)

## Agentes
| Agente | Função |
|--------|--------|
| `analista` | Análise de dados e insights de negócio |
| `dev` | Desenvolvimento full-stack |
| `reviewer` | Revisão de código e qualidade |

## Comandos Úteis
- `/analise [arquivo]` - Analisa um arquivo de dados
- `/revisar [arquivo]` - Revisa código de um arquivo
- `/deploy` - Prepara e faz deploy da aplicação

## Integração GitHub
Configure a variável de ambiente `GITHUB_TOKEN` com um Personal Access Token:
```bash
export GITHUB_TOKEN="seu_token_aqui"
```

Permissões necessárias no token:
- `repo` - Acesso completo a repositórios
- `workflow` - Gerenciar workflows
- `read:org` - Ler informações da organização

## Integração Pipedrive (CRM)
O ambiente se conecta ao CRM Pipedrive via MCP:

- URL: `https://mcp.pipedrive.ai/mcp`
- Autenticação: OAuth (login do Pipedrive na primeira conexão)
- Ao iniciar o opencode, faça login no Pipedrive quando solicitado

Capacidades:
- Buscar deals, contatos e organizações
- Criar e atualizar registros no CRM
- Analisar pipeline e funil de vendas
- Gerenciar atividades e notas

## Estrutura de Pastas
```
.opencode/
├── agents/          # Agentes personalizados
│   ├── analista.md
│   ├── dev.md
│   └── reviewer.md
├── skills/          # Habilidades customizadas
│   ├── analise-dados/
│   └── dev-negocio/
└── commands/        # Comandos personalizados
```

## Boas Práticas
1. Sempre defina o contexto do projeto ao iniciar
2. Use o agente apropriado para cada tarefa
3. Valide resultados antes de commitar
4. Mantenha documentação atualizada
