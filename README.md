# Cadastro-movimentação-de-funcionários

# Sistema de Gerenciamento de Funcionários

Este é um script em Python para gerenciar um cadastro de funcionários. Ele utiliza um banco de dados SQLite (`funcionarios.db`) para armazenar os dados e oferece um menu de console para interagir com o sistema.

Funcionalidades:
Adicionar funcionários: Cadastra um novo funcionário com nome, cargo e salário.
Listar funcionários: Exibe uma lista de todos os funcionários cadastrados, ordenados por nome.
Buscar funcionário: Permite pesquisar funcionários cujo nome contenha um termo específico.
Calcular média salarial: Mostra o número total de funcionários e a média salarial de todos eles.

Requisitos
Nenhuma biblioteca externa é necessária. O script utiliza apenas módulos padrão do Python:
  Python 3.x
  sqlite3 (incluído na biblioteca padrão do Python)

Como Usar
1.  Salve o código em um arquivo (por exemplo, `funcionarios.py`).
2.  Abra um terminal ou prompt de comando.
3.  Navegue até o diretório onde você salvou o arquivo.
4.  Execute o script:

    ```bash
    python funcionarios.py
    ```

5.  O script será iniciado e exibirá o menu principal. O arquivo de banco de dados `funcionarios.db` será criado automaticamente no mesmo diretório na primeira execução.

    ```
    SISTEMA DE FUNCIONÁRIOS
    1) Adicionar funcionário
    2) Listar funcionários
    3) Buscar funcionário por nome
    4) Calcular média salarial
    0) Sair
    Escolha:
    ```

---

Estrutura do Banco de Dados

O sistema utiliza uma única tabela chamada `funcionarios` no arquivo `funcionarios.db`.
A estrutura da tabela é definida da seguinte forma:

```sql
CREATE TABLE IF NOT EXISTS funcionarios (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    nome TEXT NOT NULL,
    cargo TEXT NOT NULL,
    salario REAL NOT NULL DEFAULT 0.0
);
