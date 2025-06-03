# [TRABALHO]

Bem-vindo ao [TRABALHO-CYPRESS]! Este é um projeto frontend que demonstra as principais funcionalidades de uma aplicação web, com testes end-to-end implementados usando Cypress para garantir a qualidade e a robustez do sistema.

---

## 🚀 Como Rodar a Aplicação

Para colocar a aplicação em funcionamento na sua máquina local, siga os passos abaixo:

1.  **Clone o repositório:**
    ```bash
    git clone [LINK_PARA_SEU_PROJETO_FRONTEND]
    cd [NOME_DO_SEU_PROJETO]
    ```

2.  **Instale as dependências:**
    Certifique-se de ter o Node.js e o npm (ou Yarn) instalados.
    ```bash
    npm install
    # ou
    yarn install
    ```

3.  **Inicie o servidor de desenvolvimento:**
    Este comando varia dependendo do seu framework (React, Vue, Angular, etc.). Aqui estão exemplos comuns:

    * **Para projetos React (Create React App):**
        ```bash
        npm start
        # ou
        yarn start
        ```
    * **Para projetos Vue (Vue CLI):**
        ```bash
        npm run serve
        # ou
        yarn serve
        ```
    * **Para projetos Angular (Angular CLI):**
        ```bash
        ng serve --open
        ```
    * **Para projetos simples (servidor HTTP como `http-server`):**
        Se o seu projeto for estático e não tiver um script de `start` no `package.json`, você pode precisar de um servidor HTTP.
        ```bash
        npm install -g http-server
        http-server .
        ```

    Após iniciar, a aplicação geralmente estará disponível em `http://localhost:3000` (ou outra porta indicada no seu terminal).

---

## 🧪 Como Executar os Testes Cypress

Os testes end-to-end foram desenvolvidos com Cypress para simular interações reais do usuário e verificar o comportamento da aplicação.

**Pré-requisito:** Certifique-se de que a **aplicação frontend esteja rodando** em `http://localhost:3000` (ou na porta configurada) antes de executar os testes.

1.  **Abra o Cypress Test Runner (Modo Interativo):**
    Este comando abrirá a interface gráfica do Cypress, onde você pode selecionar e rodar os testes individualmente.
    ```bash
    npx cypress open
    ```
    No Cypress Test Runner, escolha `E2E Testing` e, em seguida, selecione os arquivos de teste (`.cy.js`) na lista para executá-los.

2.  **Execute os testes via linha de comando (Modo Headless):**
    Este comando executará todos os testes em modo "headless" (sem interface gráfica), o que é ideal para integração contínua (CI).
    ```bash
    npx cypress run
    ```
    Você verá o progresso dos testes diretamente no seu terminal.

---

## ✅ Funcionalidades Testadas

Os testes Cypress cobrem os seguintes fluxos principais da aplicação:

### 🔐 Login
* **Exibir a tela de login:** Verifica se a página de login é carregada corretamente.
* **Falhar com credenciais inválidas:** Testa o comportamento da aplicação ao tentar fazer login com usuário e/ou senha incorretos.
* **Realizar login com sucesso:** Valida o fluxo de login com credenciais válidas, garantindo o acesso do usuário.

### 🧾 Cadastro
* **Acessar tela de cadastro:** Garante que a página de cadastro esteja acessível.
* **Exibir erro com email inválido:** Verifica a validação de formato de e-mail no formulário de cadastro.
* **Exibir erro com senha fraca (ou senhas que não coincidem):** Testa as validações de senha, como complexidade ou confirmação.
* **Criar conta com sucesso:** Simula o processo completo de criação de uma nova conta de usuário.

### 📬 Formulário de Contato
* **Exibir o formulário de contato:** Confirma que o formulário está visível e pronto para preenchimento.
* **Validar campos obrigatórios no formulário:** Testa se os campos requeridos são devidamente validados e impedem o envio sem preenchimento.
* **Enviar formulário com sucesso:** Garante que o formulário pode ser preenchido e enviado com sucesso.

### 🔗 Navegação
* **Navegar para a página de tarefas (Exemplo):** Testa a transição para uma página específica (ajuste o nome da página conforme seu projeto).
* **Voltar para a home:** Verifica a funcionalidade de retorno para a página inicial da aplicação.
