# 🗂️ Projeto Alternativa – Pipeline de Dados com Dados Corrigidos
---

## 📖 Contexto

Durante o desenvolvimento do projeto proposto, foi identificado que os dados fornecidos inicialmente apresentavam inconsistências e registros ausentes. Esse problema impactava diretamente a construção da camada Silver e, consequentemente, comprometia as análises da camada Gold.

Após reportar a situação ao administrador, enquanto o problema não era solucionado, o autor do projeto, Daniel, encontrou uma alternativa viável para garantir a continuidade do desenvolvimento e a entrega dos resultados esperados.

Essa solução surgiu a partir de uma experiência anterior que já havia trabalhado com dados provenientes de Blob Storage. Esse conhecimento possibilitou traçar uma estratégia que contornasse as limitações da base original, utilizando uma nova fonte de dados mais completa e confiável.

## 🚩 Problema Detectado

- A base de clientes original possuía registros ausentes.
- Vários IDs de clientes que apareciam na tabela de transações não existiam na tabela de clientes.
- Isso resultava em joins com muitos valores nulos, especialmente na coluna de data (`DataCriacao` ou `dt_transacao`), além de comprometer análises de volume, quantidade e evolução temporal.

## 🔄 Solução Proposta

Para garantir a qualidade dos dados e a correta construção das análises, optei por criar uma versão alternativa do pipeline:

- 🚀 **Fonte dos dados:** Foi utilizada uma nova base de dados vinda diretamente do Blob Storage, contendo os dados completos e corretos.
- 🔧 Todos os processos de construção das camadas **Bronze**, **Silver** e **Gold** foram refeitos com base nessa fonte.
- 🔗 As análises foram reconstruídas e estão agora com dados íntegros e confiáveis.

## 🚧 Estrutura da Pasta "Alternativa"

- **Camada - Bronze:** Extração dos dados do Blob, padronização e armazenamento bruto.
- **Camada - Silver:** Dados tratados, corrigidos, enriquecidos e prontos para análise.
- **Camada - Gold:** Métricas, agregações e KPIs solicitados, além de análises adicionais (Plus).
- **Camada - Configuração:** Credenciais, parâmetros e variáveis de ambiente necessárias para a execução segura do pipeline.

## ✅ Benefícios dessa abordagem

- Dados completos e íntegros.
- Joins realizados corretamente, sem perda de informações.
- Análises coerentes e fidedignas, que representam a realidade dos dados.

## ✍️ Observação

A versão original do projeto permanece no repositório, preservada para consulta, validação e histórico de desenvolvimento. Porém, recomenda-se utilizar a versão da pasta **"Alternativa"** como referência para os dados confiáveis e análises consistentes.

---
