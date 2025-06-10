# 💼 Projeto Savana Tech – Arquitetura Medalhão com Databricks

Este projeto simula a criação de um DataLake para a fintech fictícia **Savana Tech**, utilizando a arquitetura **Bronze → Silver → Gold**, com ingestão de dados do **MongoDB** e **MySQL** no Databricks.

---

## 🧱 Estrutura do Projeto

```
Savana-Tech/
│
├── Camada - Bronze              # Ingestão dos dados brutos (Spark)
├── Camada - Silver              # Tratamento e enriquecimento (Spark)
├── Camada - Gold                # Métricas finais (SQL)
├── Camada - Configuração        # ⚠️ Armazena credenciais de acesso (IGNORADO NO GIT)
├── .gitignore                   # Arquivos que não devem ser versionados
└── README.md                    # Instruções do projeto
```

---

## ⚙️ Como executar

### 1. Clone o repositório
```bash
git clone https://github.com/DanielsOfficial0102/Savana-Tech
cd seu-repo
```

### 2. Conecte no Databricks

- Crie um cluster SINGLE NODE
- Instale os conectores:
  - `org.mongodb.spark:mongo-spark-connector_2.12:10.1.1`
  - `mysql:mysql-connector-java:8.0.33`
  - `pymongo`
  - `pymysql`
  - `pandas`

### 3. Importe os notebooks

Você pode importar os notebooks `.py`, `.ipynb` ou `.dbc` diretamente no seu workspace Databricks.

---

## 🔐 Proteção de credenciais

- As credenciais e configurações sensíveis estão no notebook:
  ```
  Camada - Configuração
  ```
- Este arquivo está **ignorado via `.gitignore`** para evitar o versionamento:
  ```gitignore
  **/Camada - Configuração.*
  ```

✅ **Nunca versionar acessos diretamente em repositórios Git!**

---

## 🗂️ Sobre os dados

- As transações são extraídas de um banco MongoDB remoto.
- A base de clientes vem de um banco MySQL.
- A camada Silver realiza a junção dos dois.
- A camada Gold aplica regras de negócio com SQL para gerar métricas.

---

## 📌 Observações

- Este projeto segue as orientações do desafio da Savana Tech.
- Todos os notebooks estão organizados para execução modular (em células por etapa).
- O GitHub não contém dados sensíveis por segurança.

---

## 👤 Autor

**Daniel Lopes**
