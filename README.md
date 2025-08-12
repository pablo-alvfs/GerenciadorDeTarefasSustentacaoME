# 📌 Gerenciador de Tarefas Sustentacao ME

Para o desafio da vaga backend sustentação, criei essa API REST para gerenciamento de tarefas, desenvolvida em **C#** com **.NET 8**, usando **Entity Framework Core** para comunicação com o sql e  **Swagger**. Procurei ser organizado e utilizar solid em camadas para deixar o código limpo, visando as complexas camadas que o time deve trabalhar no dia a dia.

---

## 🚀 Funcionalidades
- Criar, listar, detalhar, atualizar e excluir tarefas.
- Validações como título obrigatório e data de vencimento futura.
- Arquitetura em camadas seguindo princípios SOLID.

---

## 🛠 Tecnologias
- .NET 8 (ASP.NET Core Web API)
- Entity Framework Core
- SQL Server
- Swagger

---

## ⚙️ Como Executar
1. **Configurar conexão com banco**  
   No arquivo `appsettings.json`:
   ```json
   "ConnectionStrings": {
     "DefaultConnection": "Server=SEU_SERVIDOR;Database=GerenciadorTarefasDB;Trusted_Connection=True;TrustServerCertificate=True;"
   }
Criar banco de dados

dotnet ef database update

Executar projeto

dotnet run

Acessar Swagger
https://localhost:5001/swagger

Testando no Postman
1️⃣ Abrir Postman
Use a versão desktop ou web: https://web.postman.co

2️⃣ Criar nova requisição
Clique em New → HTTP Request

Escolha o método:

GET → Listar tarefas (https://localhost:5001/api/tarefas)

POST → Criar tarefa (https://localhost:5001/api/tarefas)

PUT → Atualizar tarefa (https://localhost:5001/api/tarefas/{id})

DELETE → Excluir tarefa (https://localhost:5001/api/tarefas/{id})

3️⃣ Configurar POST/PUT
Vá na aba Body → selecione raw → escolha JSON.

Exemplo de corpo para POST:

json
Copiar
Editar
{
  "titulo": "Finalizar relatório",
  "descricao": "Preparar relatório mensal",
  "dataVencimento": "2025-08-15",
  "status": "Pendente"
}
4️⃣ Enviar e verificar
Clique em Send e veja o retorno da API.
