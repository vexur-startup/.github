# Estrutura Organizacional

| Elemento | Função                            |
| -------- | --------------------------------- |
| Issue    | Documento oficial de mudança (CR) |
| Branch   | Implementação técnica             |
| PR       | Revisão técnica da mudança        |
| Release  | Entrega formal                    |

## Como nomear a Change (Issue)

Você precisa de um identificador único.

- Modelo recomendado:

```text
CR-2026-014
```

- Estrutura:

```text
CR-ANO-SEQUENCIAL
```

Exemplo de título da Issue:

```text
[CR-2026-014] Ajuste regra de cálculo comissão cliente XPTO
```

Isso vira o identificador formal.

## Como nomear a Branch

A branch sempre deriva da Change.

- Formato recomendado:

```text
feature/CR-2026-014-ajuste-calculo-comissao
```

- Estrutura:

```text
tipo/ID-change-descricao-curta
```

### Tipos possíveis:

- feature/

- fix/

- hotfix/

- improvement/

- refactor/

Exemplo real:

```text

fix/CR-2026-021-validacao-cep-api
```

Isso cria rastreabilidade automática.

## Como nomear a Pull Request

O título da PR deve ser formal e referenciar a Change.

Formato:

```text
CR-2026-014 - Ajuste regra de cálculo comissão
```

Conventional Commits:

```text
feat(CR-2026-014): ajuste regra cálculo comissão cliente XPTO
```

## Como conectar tudo

Dentro da PR, sempre incluir:

```text
Closes #123
Ref: CR-2026-014
```

Onde:

```text
#123 é o número da Issue

CR-2026-014 é o ID formal
```

Isso cria vínculo automático.

## Exemplo Completo (Fluxo Real)

#### Cliente solicita mudança

Você cria Issue:

```text
#123
[CR-2026-014] Ajuste regra cálculo comissão cliente XPTO
```

#### Desenvolvedor cria branch

```text
feature/CR-2026-014-ajuste-calculo-comissao
```

#### Desenvolvedor abre PR

Título:

```text
CR-2026-014 - Ajuste regra cálculo comissão

```

Descrição:

```text
Implementa ajuste conforme CR-2026-014.

Closes #123
```
