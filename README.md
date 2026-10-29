# Testes de integração dos workflows reutilizáveis

## 1. Objetivo

Este repositório chama os componentes de [reusable-workflows](https://github.com/lpsm-dev/reusable-workflows) como um consumidor externo. O workflow usa um SHA completo para cada chamada. Os jobs cobrem análise de workflows, commits, YAML, Shell, Dockerfile, Kubernetes, dependências, imagens e segredos.

O semantic-release roda com `dry-run: true`. A execução verifica a configuração e calcula a próxima versão sem publicar uma tag ou um GitHub Release.

## 2. Execução

O [workflow de consumo](.github/workflows/consumer-tests.yaml) roda em cada push na `main` e pode ser iniciado manualmente. As fixtures estão em `fixtures/`. A configuração do release fica em `.github/config/release/` para exercitar o contrato do workflow chamado.

Quando o repositório fornecedor mudar, atualize os SHA completos no workflow em um pull request e confira os três jobs antes de usar a revisão em outros projetos.
