# Redash

Redash (https://redash.io/) é uma ferramenta para criação de painéis de informações (dashboards), facilitando a exploração de dados de múltiplas fontes (datasources).
É uma ferramenta open source mantida pela Databricks (https://www.databricks.com/). 


## Instalando o Redash com o docker-compose

A maneira mais fácil e rápida para executar o Redash é utilizando o docker-compose. Para isso você deve ter o git, Docker e Docker Compose instalado em seu ambiente. 

 1. Clone o repositório: git clone https://github.com/macabral/redash
 2. Vá para a pasta redash e execute docker-compose up -d
 3. No navegador acesse: http://localhost:5000

## Versão
Essa instalação do Redash está baseada na imagem: **redash/redash:10.1.0.b50633**

## Principais funcionalidades

 - A interface do Redash facilita a navegação e identificação dos recursos necessários para a criação de seus Dashboards. 
 - Você pode criar conexões (data sources) para vários bancos de dados inclusive criar conexões à APIs Externas (JSON). https://redash.io/integrations/.
 - Para criar as consultas (queries) aos Data Sources você utiliza a "linguagem" SQL. 
 - Você pode criar filtros específicos para cada gráfico ou para todo o Dashboard.
 - Facilidade para compartilhar o Dashboard.
 - Crie alertas conforme um critério.

 ## Fluxo para a Criação de Dashboards
 
 - Crie os "Data Sources": vá para Configurações - Data Sources
 - Crie a sua Query: Create - New Query.
 - Crie a visualização dos dados (gráficos): Na edição da query selecione "Nova Visualização".
 - Crie seu Dashboard: Create - New Dashboard.
 - Adicione a visualização dos dados: Na edição do Dashboard selecione "Add Widget".

## Configuração

No arquivo .env você encontra as configurações do Redash, inclusive a configuração do servidor de email para o envio dos alertas. (https://redash.io/help/open-source/admin-guide/env-vars-settings)
 
 

