# Azure Cognitive Search

Este repositório contém um guia prático para criar um ambiente no portal da Azure e explorar a funcionalidade de indexação e consulta de dados utilizando o Azure Cognitive Search. O objetivo é servir como material de apoio para estudos e futuras implementações.

---

## Objetivo

- Demonstrar como configurar um ambiente no Azure para o Cognitive Search.
- Explorar a funcionalidade de indexação e consulta de dados diretamente no portal da Azure.
- Fornecer insights e boas práticas adquiridas durante a prática.


## Pré-requisitos

Antes de começar, certifique-se de ter:

1. Uma conta no [Portal da Azure](https://portal.azure.com/).

---

### 1. Criar uma Conta no Azure
1. Acesse o portal do Azure em [https://portal.azure.com](https://portal.azure.com) e faça login com suas credenciais da Microsoft.
2. Caso ainda não tenha uma conta, clique em **"Criar conta gratuita"** e siga as instruções.

---

### 2. Criar um Serviço de Azure Cognitive Search
1. No portal, clique em **"Criar um recurso"**.
2. Em **"Categorias"**, selecione **"IA + Machine Learning"** e procure por **"Azure AI Search"**.
3. Clique em **"Criar"** e preencha as informações necessárias:
   - **Grupo de Recursos:** Crie um novo ou selecione um existente.
   - **Nome do Serviço:** Escolha um nome único.
   - **Região:** Escolha a East US.
   - **Plano de Tarifação:** Selecione a opção **"Basic"**.
4. Clique em **"Revisar e Criar"** e, em seguida, em **"Criar"**.

---

### 3. Criar um Recurso de IA
1. No portal, clique novamente em **"Criar um recurso"**.
2. Selecione **"AI + Machine Learning"** e clique em **"Azure AI Services"**.
3. Preencha as informações necessárias e clique em **"Revisar e Criar"**.
4. Aguarde a mensagem de sucesso para confirmar a criação do recurso.

---

### 4. Criar uma Conta de Armazenamento (Storage Account)
1. No portal, pesquise por **"Storage Account"** na barra de pesquisa e clique em **"Criar"**.
2. Preencha as informações necessárias:
   - **Performance:** Selecione **"Standard"**.
   - **Redundância:** Selecione **"LRS"**.
3. Clique em **"Revisar e Criar"** e aguarde a mensagem de sucesso.

---

### 5. Configurar Acesso Anônimo no Storage Account
1. Acesse o recurso de **Storage Account** criado.
2. Vá para **"Configurações" > "Configuração"**.
3. Ative a opção **"Allow Blob anonymous access"** e clique em **"Salvar"**.

---

### 6. Criar um Container no Storage Account
1. No recurso de **Storage Account**, vá para a aba **"Containers"** e clique em **"+ Container"**.
2. Preencha as informações necessárias:
   - **Anonymous access level:** Selecione **"Anonymous read access for containers and blobs"**.
3. Clique em **"Criar"**.

---

### 7. Fazer Upload de Arquivos no Container
1. Faça o download dos arquivos de exemplo no link: [https://aka.ms/mslearn-coffee-reviews](https://aka.ms/mslearn-coffee-reviews).
2. Extraia os arquivos baixados.
3. No container criado, clique em **"Upload"** e carregue os arquivos extraídos.

---

### 8. Importar Dados no Azure Cognitive Search
1. Acesse o recurso de **Azure Cognitive Search** criado no passo 2.
2. Clique em **"Importar Dados"**.
3. Em **"Data Source"**, selecione **"Azure Blob Storage"**.
4. Preencha as informações necessárias e conecte-se ao container criado no passo 6.
5. Clique em **"OK"** para concluir a importação.

---

### 9. Explorar Dados no Azure Cognitive Search
1. No recurso de **Azure Cognitive Search**, vá para a aba **"Search Explorer"**.
2. Insira uma consulta no formato OData para explorar os dados indexados.

**Exemplo de Consulta:**

```plaintext
search=coffee&$filter=rating ge 4
```

---

**Dica:** Consulte os seguintes links para aprofundar seus conhecimentos:

- [Documentação oficial do Azure Cognitive Search](https://learn.microsoft.com/azure/search/)
- [Exemplos de Consultas no Azure Cognitive Search](https://learn.microsoft.com/azure/search/search-query-overview)