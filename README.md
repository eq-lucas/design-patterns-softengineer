# Padrões de Projeto (Design Patterns)

Este repositório apresenta a implementação prática de três Padrões de Projeto clássicos, divididos nas categorias **Comportamental**, **Criacional** e **Estrutural**.

O objetivo é demonstrar a aplicabilidade desses padrões na resolução de problemas de Engenharia de Software, utilizando **C++** para as demonstrações técnicas de baixo nível e **Python (Django)** como contexto de casos de uso reais.

---

## 📂 Organização do Projeto

O repositório está dividido em pastas por categoria. Dentro de cada pasta, você encontrará o código fonte da implementação em C++ e uma documentação específica (`README-*.md`).

### 1. [Comportamental: Strategy](./comportamental)
* **Problema:** Necessidade de alterar o algoritmo de uma classe em tempo de execução.
* **Aplicação:** Sistema de Login que suporta múltiplas estratégias de validação (Email, Telefone, Username) dinamicamente.
* **Localização:** `comportamental/codigo`

### 2. [Criacional: Factory Method](./criacional)
* **Problema:** O código precisa criar objetos sem especificar suas classes exatas.
* **Aplicação:** Um sistema de relatórios que fabrica diferentes formatos (HTML, CSV, PDF) sem acoplar o cliente à classe concreta.
* **Localização:** `criacional/codigo`

### 3. [Estrutural: Facade](./estrutural)
* **Problema:** Interface complexa e acoplada devido a múltiplos subsistemas (Banco de Dados, APIs, Validações).
* **Aplicação:** Uma fachada para o Cadastro de Usuários (Signup), orquestrando validação de formulários, transações atômicas de banco e criação de perfis.
* **Localização:** `estrutural/codigo`

---

## 📂 Subpasta NOTES

Esta pasta armazena os materiais complementares desenvolvidos para dar suporte teórico e prático ao trabalho. Aqui encontram-se os códigos originais do projeto (em **Python/Django**) que motivaram o uso dos padrões, bem como implementações de estudo em **C++** para comparação arquitetural.

### Estrutura do Conteúdo em Notes

#### 1. `notes/casos de usos/comportamental login` (Padrão Strategy)
* **Código Original (Python):** Contém a lógica real de autenticação do Django (`views.py`, `backends.py`), demonstrando a necessidade de suportar múltiplos tipos de login (Email, Telefone, Username).
* **Design Pattern demonstrado em C++:** Implementação do padrão Strategy utilizando ponteiros e polimorfismo para replicar a lógica de "autodescoberta" de estratégia usada no Python.

#### 2. `notes/casos de usos/estrutural signup` (Padrão Facade)
* **Código Original (Python):** Contém a lógica de cadastro de usuários (`views.py`, `facade.py`, `forms.py`), demonstrando como uma Facade organiza a complexidade de transações de banco de dados e validações.
* **Design Pattern demonstrado em C++:** Implementação simulando os subsistemas (Banco, Email, Transação) e o gerenciamento de memória manual (`new`/`delete`) realizado pela Facade.

---

## 🛠 Metodologia e Ferramentas

Os códigos e explicações foram organizados da seguinte forma:

* **Base Teórica:** [Refactoring Guru](https://refactoring.guru/pt-br/design-patterns).
* **Desenvolvimento e Uso de IA (Google Gemini):**
    1.  **Aplicação Prática:** A lógica dos padrões de projeto foi desenvolvida com base na teoria do *Refactoring Guru*, aplicada diretamente aos casos de uso reais de um sistema de autenticação personalizado (como no Login e Cadastro no Django) para os padrões **Estrutural** e **Comportamental**. O padrão **Criacional** foi desenvolvido a partir do estudo realizado e inspirado em cenários clássicos de uso.
    2.  **Agilidade em C++:** A ferramenta de IA foi utilizada para agilizar a codificação dos exemplos de estudo em C++, auxiliando na adaptação da lógica original (Python) para C++ seguindo os princípios de Orientação a Objetos.
    3.  **Revisão Técnica:** Todo o código gerado foi revisado pelo autor, garantindo que a implementação em C++ respeite a lógica original, os conceitos de gerenciamento de memória e os objetivos do Design Pattern estudado.