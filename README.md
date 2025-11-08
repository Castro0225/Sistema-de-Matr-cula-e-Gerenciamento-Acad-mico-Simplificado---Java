# 🎓 Sistema de Gerenciamento Acadêmico Simplificado (SGA)
## 🎯 Projeto Final em Java | Ênfase em POO, Herança e Persistência em Arquivo

<br>

> **Sistema Simplificado para Gerenciamento Acadêmico (SGA).** Implementado em **Java 21** e utilizando a metodologia **POO**, este projeto oferece a **gestão completa do ciclo de vida acadêmico**. Ele permite o cadastro de alunos e disciplinas, alocação em turmas e o controle eficiente do **processo de matrícula**.
>
> ---
> 
> O objetivo principal é fornecer uma solução **básica e funcional** para administrar os registros acadêmicos de forma clara e organizada, servindo como uma **demonstração prática** de conceitos de programação orientada a objetos e persistência de dados (Serialização em Arquivo).

---
## 🧭 Índice

* [Funcionalidades Principais](#funcionalidades-principais)
* [Recursos e Tecnologias](#recursos-e-tecnologias)
* [Estrutura do Projeto](#estrutura-do-projeto-poo-e-modularização)
* [Como Executar](#como-executar)
---

## Funcionalidades Principais

O sistema é uma aplicação de console que permite a **gestão completa de registros acadêmicos** através das seguintes operações:

* **Cadastros:** Registro de **Alunos**, **Professores** e **Disciplinas**.
* **Matrícula:** **Alocação de Alunos em Disciplinas** com geração de registro único.
* **Avaliação:** **Lançamento de notas** com atualização automática do status (Aprovado / Reprovado).
* **Histórico:** **Consulta de matrículas** por aluno e visualização do histórico acadêmico completo.
* **Persistência:** Todos os dados são salvos em arquivos `.dat` utilizando Serialização, mantendo o estado entre as sessões.

---

##  Recursos e Tecnologias

| Categoria | Tecnologia | Justificativa |
| :--- | :--- | :--- |
| **Linguagem Principal** | **Java 21** | Foco em sintaxe moderna e Programação Orientada a Objetos. |
| **Build Tool** | ** Maven** | Gerenciamento padronizado de dependências e ciclo de vida do projeto. |
| **Persistência** | **Serialização de Objetos** | Cumprimento do requisito de persistência em formato de arquivo binário (`.dat`). |
| **Design** | **Modularização (Pacotes)** | Uso de camadas `model`, `data`, `service` e `main` para separação de responsabilidades. |

---

## Estrutura do Projeto (POO e Modularização)

O sistema segue o **Padrão de Camadas (Service Layer)** para garantir baixo acoplamento e alta coesão:

* **`model`**: Contém as classes de entidades. A classe base abstrata **`Pessoa`** implementa **Herança** para as classes **`Aluno`** e **`Professor`**.
* **`data`**: Responsável pela persistência. Possui a interface `IRepositorio` e a implementação `RepositorioArquivo` (utilizando `java.io.Serializable`).
* **`service`**: Contém a classe `ServicoAcademico`, que aplica as **Regras de Negócio** (ex: validação de matrícula e lógica de notas).
* **`main`**: Classe `MainApp` com o método `main()` para a interface de console.

---

##  Como Executar

O projeto é configurado para ser executado via **Apache Maven** no terminal ou diretamente no Eclipse.

1.  **Clonar o Repositório:**
    ```bash
    git clone [SUA_URL_AQUI]
    ```
2.  **Compilar e Empacotar (Terminal/CMD):**
    * Navegue até a pasta raiz do projeto (onde está o `pom.xml`).
    * Execute:
        ```bash
        mvn clean install
        ```
3.  **Executar no Eclipse:**
    * Importe o projeto como um projeto Maven.
    * Execute a classe **`MainApp.java`** (clique direito $\rightarrow$ Run As $\rightarrow$ Java Application).
