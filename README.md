# 🎓 Sistema de Gerenciamento Acadêmico Simplificado (SGA)

## Descrição do Projeto

# Sistema Simplificado para Gerenciamento Acadêmico (SGA). Implementado em Java, este projeto oferece funcionalidades para cadastro de alunos, criação de disciplinas, alocação em turmas e controle eficiente do processo de matrícula.

# O objetivo principal é fornecer uma solução básica e funcional para administrar os registros acadêmicos de forma clara e organizada, ideal para estudos e demonstrações de conceitos de programação orientada a objetos e persistência de dados.

## 🧭 Índice
* [Recursos e Tecnologias](#-recursos-e-tecnologias)
* [Estrutura do Projeto](#-estrutura-do-projeto)
* [Regras de Negócio (Requisitos)](#-regras-de-negócio-requisitos)
* [Como Executar](#-como-executar)

## Funcionalidades Principais

O sistema permite realizar as seguintes operações:

* **Matrícula de Alunos:** Registrar novos estudantes no sistema.
* **Gestão de Disciplinas:** Criar, visualizar e gerenciar o catálogo de disciplinas disponíveis.
* **Alocação em Turmas:** Vincular alunos a turmas específicas e disciplinas.
* **Visualização de Dados:** Consultar listas de alunos, turmas e históricos de matrícula.


## 💻 Recursos e Tecnologias

| Categoria | Tecnologia | Justificativa |
| :--- | :--- | :--- |
| **Linguagem Principal** | **Java 21 (LTS)** | Foco em sintaxe moderna (e.g., switch expressions) e POO. |
| **Build Tool** | **Apache Maven** | Gerenciamento de dependências e ciclo de vida do projeto. |
| **Persistência** | **Serialização de Objetos** | Cumprimento do requisito de persistência em formato de arquivo binário (`.dat`). |
| **Design** | **Modularização (Pacotes)** | Uso de camadas `model`, `data`, `service` e `main` para separação de responsabilidades. |

## 📂 Estrutura do Projeto (POO e Modularização)

O sistema segue o padrão de camadas (Service Layer) e é dividido nos seguintes pacotes:

* **`model`**: Contém as classes de entidades. A classe base **`Pessoa`** implementa **Herança** para as classes **`Aluno`** e **`Professor`**.
* **`data`**: Responsável pela persistência. Possui a interface `IRepositorio` e a implementação `RepositorioArquivo` (Serialização).
* **`service`**: Contém a classe `ServicoAcademico`, que aplica as **Regras de Negócio** (matrícula, lançamento de notas).
* **`main`**: Classe `MainApp` com a interface de console.

* ## ▶️ Como Executar

O projeto é configurado com Maven.

1.  **Clonar:**
    ```bash
    git clone [SUA_URL_AQUI]
    ```
2.  **Compilar e Empacotar (Terminal/CMD):**
    ```bash
    mvn clean install
    ```
3.  **Executar no Eclipse:**
    * Importe o projeto como um projeto Maven.
    * Execute a classe `MainApp.java` (Run As -> Java Application).
