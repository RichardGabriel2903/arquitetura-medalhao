🚀 Pipeline ETL com Arquitetura Medalhão: De Dados Brutos a Insights Reais
Este projeto foi desenvolvido como um desafio prático de Engenharia de Dados, focado na implementação da Arquitetura Medalhão para transformar dados crus em uma visão analítica consolidada. Indo além do conteúdo básico do curso, implementei rotinas de Data Quality, normalização de dados e análise exploratória.

🏗️ A Arquitetura e o Fluxo de Dados
O pipeline segue a separação lógica de responsabilidades para garantir escalabilidade e confiança no dado:

Camada Bronze (Raw): Armazenamento fiel dos dados brutos recebidos em formatos heterogêneos (CSV, JSON).

Camada Silver (Validated): Processo de limpeza e conversão. Aqui, os dados foram tipados e salvos em formato Parquet, otimizando o armazenamento e a performance de leitura.

Camada Gold (Enriched): Camada de consumo onde realizei o Inner Join entre Usuários e Localização (CEP), criando uma visão de negócio pronta para BI.

🛠️ Tecnologias e Ferramentas
Linguagem: Python 3.x

Processamento de Dados: Pandas

Armazenamento: Parquet (Formatos colunares)

Banco de Dados: PostgreSQL (via Docker)

Visualização: Matplotlib & Seaborn

Ambiente: Jupyter Notebooks & VS Code

💡 Meus Diferenciais (O que adicionei ao projeto)
Para elevar o nível técnico da entrega, implementei as seguintes melhorias:

Normalização de Gênero: Identifiquei e corrigi inconsistências de strings (ex: "F " vs "F") que causavam duplicidade em análises estatísticas.

Ordenação Numérica: Corrigi a lógica de ordenação da Query Gold, realizando o CAST de IDs que estavam em formato string para Integer.

Data Visualization: Desenvolvi um Dashboard no data-view.ipynb para analisar a distribuição de usuários por UF, Gênero e Ano de Nascimento.

Boas Práticas de DevOps: Configuração de .gitignore profissional e gerenciamento de dependências via requirements.txt.

🚀 Como Rodar o Projeto
Clone o repositório:

Bash

git clone https://github.com/seu-usuario/seu-repositorio.git
cd seu-repositorio
Crie e ative seu ambiente virtual:

Bash

python -m venv .venv
source .venv/bin/activate  # Linux/Mac
.venv\Scripts\activate     # Windows
Instale as dependências:

Bash

pip install -r requirements.txt
Suba o banco de dados e rode o pipeline:

Bash

docker-compose up -d
python populate_db.py
python normalize_data.py
📈 Próximos Passos
Pretendo expandir este projeto integrando o arquivo products.json para criar uma Tabela Fato de Vendas, permitindo analisar o ticket médio por região.