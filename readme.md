# Redash

Redash (https://redash.io/) é uma ferramenta para criação de painéis de informações (dashboards), facilitando a exploração de dados de múltiplas fontes (datasources).
É uma ferramenta open source mantida pela Databricks (https://www.databricks.com/). 

## Versão
Essa instalação do Redash está baseada na imagem: **redash/redash:10.1.0.b50633**

## Principais funcionalidades

 - A interface do Redash facilita a navegação e identificação dos recursos necessários para a criação de seus Dashboards. 
 - Você pode criar conexões (data sources) para vários bancos de dados inclusive criar conexões à APIs Externas (JSON). https://redash.io/integrations/.
 - Para criar as consultas (queries) aos Data Sources você utiliza a "linguagem" SQL. 
 - Você pode criar filtros específicos para cada gráfico ou para todo o Dashboard.
 - Facilidade para compartilhar o Dashboard.
 - Crie alertas conforme um critério.

## Instalando o Redash com o docker-compose

A maneira mais fácil e rápida para executar o Redash é utilizando o docker-compose. Para isso você deve ter o git, Docker e Docker Compose instalado em seu ambiente. 

 1. Clone o repositório: git clone https://github.com/macabral/redash
 2. Renomeie o arquivo .env.exemplo para .env e complete a configuração 
 3. Vá para a pasta redash e execute docker-compose up -d
 4. No navegador acesse: http://localhost:5000

## Configuração

No arquivo .env você encontra as configurações do Redash, inclusive a configuração do servidor de email para o envio dos alertas. (https://redash.io/help/open-source/admin-guide/env-vars-settings).

É importante configurar o servidor SMTP para o envio de emails. Se não desejar configurar remova as chaves de configuração (REDASH_MAIL_).
 
## Customizando os templates

Na pasta templates estão os modelos utilizados pelo Redash para o envio de alertas e emails relacionados à conta do Usuário. Você poderá alterar os templates conforme a sua necessidade, por exemplo, trocando o logo do Redash pelo logo da sua empresa.

## Dica:

Se o Redash não estiver disponível depois do reboot execute o comando: sudo systemctl enable --now docker.service

 ## Fluxo para a Criação de Dashboards
 
 - Crie os "Data Sources": vá para Configurações - Data Sources
 - Crie a sua Query: Create - New Query.
 - Crie a visualização dos dados (gráficos): Na edição da query selecione "Nova Visualização".
 - Crie seu Dashboard: Create - New Dashboard.
 - Adicione a visualização dos dados: Na edição do Dashboard selecione "Add Widget".

 ## Vídeos

 Getting Started With Redash - https://www.youtube.com/watch?v=Yn3_QDk2qQM
 
 How-to: Making Visualizations & Dashboards in Redash - https://www.youtube.com/watch?v=hp9rhiSHMZ0
 
 Introduction to Query Parameters - www.youtube.com/watch?v=02iQXd2Ouos

SPARK+AI Summit 2020 (Databricks) - https://www.youtube.com/watch?v=U32yv9e9HOI

