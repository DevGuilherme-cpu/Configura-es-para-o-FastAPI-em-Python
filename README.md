# Configura-es-para-o-FastAPI-em-Python

*Template FastAPI - Instalação e Uso:* 
Toda vez que você for começar um projeto novo, você não precisa copiar o pyproject.toml inteiro manualmente e colar. O jeito correto de iniciar um projeto com o Poetry e instalar essas ferramentas é rodando os comandos abaixo no seu PowerShell:

1. Criar o esqueleto do projeto:

poetry new --flat nome_do_seu_projeto

cd nome_do_seu_projeto

2. Instalar o FastAPI (Dependência Principal):


poetry add "fastapi[standard]"

3. Instalar as Ferramentas de Desenvolvimento:

O comando --group dev garante que essas bibliotecas não vão para o servidor de produção (como o Render), elas ficam só no seu computador para te ajudar a programar:

poetry add --group dev pytest pytest-cov taskipy ruff typos

4. Configurar os Atalhos (Opcional, mas recomendado):

Depois de rodar os comandos acima, o Poetry já terá criado um pyproject.toml para você. Você só precisa abrir ele no VS Code, copiar os blocos [tool.taskipy.tasks], [tool.ruff] e [tool.pytest] do nosso template e colar no final do arquivo.

5. Atalhos Mágicos (Taskipy) que você acabou de ganhar:

Em vez de digitar comandos gigantescos, agora você só precisa digitar task e a ação que você quer fazer no seu terminal:

- task run: Liga o seu servidor FastAPI.

- task format: Arruma automaticamente todo o seu código (espaçamentos, aspas duplas por aspas simples, etc) deixando ele nos padrões profissionais.

- task lint: Avisa se você escreveu alguma variável que não está usando ou importou algo errado.

- task test: Roda todos os seus testes automatizados de uma vez só.
