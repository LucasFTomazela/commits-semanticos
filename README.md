# Guia Completo de Commits Semânticos

Este guia foi desenvolvido para ajudar desenvolvedores de todos os níveis a entenderem e implementarem commits semânticos em seus projetos. Com explicações detalhadas e exemplos práticos, você aprenderá a criar commits mais organizados e significativos.

## Por que usar Commits Semânticos?

Os commits semânticos oferecem diversos benefícios:

1. **Histórico Claro**: Facilita o entendimento da evolução do projeto
2. **Automatização**: Permite a geração automática de changelogs
3. **Organização**: Padroniza a comunicação das alterações no código
4. **Produtividade**: Agiliza a identificação de mudanças específicas
5. **Colaboração**: Melhora a comunicação entre membros da equipe

## Estrutura do Commit

### Formato Básico
```
<tipo>[escopo opcional]: <descrição>

[corpo opcional]

[rodapé opcional]
```

### Elementos da Estrutura

1. **Tipo**: Categoria da alteração (obrigatório)
2. **Escopo**: Parte do código afetada (opcional)
3. **Descrição**: Resumo da alteração (obrigatório)
4. **Corpo**: Detalhes adicionais (opcional)
5. **Rodapé**: Informações de breaking changes ou referências a issues (opcional)

### Exemplo Completo
```
feat(auth): implementa autenticação com Google

- Adiciona dependências do OAuth2
- Configura rotas de autenticação
- Implementa middleware de verificação

BREAKING CHANGE: Esta alteração requer nova configuração no arquivo .env
Closes #123
```

## Tipos de Commits por Fase do Projeto

### Fase Inicial do Projeto
| Tipo      | Descrição                          | Objetivo                                                | Exemplos |
|-----------|------------------------------------|---------------------------------------------------------|---------|
| init      | Inicialização                      | Início do projeto ou funcionalidade                     | `init: início do projeto` <br> `init: configuração inicial do React` |
| build     | Build                              | Mudanças em scripts de build ou dependências            | `build: adiciona webpack` <br> `build: atualiza versão do Node` |
| ci        | Integração Contínua                | Alterações nos arquivos de integração contínua          | `ci: configura GitHub Actions` <br> `ci: adiciona step de testes` |
| docs      | Documentação                       | Alterações relacionadas apenas à documentação           | `docs: adiciona instruções de instalação` <br> `docs: atualiza API docs` |

### Fase de Desenvolvimento Ativo
| Tipo      | Descrição                          | Objetivo                                                | Exemplos |
|-----------|------------------------------------|---------------------------------------------------------|---------|
| feat      | Nova Funcionalidade                | Implementação de uma nova funcionalidade                | `feat(user): adiciona cadastro` <br> `feat: implementa carrinho` |
| ui        | Interface do Usuário               | Alterações específicas na interface                     | `ui: atualiza tema dark` <br> `ui(navbar): redesign do menu` |
| style     | Estilo                             | Mudanças que não afetam a lógica                       | `style: formata código` <br> `style(css): ajusta spacing` |
| test      | Testes                             | Adição ou correção de testes                            | `test: adiciona testes unitários` <br> `test(api): mock de responses` |

### Fase de Manutenção e Otimização
| Tipo      | Descrição                          | Objetivo                                                | Exemplos |
|-----------|------------------------------------|---------------------------------------------------------|---------|
| fix       | Correção de Bug                    | Solução de um problema ou bug                           | `fix: corrige cálculo total` <br> `fix(auth): token expirado` |
| refactor  | Refatoração                        | Melhorias na estrutura do código                        | `refactor: simplifica lógica` <br> `refactor(db): otimiza queries` |
| perf      | Performance                        | Otimizações de performance                              | `perf: melhora loading` <br> `perf(images): implementa lazy load` |
| security  | Segurança                          | Correções ou melhorias de segurança                     | `security: atualiza dependências` <br> `security(auth): força HTTPS` |

### Fase de Manutenção Geral
| Tipo      | Descrição                          | Objetivo                                                | Exemplos |
|-----------|------------------------------------|---------------------------------------------------------|---------|
| chore     | Tarefas Gerais                     | Mudanças em processos de build ou ferramentas          | `chore: atualiza dependências` <br> `chore(deps): remove pacotes não usados` |
| revert    | Reversão                           | Reverte um commit anterior                              | `revert: volta versão auth` <br> `revert: remove feature x` |
| locale    | Internacionalização                | Alterações em traduções e localização                   | `locale: adiciona pt-BR` <br> `locale(en): corrige textos` |
| data      | Dados                              | Mudanças em dados ou conteúdo                          | `data: atualiza lista de países` <br> `data(products): novos itens` |

## Guia Prático para Bons Commits

### Regras Essenciais

1. **Use o Imperativo**: 
   - ✅ `feat: adiciona botão de login`
   - ❌ `feat: adicionado botão de login`

2. **Seja Específico**:
   - ✅ `fix: corrige validação de email no formulário de cadastro`
   - ❌ `fix: corrige bug`

3. **Mantenha Commits Atômicos**:
   - ✅ Um commit por alteração lógica
   - ❌ Várias alterações não relacionadas no mesmo commit

4. **Use o Escopo Quando Relevante**:
   - ✅ `feat(auth): adiciona login com Google`
   - ✅ `fix(cart): corrige cálculo do total`

### Exemplos de Sequência de Commits em um Projeto

```
init: configuração inicial do projeto
build: adiciona dependências básicas
feat(auth): implementa sistema de login
test(auth): adiciona testes para autenticação
style: ajusta formatação do código
fix(auth): corrige validação de senha
perf(auth): melhora tempo de resposta
docs: atualiza README com novas instruções
```

## Dicas Avançadas

### Breaking Changes

Quando sua alteração quebra a compatibilidade:

```
feat(api): simplifica método de autenticação

BREAKING CHANGE: O método auth() agora requer um objeto de configuração
```

### Múltiplos Tipos

Quando sua alteração se encaixa em múltiplos tipos, escolha o mais significativo:

- Se você corrigiu um bug enquanto refatorava, use `refactor` se a refatoração era o objetivo principal
- Use `fix` se o bug era o foco principal da alteração

### Revertendo Commits

```
revert: feat(auth): implementa login com Google

Este commit reverte o commit abc123
```

## Ferramentas Úteis

1. **Commitizen**: CLI que ajuda a criar commits padronizados
2. **Commitlint**: Ferramenta para validar mensagens de commit
3. **Husky**: Permite adicionar hooks do git para validar commits
4. **Standard Version**: Geração automática de changelog

## Integração com Semantic Versioning

Os commits semânticos se integram naturalmente com versionamento semântico:

- `fix:` correlaciona com PATCH (1.0.1)
- `feat:` correlaciona com MINOR (1.1.0)
- `BREAKING CHANGE:` correlaciona com MAJOR (2.0.0)

## Referências

- [Commits Convencionais](https://www.conventionalcommits.org/pt-br/v1.0.0/)
- [Semantic Versioning](https://semver.org/lang/pt-BR/)
- [Angular Commit Guidelines](https://github.com/angular/angular/blob/master/CONTRIBUTING.md#commit)
- Experiências práticas de desenvolvimento

## ✍️ Autor
* [Lucas F. Tomazela](https://github.com/LucasFTomazela)
