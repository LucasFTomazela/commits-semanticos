# Guia de Commits Semânticos

Este guia foi desenvolvido com base nas práticas recomendadas de commits semânticos e em experiências de mercado, focando na simplicidade e eficiência para o dia a dia de desenvolvimento. Os tipos de commits estão organizados seguindo o ciclo de vida típico de um projeto de desenvolvimento.

## Estrutura do Commit

Os commits devem seguir o formato abaixo, onde o *tipo* é obrigatório, e a descrição deve resumir a ação do commit de forma clara:

```
<tipo>: <descrição>
```

## Tipos de Commits por Fase do Projeto

### Fase Inicial
| Tipo      | Descrição                          | Objetivo                                                | Exemplo |
|-----------|------------------------------------|---------------------------------------------------------|---------|
| build     | Build                              | Mudanças em scripts de build ou dependências            | `build: configuração inicial do projeto com webpack` |
| ci        | Integração Contínua                | Alterações nos arquivos de integração contínua          | `ci: adiciona pipeline de deploy` |
| docs      | Documentação                       | Alterações relacionadas apenas à documentação           | `docs: adiciona README com instruções de instalação` |

### Fase de Desenvolvimento
| Tipo      | Descrição                          | Objetivo                                                | Exemplo |
|-----------|------------------------------------|---------------------------------------------------------|---------|
| feat      | Nova Funcionalidade                | Implementação de uma nova funcionalidade no projeto      | `feat: implementa sistema de login` |
| style     | Estilo                             | Mudanças que não afetam a lógica, como formatação      | `style: padroniza indentação do código` |
| test      | Testes                             | Adição ou correção de testes                            | `test: adiciona testes para módulo de autenticação` |

### Fase de Manutenção e Otimização
| Tipo      | Descrição                          | Objetivo                                                | Exemplo |
|-----------|------------------------------------|---------------------------------------------------------|---------|
| fix       | Correção de Bug                    | Solução de um problema ou bug no código                 | `fix: corrige validação de formulário` |
| refactor  | Refatoração                        | Alterações que melhoram a estrutura do código          | `refactor: simplifica lógica de processamento` |
| perf      | Melhoria de Desempenho            | Alterações visando otimizar a performance               | `perf: otimiza consultas ao banco de dados` |

### Fase de Manutenção Geral
| Tipo      | Descrição                          | Objetivo                                                | Exemplo |
|-----------|------------------------------------|---------------------------------------------------------|---------|
| chore     | Tarefas Gerais                     | Outras mudanças que não modificam código-fonte         | `chore: atualiza dependências` |
| revert    | Reversão                           | Reverte um commit anterior                              | `revert: volta versão anterior do componente` |

## Boas Práticas

1. **Seja Específico**: A descrição deve ser clara e objetiva, explicando o que foi feito
2. **Mantenha Consistência**: Use sempre o mesmo padrão de commits ao longo do projeto
3. **Commits Atômicos**: Cada commit deve representar uma única alteração lógica
4. **Evite Commits Genéricos**: Não use descrições vagas como "alterações diversas" ou "update"

## Exemplos Práticos de Uso

```
feat: adiciona autenticação com Google
fix: corrige cálculo de desconto no carrinho
docs: atualiza documentação da API
style: padroniza formatação do código CSS
refactor: simplifica lógica de processamento de pedidos
perf: otimiza carregamento de imagens
test: adiciona testes para módulo de pagamento
```

## Referências

Este guia é inspirado em fontes como:
- [Commits Convencionais](https://www.conventionalcommits.org/pt-br/v1.0.0/)
- Experiências práticas de desenvolvimento

## ✍️ Autor
* [Lucas F. Tomazela](https://github.com/LucasFTomazela)
