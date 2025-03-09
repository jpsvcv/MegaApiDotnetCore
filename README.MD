# Mega Man Robots API

<p align="center">
  <img src="./_docs/assets/icon.png" alt="Mega Man Robots API" width="150" />
  <br />
  <b>Mega Man Robots API</b>
  <br />
  <sub><sup><b>(MEGA-MAN-ROBOTS)</b></sup></sub>
  <br />
  <a href="https://github.com/felipeAguiarCode/MegaApiDotnetCore/actions/workflows/build.yml">
    <img src="https://github.com/felipeAguiarCode/MegaApiDotnetCore/actions/workflows/build.yml/badge.svg" alt="Build Status" />
  </a>
  <a href="https://github.com/felipeAguiarCode/MegaApiDotnetCore/releases/latest">
    <img src="https://img.shields.io/github/v/release/felipeAguiarCode/MegaApiDotnetCore" alt="Latest Release" />
  </a>
</p>

## Visão Geral

A **Mega Man Robots API** é um serviço backend desenvolvido em **.NET Core 3.1** que fornece dados estruturados em JSON sobre os chefes da série Mega Man. Ele foi projetado para fornecer um conjunto robusto de endpoints RESTful para consulta e manipulação desses dados.

A API utiliza **Entity Framework Core** para gerenciar a persistência dos dados e segue boas práticas como **injeção de dependência** e **padrão repositório**, tornando-a modular, escalável e de fácil manutenção.

<p align="center">
  <img src="./_docs/assets/carbon.png" alt="API Preview" />
</p>

---

## 📌 Recursos Principais

✅ Estrutura modular baseada em **.NET Core 3.1**
✅ **RESTful API** para acesso aos dados
✅ **Entity Framework Core** como ORM
✅ **Padrão Repositório** para manipulação dos dados
✅ Suporte a **migrações de banco de dados**
✅ **Arquitetura em camadas** para melhor organização do código
✅ **Testabilidade aprimorada** com injeção de dependência

---

## 🚀 Endpoints da API

A API disponibiliza os seguintes endpoints para interação:

| Método  | Endpoint              | Descrição |
|---------|----------------------|-------------------------------------------|
| GET     | `/api/v1/robots`     | Retorna uma lista de todos os robôs |
| GET     | `/api/v1/robots/{id}` | Retorna detalhes de um robô específico pelo ID |
| POST    | `/api/v1/robots`     | Cria um novo registro de robô |
| PUT     | `/api/v1/robots/{id}` | Atualiza as informações de um robô específico |
| DELETE  | `/api/v1/robots/{id}` | Remove um robô do banco de dados |

### 🔹 Exemplo de Resposta para `/api/v1/robots/{id}`
```json
{
  "id": 1,
  "name": "Cut Man",
  "game": "Mega Man",
  "weakness": "Super Arm",
  "weapon": "Rolling Cutter"
}
```

---

## 🛠 Tecnologias Utilizadas

| Tecnologia | Descrição |
|------------|--------------------------------------------------|
| **.NET Core 3.1** | Framework principal para desenvolvimento da API |
| **Entity Framework Core** | ORM para acesso e manipulação do banco de dados |
| **Newtonsoft.Json** | Serialização e desserialização de objetos JSON |
| **ASP.NET Core MVC** | Estrutura para construção de APIs RESTful |
| **Swagger** | Documentação interativa para a API |
| **Docker** | Containerização e deploy |

---

## 📦 Dependências

| Pacote | Versão | Link |
|------------|---------|--------------------------------------------------|
| `Microsoft.EntityFrameworkCore` | 3.1.8 | [NuGet](https://www.nuget.org/packages/Microsoft.EntityFrameworkCore/3.1.8) |
| `Microsoft.EntityFrameworkCore.Design` | 3.1.8 | [NuGet](https://www.nuget.org/packages/Microsoft.EntityFrameworkCore.Design/3.1.8) |
| `Microsoft.EntityFrameworkCore.SqlServer` | 3.1.8 | [NuGet](https://www.nuget.org/packages/Microsoft.EntityFrameworkCore.SqlServer/3.1.8) |
| `Newtonsoft.Json` | 12.0.2 | [NuGet](https://www.nuget.org/packages/Newtonsoft.Json/12.0.2) |

---

## 📂 Estrutura do Projeto

```
📂 src
│── 📂 Controllers      # Rotas e endpoints
│── 📂 Models           # Modelos do banco de dados
│── 📂 Services         # Lógica de negócio
│── 📂 Middlewares      # Manipuladores de requisições
│── 📂 Database         # Banco de dados
│   │── 📂 DTOs             # Objetos de transferência de dados
│   │── 📂 EntityFramework  # Configuração do ORM
│   │    │── 📂 Context         # Configuração do contexto
│   │    │── 📂 Migrations      # Migrações do banco de dados
│   │── 📂 Repositories     # Implementação do padrão Repositório
```

---

## 🎯 Como Executar o Projeto

1️⃣ Clone o repositório:
```sh
git clone https://github.com/felipeAguiarCode/MegaApiDotnetCore.git
```

2️⃣ Acesse o diretório do projeto:
```sh
cd MegaApiDotnetCore
```

3️⃣ Instale as dependências:
```sh
dotnet restore
```

4️⃣ Execute a aplicação:
```sh
dotnet run
```

A API estará disponível em `http://localhost:5000`.

---

## 🛡️ Segurança

Esta API segue boas práticas de segurança, incluindo:
- **Validação de entrada de dados** para evitar injeções SQL
- **Controle de autenticação e autorização** (a ser implementado)
- **Proteção contra CORS** para restringir acessos indevidos
- **HTTPS obrigatório** para maior segurança nas requisições

---

## 📝 Contribuindo

Sinta-se à vontade para contribuir com melhorias para o projeto! Para isso:
1. Faça um **fork** do repositório
2. Crie uma **branch** para sua feature: `git checkout -b minha-feature`
3. Faça suas alterações e **commit**: `git commit -m 'Minha nova feature'`
4. Envie para o GitHub: `git push origin minha-feature`
5. Abra um **Pull Request**

---

## 📜 Licença

Este projeto está licenciado sob os termos da licença **MIT**. Para mais informações, consulte o arquivo [LICENSE](https://github.com/felipeAguiarCode/MegaApiDotnetCore/blob/main/LICENSE).

---

**Autor:** [Felipe Aguiar](https://github.com/felipeAguiarCode)

**Atualizado por:** [Jakson P.](https://github.com/jpsvcv)
