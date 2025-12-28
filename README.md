# 🚀 Pipeline ETL com Arquitetura Medalhão

Este projeto foi desenvolvido como um desafio prático de Engenharia de Dados, focado na implementação da **Arquitetura Medalhão** para transformar dados crus em uma visão analítica consolidada. Indo além do básico, implementei rotinas de **Data Quality**, normalização e análise exploratória.

---

## 🏗️ A Arquitetura e o Fluxo de Dados

O pipeline segue a separação lógica de responsabilidades:

* **Camada Bronze (Raw):** Armazenamento fiel dos dados brutos recebidos (`CSV`, `JSON`).
* **Camada Silver (Validated):** Processo de limpeza e conversão para formato **Parquet**, otimizando performance.
* **Camada Gold (Enriched):** Camada de consumo com **Inner Join** entre Usuários e Localização (CEP), gerando uma visão pronta para BI.

---

## 🛠️ Tecnologias e Ferramentas

* **Linguagem:** Python 3.x
* **Processamento:** Pandas
* **Armazenamento:** Parquet (Formatos colunares)
* **Banco de Dados:** PostgreSQL (Docker)
* **Visualização:** Matplotlib & Seaborn
* **Ambiente:** Jupyter Notebooks & VS Code

---

## 💡 Meus Diferenciais (Data Quality)

Para elevar o nível técnico, implementei:

* **Normalização de Gênero:** Correção de strings (ex: "F " vs "F") para evitar duplicidade.
* **Ordenação Numérica:** Uso de `CAST` de IDs para ordenação correta na Gold.
* **Data Visualization:** Dashboard completo no `data-view.ipynb`.
* **Boas Práticas:** `.gitignore` profissional e `requirements.txt`.

---

## 🚀 Como Rodar o Projeto

1. **Clone o repositório:**
   ```bash
   git clone [https://github.com/seu-usuario/seu-repositorio.git](https://github.com/seu-usuario/seu-repositorio.git)
   cd seu-repositorio

2. **Crie e ative seu ambiente virtual:**
   ```bash
   python -m venv .venv
    # Windows:
    .venv\Scripts\activate
    # Linux/Mac:
    source .venv/bin/activate

3. **Instale as dependências:**
   ```bash
   pip install -r requirements.txt

4. **Suba o banco e rode o pipeline:**
    ```bash
    docker-compose up -d
    python populate_db.py
    python normalize_data.py

---

## 📈 Próximos Passos

Pretendo integrar o arquivo products.json para criar uma Tabela Fato de Vendas, permitindo analisar o ticket médio por região.