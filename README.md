# Sistema de Gestão de Funcionários

## Descrição

Este projeto consiste em um sistema de banco de dados para gerenciar funcionários, departamentos e salários em uma empresa. O sistema permite o registro e a atualização das informações dos funcionários, a gestão dos departamentos e dos salários.

## Estrutura do Banco de Dados

O banco de dados é composto pelas seguintes tabelas:

- **Departamentos**: Armazena informações sobre os departamentos da empresa.
  - `id_departamento` (INT, PRIMARY KEY, AUTO_INCREMENT)
  - `nome` (VARCHAR(50), NOT NULL)

- **Funcionarios**: Armazena informações sobre os funcionários da empresa.
  - `id_funcionario` (INT, PRIMARY KEY, AUTO_INCREMENT)
  - `nome` (VARCHAR(100), NOT NULL)
  - `cargo` (VARCHAR(50), NOT NULL)
  - `salario` (DECIMAL(10, 2), NOT NULL)
  - `id_departamento` (INT, FOREIGN KEY REFERENCES Departamentos(id_departamento))

- **Salarios**: Armazena o histórico de salários dos funcionários.
  - `id_salario` (INT, PRIMARY KEY, AUTO_INCREMENT)
  - `id_funcionario` (INT, FOREIGN KEY REFERENCES Funcionarios(id_funcionario))
  - `data` (DATE, NOT NULL)
  - `valor` (DECIMAL(10, 2), NOT NULL)

## Como Usar

1. **Configuração Inicial**:
   - Crie um banco de dados chamado `GestaoFuncionarios`.
   - Execute os scripts SQL fornecidos para criar as tabelas no banco de dados.

2. **Inserção de Dados**:
   - Insira dados de exemplo nas tabelas para testar o sistema.

3. **Consultas**:
   - Utilize os comandos SQL fornecidos para consultar informações, como listar funcionários e seus departamentos, calcular salários totais por departamento e verificar salários históricos.

4. **Atualizações e Exclusões**:
   - Use comandos SQL para atualizar salários e modificar ou excluir registros conforme necessário.

## Requisitos

- Sistema de gerenciamento de banco de dados SQL (MySQL, PostgreSQL, etc.)
- Ferramenta de acesso ao banco de dados (como MySQL Workbench ou pgAdmin)

## Licença

Este projeto está licenciado sob a [MIT License](LICENSE).

