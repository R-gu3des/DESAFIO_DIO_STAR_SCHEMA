# Desafio do Star Schema

## Visão Geral
Este projeto implementa um modelo de dados Star Schema para facilitar a análise eficiente de dados e relatórios para uma instituição educacional. O esquema inclui tabelas de fato e dimensões que representam matrículas de alunos, cursos, professores e departamentos.

## Design do Esquema
### Tabela de Fato
- **Fato Matrícula**
  - **idMatricula** (INT) - Chave primária para registros de matrícula exclusivos.
  - **Ano** (INT) - Ano da matrícula.
  - **Semestre** (INT) - Semestre da matrícula.
  - **Nota** (DECIMAL(5,2)) - Nota final do curso.
  - **idAluno** (INT) - Chave estrangeira referenciando a **Dimensão Aluno**.
  - **idCurso** (INT) - Chave estrangeira referenciando a **Dimensão Curso**.
  - **idDepartamento** (INT) - Chave estrangeira referenciando a **Dimensão Departamento**.
  - **idProfessor** (INT) - Chave estrangeira referenciando a **Dimensão Professor**.

### Tabelas de Dimensão
- **Dimensão Aluno**
  - **idAluno** (INT) - Chave primária.
  - **Nome** (VARCHAR(100)) - Nome do aluno.
  - **DataNascimento** (DATE) - Data de nascimento do aluno.
  - **Email** (VARCHAR(100)) - Email do aluno.
  
- **Dimensão Curso**
  - **idCurso** (INT) - Chave primária.
  - **NomeCurso** (VARCHAR(100)) - Nome do curso.
  
- **Dimensão Professor**
  - **idProfessor** (INT) - Chave primária.
  - **NomeProfessor** (VARCHAR(100)) - Nome do professor.
  
- **Dimensão Departamento**
  - **idDepartamento** (INT) - Chave primária.
  - **NomeDepartamento** (VARCHAR(100)) - Nome do departamento.

## Propósito
O Star Schema é projetado para otimizar o desempenho das consultas e simplificar a estrutura de dados, facilitando a geração de insights sobre o desempenho dos alunos, a eficácia dos cursos e a eficiência dos departamentos.

## Uso
1. Carregue o esquema no seu banco de dados.
2. Insira dados nas tabelas de dimensão e na tabela de fato.
3. Use consultas SQL para analisar e visualizar os dados.
