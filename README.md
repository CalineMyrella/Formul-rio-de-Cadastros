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
