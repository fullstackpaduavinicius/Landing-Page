Landing Page com Integração ao Google Sheets 📝
Sobre o Projeto
Esta Landing Page foi desenvolvida para capturar informações dos usuários, como nome, e-mail e mensagens, armazenando os dados diretamente em uma planilha do Google Sheets. O projeto utiliza HTML, CSS e JavaScript para criar um design atraente e funcional, além de garantir a integração perfeita com o Google Sheets via API.

Funcionalidades
📋 Captura de dados de usuários (ex.: nome, e-mail, mensagem).
📊 Integração em tempo real com Google Sheets para armazenar as informações capturadas.
📱 Design responsivo, adaptado para dispositivos móveis e desktops.
🖌️ Layout moderno e personalizável.

Tecnologias Utilizadas
HTML5: Estrutura da página.
CSS3: Estilização e responsividade.
JavaScript: Lógica de validação de formulários e integração com Google Sheets.
Google Apps Script: Configuração do script para receber os dados na planilha.

Como Usar
Pré-requisitos
Uma conta Google para criar e acessar a planilha do Google Sheets.
Navegador atualizado para acessar a landing page.
Configuração
Crie a Planilha do Google Sheets

Acesse o Google Sheets e crie uma nova planilha.
Nomeie as colunas (ex.: Nome, E-mail, Mensagem, Data).
Configure o Google Apps Script

Vá em Extensões > Apps Script na planilha.
Cole o seguinte código no editor de script:
javascript
Copiar código
function doPost(e) {
  const sheet = SpreadsheetApp.getActiveSpreadsheet().getActiveSheet();
  const params = JSON.parse(e.postData.contents);
  sheet.appendRow([params.nome, params.email, params.mensagem, new Date()]);
  return ContentService.createTextOutput("Dados recebidos com sucesso");
}
Salve o script, publique-o como Aplicativo Web e copie o link gerado.
Adapte o código do formulário no script.js

Substitua a URL do Apps Script no arquivo script.js:
javascript

const scriptURL = "COLE_A_URL_DO_SEU_APLICATIVO_WEB_AQUI";
Clone o repositório e execute o projeto

Clone este repositório:
bash
Copiar código
git clone https://github.com/fullstackpaduavinicius/Landing-Page.git
Abra o arquivo index.html no navegador.
Estrutura de Arquivos

landing-page/
│
├── index.html          # Estrutura da landing page
├── styles.css          # Estilo da página
├── script.js           # Lógica e integração com Google Sheets
└── README.md           # Documentação do projeto

Contribuição
Contribuições são sempre bem-vindas! Siga os passos abaixo para contribuir:

Faça um fork do repositório.
Crie uma branch com sua funcionalidade:

git checkout -b minha-funcionalidade
Faça o commit das alterações:

git commit -m 'Adiciona nova funcionalidade'
Faça o push para a branch:

git push origin minha-funcionalidade
Abra um pull request.

Autor
Desenvolvido por Padua vinicius (TROVÃo)
Entre em contato via LinkedIn: https://www.linkedin.com/in/ivan-vin%C3%ADcius-832821330/

