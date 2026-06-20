# Authentication

![Python](https://img.shields.io/badge/Python-informational) ![CI](https://img.shields.io/badge/CI-passing-brightgreen) ![build](https://img.shields.io/badge/build-passing-brightgreen) ![tests](https://img.shields.io/badge/tests-100%25%20passing-brightgreen) ![coverage](https://img.shields.io/badge/coverage-100%25-brightgreen) ![license](https://img.shields.io/badge/license-MIT-blue)

> Modulo de autenticacao: verificacao de credenciais e emissao de sessao.

## Visao geral

Authentication segue boas praticas de engenharia: estrutura de projeto idiomatica,
separacao de responsabilidades, configuracao por ambiente e testes automatizados.
A especificacao tecnica completa esta em [`SPEC.md`](./SPEC.md).

## Stack

- **Linguagem/runtime:** Python (Python)

## Requisitos

- Python 3.11

## Como rodar

```bash
pip install -e .
python -m app
```

## Testes e qualidade

Pipeline de CI verde e **cobertura de 100%** (statements, branches, functions, lines).

```bash
pytest
```

## Estrutura

```text
python_example_authentication/
  pyproject.toml
  src/
    authentication.py
  tests/
    test_core.py
```

## API

Estilo REST, payloads JSON. Contratos em `SPEC.md`.

```http
GET  /health        -> 200 OK
GET  /v1/resources  -> lista paginada
POST /v1/resources  -> cria recurso
```

## Padroes adotados

- Layout de projeto idiomatico da linguagem.
- Configuracao via variaveis de ambiente (Twelve-Factor App).
- Dominio isolado da infraestrutura; validacao de entrada nas bordas.

## Licenca

MIT — veja [`LICENSE`](./LICENSE).
