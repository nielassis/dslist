# 🕹️ DSList - Gerenciamento de Listas de Jogos

Bem-vindo ao **DSList**, uma aplicação que permite organizar listas de jogos com funcionalidade de reordenação de itens, proporcionando uma experiência interativa e eficiente para os usuários.

---

## 🚀 Funcionalidades

- 📋 **Gerenciamento de listas de jogos** – visualização e reordenação de jogos em diferentes listas.
- 🔄 **Reordenação de jogos** – Alteração da posição de jogos dentro das listas de forma dinâmica.
- 🗂️ **API RESTful** – Endpoints organizados para facilitar a integração com o frontend.
- 🔍 **Consulta eficiente** – Busca de jogos por listas específicas.

---

## 🛠️ Tecnologias utilizadas

### Backend:

- ![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
- ![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)
- ![PostgreSQL](https://img.shields.io/badge/PostgreSQL-316192?style=for-the-badge&logo=postgresql&logoColor=white)
- ![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)

### Ferramentas adicionais:

- ![Maven](https://img.shields.io/badge/Maven-C71A36?style=for-the-badge&logo=apachemaven&logoColor=white)
- ![Spring Web](https://img.shields.io/badge/Spring%20Web-6DB33F?style=for-the-badge&logo=spring&logoColor=white)
---

## 📂 Estrutura do Projeto

```
dslist
│-- src
│   ├── main
│   │   ├── java/com/project/dslist
│   │   │   ├── controllers    # Controladores da API
│   │   │   ├── dto             # Data Transfer Objects
│   │   │   ├── entities        # Entidades JPA
│   │   │   ├── projections     # Interfaces para consultas otimizadas
│   │   │   ├── repositories    # Interfaces de acesso a dados
│   │   │   ├── services        # Regras de negócio
│   │   │   └── DslistApplication.java  # Ponto de entrada da aplicação
│   ├── resources
│   │   ├── application.properties  # Configuração da aplicação
│-- pom.xml      # Configurações do projeto Maven
│-- README.md    # Documentação do projeto
```

---

## 🚀 Como executar o projeto

### ⚙️ Pré-requisitos

- [Java 17](https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html)
- [Maven](https://maven.apache.org/)
- [Docker](https://www.docker.com/) (Opicional)

---
1. Clone o repositório:

   ```bash
   git clone https://github.com/seu-usuario/dslist.git
   cd dslist
   ```

2. Configure o banco de dados PostgreSQL (OPICIONAL).
3. Execute a aplicação:

   ```bash
   ./mvnw spring-boot:run
   ```
---

## 📖 Endpoints da API

### Lista todos os jogos cadastrados

```bash
GET /games
```

### Obtem o jogo cadastrado pelo ID

```bash
GET /games/{id}
```


### Lista todas as listas de jogos

```bash
GET /lists
```

### Obtem Jogos de uma lista específica

```bash
GET /lists/{listId}/games
```

### Reordena jogos na lista

```bash
POST /lists/{listId}/replacement
Body:
{
  "sourceIndex": 1,
  "targetIndex": 3
}
```

---

## 🤝 Contribuição
### Contribuições são bem vindas! Para contribuir:
1. Faça um fork do repositório.
2. Crie uma branch com sua feature: `git checkout -b minha-feature`
3. Faça um commit das suas mudanças `git commit -m "feat: adiciona nova funcionalidade"`
4. Faça um push para a branch: `git push origin minha-feature`
5. Abra um PR (Pull Request)