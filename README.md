# AZURE-dio
Criei este repositório para organizar e compartilhar as atividades realizadas durante o Bootcamp Azure promovido pela DIO.

# Aprendizado em Azure: Banco de Dados para Transporte

Este projeto demonstra meu aprendizado em recursos do Microsoft Azure, especialmente na criação, monitoramento e uso de um banco de dados SQL para armazenar e consultar dados relacionados a transporte.

Recursos Azure Utilizados

- **Azure SQL Database:** Criação e gerenciamento de banco de dados relacional na nuvem.
- **Azure Portal:** Utilizado para configuração, administração e acesso ao banco de dados.
- **Editor de Consultas SQL:** Para inserção, consulta e exportação de dados diretamente pelo portal.
- **Azure Dashboard:** Criação de painéis de monitoramento personalizados.

Estrutura do Banco de Dados

Foi criada uma tabela chamada `Viagens` com os seguintes campos:

- `id_viagem` (int, chave primária)
- `cidade_origem` (varchar)
- `cidade_destino` (varchar)
- `custo_frete` (decimal)
- `receita_frete` (decimal)
- `data_viagem` (date)

Exemplo de Dados Inseridos

| id_viagem | cidade_origem   | cidade_destino   | custo_frete | receita_frete | data_viagem |
|-----------|----------------|------------------|-------------|---------------|-------------|
| 1         | São Paulo      | Rio de Janeiro   | 1500.00     | 2500.00       | 2024-03-01  |
| 2         | Belo Horizonte | São Paulo        | 1200.00     | 2000.00       | 2024-03-05  |
| 3         | Rio de Janeiro | Curitiba         | 1800.00     | 2800.00       | 2024-03-10  |
| 4         | Curitiba       | Porto Alegre     | 1300.00     | 2200.00       | 2024-03-15  |
| 5         | São Paulo      | Belo Horizonte   | 1100.00     | 1900.00       | 2024-03-20  |

Dashboard de Monitoramento

Criei um dashboard no Azure Portal para monitorar três métricas principais do meu banco de dados `dio-nivia/adb-dio-transportes`:

- **Data space used (Máx):** 20,56 SB  
- **Failed Connections : User Errors (Contagem):** 5  
- **Successful Connections (Contagem):** 16  

Abaixo, segue a imagem do meu dashboard com essas métricas:
![image](https://github.com/user-attachments/assets/860df0d2-949f-4630-8797-8227e40df390)

## Pipeline de Transferência de Dados

1. Conceitos de Integração de Dados
   
- Pipelines de Dados: Entendi o papel dos pipelines como fluxos automatizados para mover e transformar dados entre sistemas.

- ETL (Extract, Transform, Load): Aprendi a extrair dados de uma fonte, realizar transformações (quando necessário) e carregá-los em um destino.

![image](https://github.com/user-attachments/assets/11995b4c-3934-4571-816e-aee0a7d8a0b3)


2. Azure Data Factory
Criação de Linked Services: Descobri como conectar o Azure Data Factory ao banco de dados de origem (SQL Server) e ao destino (Azure Blob Storage).

- Datasets: Aprendi a configurar datasets representando a tabela de origem e o arquivo de destino.

# Atividades de Cópia: Configurei uma atividade de cópia para transferir os dados da tabela viagens para o container bronze.

![image](https://github.com/user-attachments/assets/d3d67b53-b8f2-4279-b6b0-28fe499207ce)


3. Banco de Dados e Armazenamento em Nuvem
Consulta e Seleção de Dados: Pratiquei como selecionar e filtrar dados relevantes para exportação.

Azure Blob Storage: Aprendi a criar containers e entender a diferença entre as camadas bronze, silver e gold.

![image](https://github.com/user-attachments/assets/9ad06eb0-a027-464c-8bc4-e04327ed9e22)


4. Resolução de Problemas
Mensagens de Erro: Aprendi a interpretar mensagens de erro (como "Invalid object name") e a importância de validar nomes de tabelas, schemas e permissões.

Testes e Validações: Compreendi a necessidade de testar conexões e permissões antes de executar o pipeline completo.

## Exercício – Explorar o Azure Databricks

- CRIANDO UM CLUSTER

*Usando a Região Brazil South*

![image](https://github.com/user-attachments/assets/abd1217b-9b91-4c98-9243-b138d018478c)

  - ANÁLISE DE DADOS E FILTROS

![image](https://github.com/user-attachments/assets/c753fe53-f621-409e-b30c-25c0b863f9d3)

- GERNADO UM GRÁFICO

  ![image](https://github.com/user-attachments/assets/69a79c08-28d3-4831-9792-e765d2389b08)

*com as 10 categorias com mais produtos*


## Configurando o Azure Data Factory com Repositório do Azure DevOps

1. Criação do Data Factory
   
- No portal do Azure, crie um novo recurso do tipo Data Factory.
- Preencha as informações básicas: nome, grupo de recursos e região.
   
2. Acesso ao Data Factory Studio
Após a criação, acesse o recurso e clique em Iniciar Studio.

![image](https://github.com/user-attachments/assets/25af348f-3be4-442d-8d7c-2e8ed4ad71e0)
 
## 3. Configuração do Repositório Git 
No Data Factory Studio, vá em Gerenciar > Configuração do Git.

Escolha Azure DevOps Git como tipo de repositório.

Preencha os campos:

Microsoft Entra ID: Nome do locatário.

Organização do Azure Repos: Nome da organização no Azure DevOps.

Projeto: Nome do projeto no Azure DevOps.

Repositório: Nome do repositório Git.

Branch de colaboração: Ex: main.

Branch de publicação: Padrão adf_publish.

Pasta raiz: Caminho onde os arquivos serão salvos.

4. Finalização
Clique em Aplicar para concluir.
![image](https://github.com/user-attachments/assets/9980bf67-be16-4367-823c-1dd568db9098)

Seu Data Factory estará integrado ao Azure DevOps: todas as alterações serão versionadas automaticamente no repositório, facilitando o controle de mudanças e a colaboração em equipe.

![image](https://github.com/user-attachments/assets/8c799edd-d0b1-4682-b6db-bf41375be1f4)
