# Guia de Contribuição

Obrigado pelo interesse em contribuir com o projeto! Este documento reúne as instruções para configurar o ambiente local e enviar alterações de forma padronizada.

## 1. Pré-requisitos

Antes de começar, certifique-se de ter instalado em sua máquina:
- **Git** (para controle de versão e envio de alterações).
- **Navegador web atualizado** (Chrome, Firefox, Edge ou Safari) para executar e testar o jogo.
- **Editor de código** de sua preferência (recomendado: Visual Studio Code).

## 2. Como clonar o repositório

1. Abra o terminal na pasta onde deseja salvar o projeto.
2. Execute o comando para clonar o fork da equipe:
   ```bash
   git clone [https://github.com/Guilhermeleandro-N/github-games.git](https://github.com/Guilhermeleandro-N/github-games.git)
   ```
3. Acesse a pasta do projeto:
   ```bash
   cd github-games
   ```

## 3. Como executar o jogo localmente

Como o projeto é construído com HTML, CSS e JavaScript puro, não é necessário instalar dependências externas ou servidores complexos:

1. Localize o arquivo `index.html` na raiz da pasta `github-games`.
2. Dê um duplo clique no arquivo para abri-lo no seu navegador padrão — ou execute via terminal (Windows):
   ```powershell
   start index.html
   ```
3. *(Opcional)* Caso utilize o VS Code, você também pode clicar com o botão direito em `index.html` e selecionar **Open with Live Server**.

## 4. Como criar branches para novas alterações

Toda alteração deve ser vinculada a uma Issue aberta e desenvolvida em uma branch própria a partir da `main` atualizada:

1. Garanta que sua branch `main` local está sincronizada com o repositório remoto:
   ```bash
   git switch main
   git pull origin main
   ```
2. Crie e acesse uma nova branch utilizando o prefixo correspondente à categoria da Issue (`fix/`, `feature/`, `enhancement/` ou `docs/`) seguido do número da Issue:
   ```bash
   git switch -c fix/issue-17-pausar-ao-reiniciar
   ```

## 5. Como registrar commits e enviar Pull Requests

1. Após implementar e testar suas alterações no navegador, verifique os arquivos modificados:
   ```bash
   git status
   ```
2. Adicione os arquivos e registre um commit com mensagem clara e objetiva:
   ```bash
   git add .
   git commit -m "fix: pausa o jogo ao abrir confirmacao de reinicio"
   ```
3. Envie sua branch para o repositório remoto:
   ```bash
   git push -u origin fix/issue-17-pausar-ao-reiniciar
   ```
4. No GitHub, acesse a aba **Pull requests** > **New pull request**.
5. Confira se a base de destino é a branch `main` do fork da equipe (`Guilhermeleandro-N/github-games`) e a branch de comparação é a sua branch de trabalho.
6. Na descrição do Pull Request, inclua `Closes #<numero-da-issue>` para vincular e fechar a Issue automaticamente após o merge.

## 6. Boas práticas para contribuir

- **Nunca faça push diretamente na `main`:** todas as mudanças devem passar por Pull Request.
- **Teste antes de enviar:** abra o jogo no navegador e valide os critérios de conclusão descritos na Issue antes de abrir o PR.
- **Mantenha o escopo focado:** resolva apenas uma Issue por branch/Pull Request.
- **Solicite revisão:** atribua sempre outro integrante da equipe como *Reviewer* antes de concluir o merge.