# AZURE-dio
Criei este repositório para organizar e compartilhar as atividades realizadas durante o Bootcamp Azure promovido pela DIO.

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
