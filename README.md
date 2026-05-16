# Painel de Produtividade Matinal Pessoal

Um dashboard pessoal moderno e dinâmico, focado em produtividade para o início do dia. O projeto integra-se diretamente com as APIs do Google (Gmail, Calendar e Tasks) para fornecer um resumo em tempo real da sua rotina diária assim que você acorda.

## Funcionalidades

- **Design Moderno e Responsivo**: Interface com tema escuro (*dark mode*), efeitos de *glassmorphism*, gradientes suaves e micro-interações que oferecem uma experiência premium.
- **Autenticação com o Google**: Login seguro via Google Identity Services (GSI) com escopo de acesso apenas leitura (*read-only*), garantindo a privacidade e segurança dos seus dados.
- **Resumo de E-mails**: Exibição da quantidade de e-mails não lidos na caixa de entrada em tempo real.
- **Agenda do Dia**: Integração com o Google Calendar para listar as próximas reuniões e eventos do seu dia, destacando o evento mais próximo.
- **Tarefas Pendentes**: Sincronização com o Google Tasks para mostrar a quantidade de tarefas não concluídas e quantas vencem no dia atual.
- **Gráfico de Volume de E-mails**: Visualização em barras (usando Chart.js) mostrando a quantidade de e-mails recebidos nos últimos 7 dias.

## Tecnologias Utilizadas

- **Front-end Core**: HTML5, CSS3 (Vanilla) e JavaScript (ES6+).
- **Integração**: [Google Identity Services (GSI)](https://developers.google.com/identity/gsi/web) para autenticação OAuth2.
- **APIs**: Gmail API, Google Calendar API e Google Tasks API.
- **Visualização de Dados**: [Chart.js](https://www.chartjs.org/) para o gráfico de e-mails da semana.
- **Tipografia**: Fonte [Inter](https://fonts.google.com/specimen/Inter) (Google Fonts).

## Como executar o projeto localmente

Para rodar este projeto em sua máquina local, você precisará de um servidor web simples (como a extensão *Live Server* do VSCode ou `http-server` via Node.js). O projeto não requer *builds* complexos por ser construído com tecnologias web padrão (Vanilla).

1. Clone o repositório:
   ```bash
   git clone https://github.com/SEU_USUARIO/NOME_DO_REPOSITORIO.git
   ```

2. Acesse a pasta do projeto:
   ```bash
   cd NOME_DO_REPOSITORIO
   ```

3. Abra o arquivo `index.html` usando um servidor local. Por exemplo, se estiver usando a extensão *Live Server* no VSCode, clique em "Go Live".

### Configuração da API do Google (Opcional para seu próprio fork)

O projeto já contém um `CLIENT_ID` configurado no arquivo `index.html`. No entanto, se você quiser configurar o seu próprio no Google Cloud Console:

1. Acesse o [Google Cloud Console](https://console.cloud.google.com/).
2. Crie um novo projeto.
3. Ative as APIs: **Gmail API**, **Google Calendar API** e **Google Tasks API**.
4. Configure a Tela de Consentimento OAuth.
5. Crie credenciais do tipo **ID do cliente OAuth** para Aplicação Web.
6. Adicione `http://localhost:5500` (ou a porta que estiver usando) em "Origens JavaScript autorizadas".
7. Substitua o valor da constante `CLIENT_ID` no arquivo `index.html` pelo seu novo ID de cliente.

## Privacidade

O aplicativo solicita apenas permissões de **leitura** (`readonly`) para a sua conta Google. Nenhum dado é enviado, armazenado em servidores de terceiros ou modificado em sua conta. Toda a integração ocorre diretamente entre o seu navegador e as APIs do Google.

## Contribuição

Contribuições são sempre bem-vindas! Sinta-se à vontade para abrir uma *issue* ou enviar um *pull request*.

---
Feito para maior produtividade no início do seu dia!
