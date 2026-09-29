# 📦 Formulario de Cadastros - Cadastro de Produtos em PHP & MySQL

Este repositório contém uma aplicação web simples desenvolvida em **PHP**, **HTML5** e **MySQL** para o cadastro e validação de produtos em banco de dados.


# 📋 Sobre o Projeto

O objetivo deste projeto é fornecer uma interface onde o usuário possa cadastrar novos produtos informando o **Nome** e o **Preço**. Antes de salvar os dados no banco de dados, o sistema realiza validações via PHP no lado do servidor para garantir a integridade das informações.

# 🎯 Requisitos Atendidos:
- [x] Conexão com o banco de dados `exercicio`.
- [x] Criação da tabela `produtos` (script SQL incluso).
- [x] Formulário HTML para entrada do nome do produto e preço.
- [x] Validação em PHP no servidor:
  - Nome não pode estar vazio.
  - Preço deve ser numérico e estritamente maior que zero (`> 0`).
- [x] Exibição de mensagens de sucesso ou de erro estilizadas.
- [x] Ocultação automática da mensagem após 5 segundos via JavaScript.



# 🛠️ Tecnologias Utilizadas

- **HTML5**: Estruturação da página e do formulário.
- **PHP**: Processamento dos dados enviadas via `POST` e validação no servidor.
- **MySQL / MySQLi**: Banco de dados relacional para persistência das informações.
- **JavaScript**: Efeito visual para ocultar avisos dinamicamente.



# 🗄️ Estrutura do Banco de Dados

Para executar o projeto localmente, crie o banco de dados `exercicio` e execute o script SQL abaixo para gerar a tabela `produtos`:

```sql
CREATE DATABASE IF NOT EXISTS exercicio;
USE exercicio;

CREATE TABLE IF NOT EXISTS produtos (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nome VARCHAR(100) NOT NULL,
    preco DECIMAL(10, 2) NOT NULL
);
```



# 🚀 Como Executar o Projeto

# Pré-requisitos
- Servidor Web local com suporte a PHP e MySQL (ex: **XAMPP**, **WAMP**, **Laragon** ou **LAMP**).

# Passo a Passo

1. **Clonar o Repositório**:
   ```bash
   git clone https://github.com/CalineMyrella/Formul-rio-de-Cadastros.git
   ```

2. **Mover para o diretório do servidor**:
   - Mova a pasta do projeto para o diretório `htdocs` (se estiver usando XAMPP) ou equivalente.

3. **Configurar o Banco de Dados**:
   - Abra o **phpMyAdmin** ou o SGBD de sua preferência.
   - Execute o script SQL fornecido na seção [Estrutura do Banco de Dados](#-estrutura-do-banco-de-dados).
   - Certifique-se de ajustar as credenciais de acesso no arquivo PHP caso seu usuário/senha do MySQL sejam diferentes dos padrões (`root` / `Senai@118`).

4. **Acessar no Navegador**:
   - Abra o navegador e acesse:
     ```text
     http://localhost/Formul-rio-de-Cadastros/10a_desafio2.php
     ```

---

# 💻 Funcionalidade e Regras de Negócio

1. **Validação do Formulário**:
   - Caso o produto esteja vazio, retorna: `<span style="color: red;">Erro: O produto precisa ter um nome válido.</span>`
   - Caso o preço seja menor ou igual a `0`, retorna: `<span style="color: red;">Erro: O preço deve ser um número positivo.</span>`
   - Se os dados estiverem válidos, realiza a inserção e exibe: `<span style="color: darkgreen;">Produto cadastrado com sucesso!!</span>`
2. **Feedback ao Usuário**:
   - As mensagens exibidas somem automaticamente da tela após **5 segundos**.

---

# 📂 Arquivos do Repositório

| Arquivo | Descrição |
|---|---|
| `10a_desafio2.php` | Código completo contendo a interface HTML, processamento PHP e lógica JS. |
| `README.md` | Documentação do projeto. |

---

Desenvolvido para fins de aprendizado e avaliação de práticas em PHP & Banco de Dados.
