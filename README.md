# 💰 FinTrack

FinTrack é uma aplicação simples de rastreamento financeiro pessoal, desenvolvida em Python, com banco de dados local (SQLite ou PostgreSQL) e arquitetura modular. O objetivo é ajudar usuários a registrar, organizar e visualizar suas transações financeiras de forma eficiente.

## 🚀 Funcionalidades

- Registro de transações (entrada e saída)
- Armazenamento em banco de dados
- Geração de relatórios financeiros (mensais, por categoria, etc.)
- Estrutura limpa e modular para expansão futura

## 🗂️ Estrutura do Projeto

```
fintrack/
├── main.py                # Arquivo principal para execução do app
├── database/
│   └── db_manager.py      # Gerenciamento da conexão com o banco de dados
├── models/
│   └── transaction.py     # Modelos de dados (ex: transações)
├── reports/
│   └── generator.py       # Geração de relatórios financeiros
├── utils/
│   └── helpers.py         # Funções auxiliares diversas
├── data/
│   └── db.sqlite3         # Banco de dados local (pode ser migrado para PostgreSQL)
├── README.md              # Este arquivo
```

## ⚙️ Tecnologias Utilizadas

- Python 3.x
- SQLite (pode ser facilmente adaptado para PostgreSQL)
- SQLAlchemy ou sqlite3 (dependendo da sua implementação)
- (Opcional) Pandas para geração de relatórios

## 📦 Instalação

1. Clone o repositório:
   ```bash
   git clone https://github.com/seu-usuario/fintrack.git
   cd fintrack
   ```

2. Crie um ambiente virtual:
   ```bash
   python -m venv venv
   source venv/bin/activate  # no Windows use: venv\Scripts\activate
   ```

3. Instale as dependências:
   ```bash
   pip install -r requirements.txt
   ```

4. Execute o projeto:
   ```bash
   python main.py
   ```

## 🛢️ Usando PostgreSQL

Para usar PostgreSQL ao invés do SQLite:

1. Instale a biblioteca:
   ```bash
   pip install psycopg2
   ```

2. Edite o arquivo `database/db_manager.py` para conectar ao seu banco PostgreSQL usando:
   ```python
   psycopg2.connect(
       dbname="fintrack_db",
       user="seu_usuario",
       password="sua_senha",
       host="localhost",
       port="5432"
   )
   ```

## 📈 Exemplo de Uso

```python
from models.transaction import Transaction
from database.db_manager import add_transaction

t = Transaction("Salário", 5000.0, "entrada", "2025-05-01")
add_transaction(t)
```

## 📋 Planejamentos Futuros

- Interface gráfica (Tkinter ou PyQt)
- API RESTful com FastAPI
- Dashboard Web com Flask ou Django
- Exportação para CSV/PDF
- Suporte a múltiplos usuários

## 📄 Licença

Este projeto está licenciado sob a MIT License. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

---

Desenvolvido com 💻 por Diego Honório Magalhães
