
# SGHSS - Sistema de Gestão Hospitalar e de Serviços de Saúde

Este projeto consiste no desenvolvimento de uma API Back-End para um Sistema de Gestão Hospitalar e de Serviços de Saúde (SGHSS), com o objetivo de automatizar e organizar processos hospitalares, como cadastro de pacientes, profissionais de saúde, agendamento de consultas, gerenciamento de prontuários e registrar atividades essenciais por meio de log, garantindo a auditoria e conformidade legal. Além de Realizar a autenticação e o controle de acesso do usuário do sistema, assim assegurando a proteção, integridade e confidencialidade dos dados armazenados.

O sistema foi desenvolvido utilizando Python e o framework FastAPI, seguindo boas práticas de arquitetura, segurança e organização de código.


---

## Tecnologias utilizadas

- **Python 3.12**
- **FastAPI** - Framework para construção de APIs REST
- **SQLAlchemy** - ORM para mapeamento objeto-relacional
- **PostgreSQL** - Banco de dados relacional
- **Alembic** - Controle de migrações do banco de dados
- **Uvicorn** - Servidor ASGI
- **Pydantic** - Validação e serialização de dados
- **Passlib** - Hash de senha
- **PyJWT (Token JWT)** - Autenticação e autorização
- **Swagger / OpenAPI** – Documentação automática da API
- **Postman** - Testar endpoints da API, simular requisições HTTP e validar os fluxos de autenticação, cadastro e manipulação de dados
- **Git e GitHub** - Controle de versão realizado por meio do Git, com o repositório remoto hospedado no GitHub

---

---

## Funcionalidades principais

- **Autenticação com JWT**
- **CRUD de Usuários**
- **CRUD de Pacientes**
- **CRUD de Consultas**
- **CRUD de Prontuários**
- **Logs automáticos** das operações que são realizadas no sistema

---

## Requesistos Funcionais 

- Cadsatro de Usuário
- Login de Usuário
- Cadastro de Pacientes 
- Consulta de Pacientes
- Atualização de Pacientes
- Excllusão de Pacientes
- Agendamento de Consultas
- Consulta de Agendamento
- Atualização de Agendamentos
- Exclusão de Agendamentos
- Cadastro de prontuários
- Consulta de Prontuários
- Registro de Logs
- Teleconsulta 
---

---
## Requisitos não Funcionais

- Segurança da Informação 
- Disponibilidade
- Usabilidade
- Perfomance
- Consistência de Dados 
- Documentação
- Versionamento 
- Armazenamento de Logs

---

---

## Estrutura do Projeto

```plaintext
app/
├── auth/ # Autenticação e JWT (segurança, JWT, logs)
├── crud/ # Operações de banco de dados 
├── database.py # Conexão com o banco de dados
├── main.py # Arquivo principal que inicializa a aplicação FastAPI
├── models/ # Modelos ORM que representam as tabelas do banco de dados
├── routers/ # Rotas da aplicação
├── schemas/ # Schemas Pydantic utilizados para validação de dados de entrada/saída
└── alembic/ # Migrações do banco de dados
```
---

## Como rodar o projeto localmente

### Pré-requisitos

- Python instalado (versão 3.10 ou superior)
- PostgreSQL instalado e rodando

### Clone o repositório

```bash
git clone https://github.com/Scarlet-Code/https://github.com/Scarlet-Code/SGHSS-.git
cd SGHSS
```

### Crie e ative um ambiente virtual

```bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate   # Windows
```

### Instale as dependências

```bash
pip install -r requirements.txt
```

### Configure as variáveis de ambiente

Crie um arquivo `.env` (se desejar centralizar configs) com:

```env
DATABASE_URL=postgresql://usuario:senha@localhost:5432/sghss
SECRET_KEY=sua_chave_secreta
ALGORITHM=HS256
ACCESS_TOKEN_EXPIRE_MINUTES=60
```

### Banco de Dados

Execute as migrações com o Alembic:


```bash
alembic uprade head
```

### Execute a Aplicação

```bash
uvicorn main:app --reload
```

---

## Documentação 

- A documentação da API é gerada automaticamente pelo FastAPI e pode ser acessada via Swagger. Acesse a documentação em:

```plaintext
Swagger UI: http://127.0.0.1:8000/docs
```

---

---

## Autor

Desenvolvido por [Yara Godoy](https://github.com/Scarlet-Code/SGHSS-.git). 
O projeto foi desenvolvido para fins acadêmicos como parte de conclusção de curso, com foco em Back-End.

---

## Status do Projeto

**Concluído - TCC 2025**
