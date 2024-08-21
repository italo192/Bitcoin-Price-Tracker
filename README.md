# Rastreador de Preços do Bitcoin

Um script Python que monitora o preço do Bitcoin em tempo real e envia alertas por e-mail quando o valor cai abaixo de um limite definido pelo usuário.

## Funcionalidades

- Obtém o preço atual do Bitcoin em BRL usando a API da CoinGecko.
- Envia um e-mail de alerta quando o preço do Bitcoin cai abaixo de um limite definido pelo usuário.
- Automatiza o rastreamento e envio de alertas a cada 10 minutos.

## Tecnologias Utilizadas

- Python 3.7+
- `requests` (para fazer requisições HTTP)
- `smtplib` (para envio de e-mails)
- `email` (para criação de e-mails em formato HTML)
- `decouple` (para gerenciar variáveis de ambiente)
- `schedule` (para agendamento de tarefas)

## Como Usar

1. **Instalação das Dependências:**
   - Certifique-se de ter o Python 3.7+ instalado.
   - Instale as dependências necessárias:

     ```sh
     pip install requests python-decouple schedule
     ```

2. **Configuração do Ambiente:**
   - Crie um arquivo `.env` na raiz do projeto e adicione suas credenciais de e-mail:

     ```env
     EMAIL_USER=seu_email@gmail.com
     EMAIL_PASS=sua_senha_de_app
     RECIPIENT_EMAIL=email_destinatario1@gmail.com,email_destinatario2@gmail.com
     ```

   > **Nota:** Utilize uma senha de aplicativo gerada no Gmail em vez da sua senha principal por questões de segurança.

3. **Execução:**
   - Clone este repositório: `git clone https://github.com/seu_usuario/bitcoin-price-tracker.git`
   - Navegue até o diretório do projeto: `cd bitcoin-price-tracker`
   - Execute o script Python:

     ```sh
     python tracker.py
     ```

4. **Uso:**
   - Insira o valor limite para o alerta do Bitcoin quando solicitado.
   - O script começará a rastrear o preço do Bitcoin e enviará e-mails de alerta conforme necessário.

## Personalização

- **Intervalo de Tempo:** O script está configurado para verificar o preço a cada 10 minutos. Para ajustar o intervalo, edite a linha onde o agendamento é definido:

  ```python
  schedule.every(10).minutes.do(check_price, threshold)
Destinatários do E-mail: Adicione ou remova destinatários editando a variável RECIPIENT_EMAIL no arquivo .env.
Contribuição
Sinta-se à vontade para fazer um fork do projeto, abrir issues ou enviar pull requests.

Licença
Este projeto está licenciado sob a MIT License.
