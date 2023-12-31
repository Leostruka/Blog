<div align="center">
<h1>My BlogLO</h1>
  Website → [https://leostruka.github.io/Blog]

Bem-vindo ao meu projeto pessoal de desenvolvimento de software!
Neste projeto, compartilharei minha jornada de aprendizado em programação e engenharia de software, abrangendo uma ampla gama de tópicos, desde conceitos fundamentais até abordagens avançadas.

</div>

## Pré-requisitos
Certifique-se de ter as seguintes ferramentas instaladas em seu sistema:
- Git: https://git-scm.com/
- Node.js: https://nodejs.org/
- npm (gerenciador de pacotes do Node.js): https://www.npmjs.com/

## Como Clonar o Projeto
1. Abra o terminal ou prompt de comando.

2. Navegue até o diretório onde deseja clonar o projeto.

3. Execute o seguinte comando para clonar o repositório:
   ```sh
   git clone https://github.com/Leostruka/Blog.git
4. Navegue até o diretório do projeto:
   ```sh
   cd seu-projeto

5. Configurar o Ambiente Local
Instale as dependências do projeto usando o npm:
   ```sh
   npm install

Realize qualquer configuração adicional necessária, como definir variáveis de ambiente ou criar arquivos de configuração.

6. Executar o Projeto
Inicie o projeto com o seguinte comando:
   ```sh
   npm start

O projeto será iniciado e estará disponível em http://localhost:1313/ (ou outra porta, se especificada).
Abra seu navegador e acesse http://localhost:1313/ para visualizar o projeto em execução.

# Como Contribuir
Se deseja contribuir para este projeto, siga estas etapas:

1. Crie um fork do projeto.
2. Crie uma nova branch com sua feature: git checkout -b minha-feature
3. Faça commit das suas alterações: git commit -m 'Adicionei uma nova feature'
4. Faça push para a branch: git push origin minha-feature
5. Abra um pull request no repositório original.

# Funcionamento do GitHub Actions
- O fluxo de trabalho é acionado por um push na branch "master" ou manualmente através da ação "workflow_dispatch".
- Define permissões de leitura de conteúdo, escrita em páginas e escrita de token de identificação.
- Gerencia a concorrência no grupo "pages" sem cancelar execuções em andamento.
- Configura o shell padrão como "bash".
## Job "build" (Construção)
- Executa na máquina com Ubuntu mais recente.
- Instala o Hugo CLI, o Dart Sass e realiza o checkout do repositório.
- Configura as páginas e instala as dependências do Node.js.
- Usa o Hugo para construir o site estático com otimizações.
- Faz upload dos arquivos gerados como um artefato.
## Job "deploy" (Implantação)
- Implanta as páginas no GitHub Pages.
- Define um ambiente chamado "github-pages" com uma URL baseada na saída do job anterior.
- Este job é executado após o job "build" ser concluído.
